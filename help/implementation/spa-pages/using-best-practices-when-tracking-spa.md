---
title: 'Prácticas recomendadas para el seguimiento de aplicaciones de una sola página (SPA) en Adobe Analytics '
description: En este documento, describiremos varias prácticas recomendadas que debe seguir y tener en cuenta a medida que utiliza Adobe Analytics para rastrear aplicaciones de una sola página (SPA). Este documento se centrará en el uso de Experience Platform Launch, que es el método de implementación recomendado.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: "Developer, Data Engineer"
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 0%

---


# Prácticas recomendadas para el seguimiento de aplicaciones de una sola página (SPA) en Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

En este documento, describiremos varias prácticas recomendadas que debe seguir y tener en cuenta a medida que utiliza Adobe Analytics para rastrear aplicaciones de una sola página (SPA). Este documento se centrará en el uso de Adobe [!DNL Experience Platform Launch], que es el método de implementación recomendado.

NOTAS INICIALES:

* Los elementos siguientes asumirán que está utilizando [!DNL Experience Platform Launch] para implementar en el sitio. Las consideraciones seguirían existiendo si no utiliza [!DNL Experience Platform Launch], pero tendría que adaptarlas a su método de implementación.
* Todas las SPA son diferentes, por lo que es posible que tenga que modificar algunos de los siguientes elementos para adaptarlos a sus necesidades, pero quisimos compartir algunas prácticas recomendadas con usted; cosas que debe tener en cuenta al implementar Adobe Analytics en páginas de SPA.

## Diagrama sencillo del trabajo con SPA en [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa para análisis en launch](assets/spa_for_analyticsinlaunch.png)

**NOTA:** Como se ha indicado, este es un diagrama simplificado de cómo se gestionan las páginas de SPA en una implementación de Adobe Analytics mediante  [!DNL Experience Platform Launch]. En las secciones siguientes de esta página, analizaremos los pasos y cualquier tema que debe considerar cuidadosamente o sobre el que debe actuar.

## Configuración de la capa de datos {#setting-the-data-layer}

Cuando se carga contenido nuevo en una página de SPA, o cuando se realiza una acción en una página de SPA, una de las primeras cosas que debe hacer es actualizar la capa de datos. Esto debe suceder ANTES de que el evento personalizado se active y active las reglas en [!DNL Experience Platform Launch], de modo que [!DNL Experience Platform Launch] pueda recoger los nuevos valores de la capa de datos e insertarlos en Adobe Analytics.

A continuación se muestra una capa de datos de ejemplo, cuyos elementos podrían cambiarse al cambiar la vista o la acción en su SPA. Por ejemplo, en un cambio de pantalla completo/mayoritario, sería común cambiar un elemento &quot;[!DNL pageName]&quot;, de modo que el nuevo se pueda capturar en [!DNL Experience Platform Launch] y enviarse a Adobe Analytics.

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

## Configuración de eventos personalizados y escucha en [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Cuando se carga contenido nuevo en la página o cuando se produce una acción en el sitio, se recomienda informar a [!DNL Experience Platform Launch] para que pueda ejecutar una regla y enviar datos a [!DNL Analytics]. Hay un par de formas diferentes de hacerlo: [!UICONTROL Llamada directa] [!UICONTROL reglas] o Eventos personalizados.

* [!UICONTROL Reglas de ] [!UICONTROL llamada directa]: en  [!DNL Experience Platform Launch], puede configurar una regla de llamada  [!UICONTROL directa ]  que se ejecute cuando se llame directamente desde la página. Si la carga de la página o la acción en el sitio es muy sencilla, o si es única y puede ejecutar un conjunto específico de instrucciones cada vez (establezca [!DNL eVar4] en X y active [!DNL event2] cada vez), puede utilizar una [!UICONTROL llamada directa] [!UICONTROL regla]. Consulte la documentación [!DNL Experience Platform Launch] sobre la creación de [!UICONTROL reglas] de [!UICONTROL llamada directa].
* Eventos personalizados: Para obtener más funcionalidad y para poder adjuntar dinámicamente una carga útil con diferentes valores, debe configurar eventos JavaScript personalizados y escucharlos en [!DNL Experience Platform Launch], donde puede utilizar la carga útil para establecer variables y enviar los datos a Adobe Analytics. Es más probable que necesite esta funcionalidad y, por lo tanto, esta opción se considera la práctica recomendada. Sin embargo, cada función del sitio puede determinar qué método es el más adecuado. En este documento avanzaremos suponiendo que necesite utilizar este método de eventos personalizado.

