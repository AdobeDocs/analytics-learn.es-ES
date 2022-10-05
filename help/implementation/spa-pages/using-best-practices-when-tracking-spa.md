---
title: Prácticas recomendadas de implementación para aplicaciones de una sola página (SPA)
description: Conozca algunas prácticas recomendadas para implementar Adobe Analytics en aplicaciones de una sola página (SPA). Esto incluye el uso de etiquetas de Experience Platform, el método de implementación recomendado.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 2%

---

# Prácticas recomendadas de implementación para aplicaciones de una sola página (SPA) {#implementation-best-practices-for-single-page-appliations}

Conozca algunas prácticas recomendadas para implementar [!DNL Adobe Analytics] en aplicaciones de una sola página (SPA). Esto incluye el uso de [!DNL Experience Platform Tags], el método de implementación recomendado.

NOTAS INICIALES:

* El contenido siguiente hace referencia al uso de [!DNL Experience Platform Tags] para implementar Adobe Analytics en el sitio. Estas consideraciones se aplican si [!DNL Experience Platform Tags] no se utiliza, por lo tanto, debe adaptarlos al método de implementación.
* Existen diferencias en SPA, por lo tanto, debe ajustar su enfoque en consecuencia para satisfacer mejor sus necesidades.

## Diagrama sencillo del trabajo con SPA en [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA para analytics en etiquetas](assets/spa_for_analyticsinlaunch.png)

**NOTA:** Este es un diagrama simplificado de cómo se gestionan SPA páginas en una implementación de Adobe Analytics mediante [!DNL Experience Platform Tags]. En las secciones siguientes se identifican los pasos y los problemas que se deben tener en cuenta.

## Establecer la capa de datos {#set-the-data-layer}

Cuando se carga contenido nuevo o cuando se produce una acción en una página SPA, *actualice primero la capa de datos*. Esto debe suceder **before** un evento personalizado que déclencheur la ejecución de una regla en [!DNL Experience Platform Tags]. Esto garantiza que los valores correctos de la capa de datos se inserten en las etiquetas y, a continuación, en Adobe Analytics.