**Ejemplos:** En  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) ESTE documento de ayuda, hay vínculos a sitios de SPA de muestra que se han implementado  [!DNL Analytics] (y otras soluciones de Experience Cloud), así como documentos que describen lo que se ha implementado. En estos ejemplos de SPA se han utilizado los siguientes eventos personalizados:

* [!DNL event-view-start]: Este evento debe activarse al inicio de la vista del estado que se está cargando.
* [!DNL event-view-end]: Este evento debe activarse incluso cuando se ha producido un cambio de vista/estado y todos los componentes de SPA de la página han terminado de cargarse. Este es el evento que generalmente activa una llamada a Adobe Analytics.
* [!DNL event-action-trigger]: Este evento se debe activar cuando se produzca cualquier evento en la página excepto en la carga de vista/estado. Podría ser un evento de clic o un cambio de contenido más pequeño sin un cambio de vista.

Consulte las páginas o documentos a los que se hace referencia para obtener más información sobre cómo y cuándo se activan. No es necesario que utilice estos mismos nombres de evento, pero la funcionalidad que se enumera aquí es una práctica recomendada. El siguiente vídeo muestra un sitio de muestra y dónde en [!DNL Experience Platform Launch] para escuchar los eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ejecución de s.t() o s.tl() en la [!DNL Experience Platform Launch] [!UICONTROL Regla] {#running-s-t-or-s-tl-in-the-launch-rule}

Una de las cosas más importantes que se deben comprender para [!DNL Analytics] al trabajar con una SPA es la diferencia entre `s.t()` y `s.tl()`. Se activará uno de estos métodos en [!DNL Experience Platform Launch] para enviar datos a [!DNL Analytics], pero es necesario que sepa cuándo enviarlos.

* **s.t()** : la &quot;t&quot; significa &quot;track&quot; y es una vista de página normal. Aunque la dirección URL no cambie, ¿cambia lo suficiente la vista para que *considere* como una nueva &quot;página&quot;? Si es así, configure la variable s.[!DNL pageName] y utilice `s.t()` para enviar la llamada a [!DNL Analytics]

* **s.tl()** : &quot;tl&quot; significa &quot;vínculo de seguimiento&quot; y se utiliza normalmente para rastrear clics o pequeños cambios de contenido en la página, en contraposición a un cambio de pantalla completa. Si el cambio en la página es pequeño, para que no lo considere una nueva &quot;página&quot; completa, utilice `s.tl()` y no se preocupe por configurar la variable s.pageName, ya que [!DNL Analytics] la ignorará.

**SUGERENCIA:** Algunas personas utilizan una guía general que indica que si la pantalla cambia más del 50 %, debe considerarse una vista de página y usarla  `s.t()`. Si el cambio a la pantalla es inferior al 50%, utilice `s.tl()`. Sin embargo, depende totalmente de usted y de lo que considere una nueva &quot;página&quot; y de cómo le gustaría rastrear su sitio en Adobe Analytics.

El siguiente vídeo muestra dónde/cómo activar `s.t()` o `s.tl()` en Launch mediante Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Borrado de variables {#clearing-variables}

Al rastrear su sitio con Adobe Analytics, por supuesto, solo desea enviar los datos correctos a [!DNL Analytics] en el momento adecuado. En un entorno de SPA, un valor rastreado en una variable [!DNL Analytics] puede persistir y reenviarse a [!DNL Analytics], posiblemente cuando ya no lo deseamos. Por este motivo, existe una función en la extensión [!DNL Analytics] [!DNL Launch] para borrar las variables, de modo que tenga una pizarra nueva cuando ejecute la siguiente solicitud de imagen y envíe datos a [!DNL Analytics].

En el diagrama anterior, lo tenemos listado al final del proceso, borrando las variables *después* que envía en la visita. En realidad, se puede hacer antes o después de que la visita se envíe, pero debe ser coherente en las reglas [!DNL Experience Platform Launch], de modo que siempre borre antes o después de configurar las variables y enviarlas. Recuerde, si va a borrar las variables *antes* de ejecutar `s.t()`, asegúrese de borrar las variables primero, luego establecer las variables nuevas y, finalmente, enviar los nuevos datos a [!DNL Analytics].

**NOTA:** No siempre es necesario borrar variables al ejecutarse  `s.tl()`, ya que  `s.tl()` requiere el uso de la  [!DNL linkTrackVars] variable junto a ella cada vez para indicar  [!DNL Analytics] qué variables se van a configurar (se añaden automáticamente entre bastidores en  [!DNL Experience Platform Launch]). Esto significa que las variables errantes no suelen aparecer al utilizar `s.tl()`, pero es muy recomendable cuando se utiliza `s.t()` en un entorno SPA. Dicho todo esto, me gustaría recomendarlo como una práctica recomendada para utilizar la función Clear Variables tanto para `s.t()` como para `s.tl()` en un entorno SPA, solo para garantizar la recopilación de datos de calidad.

El siguiente vídeo muestra dónde/cómo borrar las variables en [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Consideraciones adicionales {#additional-considerations}

### Ventanas de código personalizado en [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

En la extensión [!DNL Launch] [!DNL Analytics] hay dos lugares en los que puede insertar código personalizado: La sección [!UICONTROL administración de biblioteca] y la sección adicional &quot;[!UICONTROL Configurar rastreador usando código personalizado]&quot;.

![Ventanas de código personalizado de Launch Analytics](assets/launch_analyticscustomcodewindows.png)

Es importante saber que cualquiera de estas ubicaciones solo va a ejecutar el código una vez, cuando la carga inicial de la página SPA se produce en la página SPA. Si necesita que el código se ejecute en un cambio de vista o en una acción de su sitio, debe agregar una Acción adicional a la **[!UICONTROL regla]** apropiada (por ejemplo, en la &quot;carga de página&quot;: event-view-end&quot; [!UICONTROL rule]), de modo que el código se ejecute cada vez que se ejecute [!UICONTROL rule]. Al crear esa acción en la [!UICONTROL regla], establezca *Extensión = Core* y *Tipo de acción = Custom Code*.

### SPA/Sitios regulares &quot;híbridos&quot; {#hybrid-spa-regular-sites}

Algunos sitios son una combinación de páginas &quot;regulares&quot; y páginas de SPA. En este caso, deberá utilizar una estrategia que funcione para ambos tipos de página. Al configurar los eventos personalizados en el sitio y activar las reglas en [!DNL Experience Platform Launch], asegúrese de que no haya visitas dobles que entren en [!DNL Analytics] desde la página, en función de cambios hash, etc. (si así es como ha elegido activar la regla [!DNL Experience Platform Launch]). En este caso, deberá suprimir una de las vistas de página para que no le proporcione datos defectuosos en Adobe Analytics.

Si decide dividir la funcionalidad en [!UICONTROL reglas] separadas para tener más control sobre ella, asegúrese de recordar/documentar que lo ha hecho, de modo que cualquier cambio en una [!UICONTROL regla] también se pueda realizar en la otra [!UICONTROL regla], protegiendo su [!DNL Analytics] integridad de datos.

### Integración con [!DNL Target] mediante A4T {#integration-with-target-via-a4t}

Un breve llamado aquí. Si está integrando con [!DNL Target] mediante A4T, asegúrese de que la solicitud [!DNL Target] y la solicitud [!DNL Analytics] del mismo cambio de vista tengan el mismo SDID. Esto garantizará que los datos se sincronicen correctamente en las soluciones.

Para ver las visitas, utilice un depurador o un programa de husmeador de paquetes. También puede utilizar Experience Cloud Debugger, una extensión de Chrome que se puede descargar [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] debe activarse primero en la página, por lo que también puede comprobarlo en la consola de JavaScript o en el depurador.

## Recursos adicionales {#additional-resources}

* [Debate sobre la SPA en los foros de Adobe](https://forums.adobe.com/thread/2451022)
* [Sitios de arquitectura de referencia para mostrar cómo implementar SPA en Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)