A continuación se muestra una capa de datos de ejemplo. Cualquiera de estos elementos puede cambiar según la vista inicial o el cambio posterior de la vista, dado que se ha realizado una acción en la página de SPA. Por ejemplo, en un cambio de vista completo o mayoritario, es un requisito común pasar un &quot;[!DNL pageName]&quot; para diferenciar entre las vistas de los informes de Adobe Analytics.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Configure eventos personalizados y escuche estos eventos en [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Cuando se carga contenido nuevo o cuando se produce una acción en la página SPA, se debe informar a las etiquetas del Experience Platform para que ejecuten una regla que envíe datos a [!DNL Analytics]. Hay un par de enfoques para esto: [!UICONTROL Reglas de llamada directa] o Eventos personalizados.

* [!UICONTROL Reglas de llamada directa]: Configure un [!UICONTROL regla de llamada directa] que se ejecuta cuando se llama directamente desde la página. Si la carga o la acción de la página es simple o única y puede ejecutar un conjunto específico de instrucciones cada vez (por ejemplo, configurar [!DNL eVar4] a X y déclencheur [!DNL event2] cada vez), entonces este enfoque es adecuado. Consulte [!DNL Experience Platform Tags] documentación para obtener más información sobre la creación [!UICONTROL reglas de llamada directa].
* Eventos personalizados: Si necesita adjuntar dinámicamente una carga útil con valores únicos para los eventos que se producen en SPA páginas, utilice eventos de JavaScript personalizados y escuche en [!DNL Experience Platform Tags]. Utilice la carga útil para establecer elementos de datos y variables de Analytics en Etiquetas. Este método se considera una práctica recomendada, ya que esta necesidad suele prevalecer para SPA. Nuestros ejemplos siguientes utilizan el método de eventos personalizados.

**Ejemplos:** [En este](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) documento de ayuda, hay vínculos a sitios de SPA de ejemplo que implementan [!DNL Analytics] y otras soluciones de Experience Cloud. En estos ejemplos se utilizan los siguientes eventos personalizados:

* **[!DNL Event-view-start]**: Se ejecuta al inicio de la vista de la vista o el estado que se carga.
* **[!DNL Event-view-end]**: Se ejecuta cuando se produce un cambio de vista/estado y todos los componentes SPA de la página terminan de cargarse. Este es el evento que suele enviar datos a Adobe Analytics.
* **[!DNL Event-action-trigger]**: Se ejecuta cuando se produce cualquier evento en la página excepto la carga de vista/estado. Algunos ejemplos de esto son un evento de clic o un cambio de contenido más pequeño sin un cambio de vista.

Consulte las páginas y los documentos a los que se hace referencia anteriormente para obtener más información sobre cómo y cuándo se activan estos eventos. No es necesario que utilice los mismos nombres de evento en la implementación. El caso de uso funcional del método utilizado es esencial para entenderlo como la mejor práctica recomendada para cada uno. El siguiente vídeo muestra una página SPA de muestra y un código de muestra en [!DNL Experience Platform Tags] que escucha los eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ejecute s.t() o s.tl() en la variable [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Un concepto importante para [!DNL Analytics] al trabajar con un SPA es la diferencia entre `s.t()` y `s.tl()`. El código déclencheur uno de estos métodos en [!DNL Experience Platform Tags] para enviar datos a [!DNL Analytics].

* **s.t()** - La &quot;t&quot; significa &quot;track&quot; y representa una vista de página. Si la vista cambia lo suficiente como para que  *considere* es una nueva &quot;página&quot;, utilice esta llamada . Establezca un valor único en la variable [!DNL s.pageName] y use `s.t()` para enviar los datos a [!DNL Analytics].

* **s.tl()** : &quot;tl&quot; significa &quot;vínculo de seguimiento&quot; y representa un clic en vínculo o un pequeño cambio en el contenido. Si el cambio de vista es mínimo, utilice `s.tl()` para pasar un valor único sobre la interacción a [!DNL Analytics]. Esta variable transferida no [!DNL s.pageName], ya que esto se ignora en Analytics cuando `s.tl()` se reciben las llamadas de .

**SUGERENCIA:** Como guía general, si la pantalla cambia en más del 50 %, utilice la variable `s.t()` vista de página . De lo contrario, utilice `s.tl()`. Sin embargo, juzgue las acciones que constituyen una nueva &quot;página&quot; y cómo deben presentarse en los informes de Adobe Analytics.

El siguiente vídeo muestra dónde y cómo realizar el déclencheur `s.t()` o `s.tl()` en Etiquetas.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Borrar variables {#clear-variables}

Enviar los datos adecuados a [!DNL Analytics] en el momento adecuado. En un entorno SPA, un valor almacenado en un [!DNL Analytics] persiste y se reenvía a [!DNL Analytics], potencialmente cuando ya no lo desea. Existe una función en la variable [!DNL Analytics] [!DNL Tags] para borrar las variables y garantizar que la siguiente llamada no envíe datos de forma errante a [!DNL Analytics].

El diagrama anterior muestra las variables borradas *after* los datos se envían. En realidad, esto puede suceder antes O después de la llamada, sin embargo, sea coherente en su [!DNL Experience Platform Tags] reglas para una implementación más limpia. Si borra las variables *before* ejecute `s.t()`, configure las nuevas variables inmediatamente después de la llamada de y, a continuación, proceda a enviar los nuevos datos a [!DNL Analytics].

**NOTA:** No siempre es necesario borrar variables al ejecutar `s.tl()`. Esta llamada requiere el uso de la variable [!DNL linkTrackVars] para ordenar [!DNL Analytics] qué variables se van a establecer. Esto sucede automáticamente [!DNL Experience Platform Tags] mediante la configuración. Evita que las variables errantes se configuren en contraste con el comportamiento con `s.t()` en un entorno SPA. Para garantizar la implementación más limpia y fiable, es probable que sea más fácil utilizar la función clear variables para ambas llamadas en un entorno SPA.

El siguiente vídeo muestra dónde y cómo borrar variables en [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Consideraciones adicionales {#additional-considerations}

### Ventanas Código personalizado en [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

En el [!DNL Tags] [!DNL Analytics] , hay dos lugares en los que se puede insertar código personalizado: La variable[!UICONTROL administración de bibliotecas]&quot; y &quot;[!UICONTROL Configuración del rastreador con código personalizado]&quot;.

![Etiquetas Ventanas de código personalizado de Analytics](assets/launch_analyticscustomcodewindows.png)

Cualquiera de estas ubicaciones ejecuta el código contenido en él una vez para la carga inicial de la página SPA. Si el código debe ejecutarse en una vista o cambio de acción, implemente ese código en el **[!UICONTROL regla]** (por ejemplo, la carga de página: &quot;event-view-end&quot;), para garantizar que el código se ejecute cada vez que se ejecute la función [!UICONTROL regla] se ejecuta. Al crear la acción en la variable [!UICONTROL regla], conjunto *Extensión = Core* y *Tipo de acción = Código personalizado*.

### SPA &quot;híbridos&quot; y sitios tradicionales {#hybrid-spa-and-traditional-sites}

Algunos sitios están compuestos por una combinación de páginas tradicionales y SPA. En este caso, utilice una estrategia que funcione para ambos tipos de página. Al configurar los eventos personalizados del sitio y activar las reglas en [!DNL Experience Platform Tags], asegúrese de que las visitas dobles no se envíen a [!DNL Analytics] en función de cambios hash, etc. En este caso, suprima una de las vistas de página para evitar que se pasen datos duplicados a Adobe Analytics.

Si decide separar la funcionalidad en una única [!UICONTROL reglas] para obtener más control, recuerde documentar que ha hecho esto. Si cambia una [!UICONTROL regla], realice el mismo cambio que el otro [!UICONTROL regla].

### Integración con [!DNL Target] Uso de A4T {#integration-with-target-using-a4t}

Al integrar con [!DNL Target] con A4T, confirme que la variable [!DNL Target] y [!DNL Analytics] las solicitudes enviadas en la misma vista o acción pasan el mismo valor de parámetro SDID. Esto garantiza que los datos se sincronicen correctamente en el servidor.

Para ver estas visitas, utilice un depurador o una herramienta de monitorización de paquetes. Adobe proporciona un depurador Experience Platform para este fin. Es una extensión de Chrome que puede ser [descargado aquí](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=en). [!DNL Target] debe ejecutarse primero en la página. Esto también se puede comprobar en Debugger.

## Recursos adicionales {#additional-resources}

* [Debate SPA en los foros de Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Sitios de arquitectura de referencia para mostrar cómo implementar SPA en Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
