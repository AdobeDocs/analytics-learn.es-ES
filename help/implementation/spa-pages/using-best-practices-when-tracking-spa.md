---
title: 'Prácticas recomendadas para el seguimiento de aplicaciones de una sola página (SPA) en Adobe Analytics '
description: En este documento, describiremos varias prácticas recomendadas que debe seguir y tener en cuenta mientras utiliza Adobe Analytics para rastrear aplicaciones de una sola página (SPA). Este documento se centrará en el uso de Experience Platform Launch, que es el método de implementación recomendado.
feature: implementation basics
topics: spa
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
translation-type: tm+mt
source-git-commit: 548ac75589383dfd4da4ae02412de91a0a3b28d6
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 0%

---


# Prácticas recomendadas para el seguimiento de aplicaciones de una sola página (SPA) en Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

En este documento, describiremos varias prácticas recomendadas que debe seguir y tener en cuenta mientras utiliza Adobe Analytics para rastrear aplicaciones de una sola página (SPA). Este documento se centrará en el uso de Adobe [!DNL Experience Platform Launch], que es el método de implementación recomendado.

NOTAS INICIALES:

* Los siguientes elementos supondrán que se utiliza [!DNL Experience Platform Launch] para implementar en el sitio. Las consideraciones seguirían existiendo si no se utiliza [!DNL Experience Platform Launch], pero tendría que adaptarlas al método de implementación.
* Todos los SPA son diferentes, por lo que es posible que tenga que modificar algunos de los siguientes elementos para adaptarlos mejor a sus necesidades, pero queremos compartir con usted algunas prácticas recomendadas; cosas que debe tener en cuenta al implementar Adobe Analytics en las páginas de SPA.

## Diagrama sencillo del trabajo con SPA en [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa para análisis en inicio](assets/spa_for_analyticsinlaunch.png)

**NOTA:** Como se ha indicado, este es un diagrama simplificado de cómo se gestionan las páginas de SPA en una implementación de Adobe Analytics mediante [!DNL Experience Platform Launch]. En las siguientes secciones de esta página, analizaremos los pasos y los temas que debe considerar cuidadosamente o en los que debe actuar.

## Configuración de la capa de datos {#setting-the-data-layer}

Cuando se carga contenido nuevo en una página SPA o cuando se realiza una acción en una página SPA, una de las primeras acciones que debe realizar es actualizar la capa de datos. Esto debe suceder ANTES de que el evento personalizado se active y active las reglas en [!DNL Experience Platform Launch], de modo que [!DNL Experience Platform Launch] pueda recoger los nuevos valores de la capa de datos e insertarlos en Adobe Analytics.

A continuación se muestra una capa de datos de muestra, cuyos elementos podrían cambiarse al cambiar la vista o al realizar acciones en la SPA. Por ejemplo, en un cambio en la pantalla de mayoría/total, sería común cambiar un elemento &quot;[!DNL pageName]&quot; para que el nuevo se pueda capturar en [!DNL Experience Platform Launch] y enviar a Adobe Analytics.

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

## Configuración de Eventos personalizados y escucha en [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Cuando se cargue contenido nuevo en la página o cuando se produzca una acción en el sitio, querrá informar [!DNL Experience Platform Launch] para que pueda ejecutar una regla y enviar datos a [!DNL Analytics]. Hay un par de formas diferentes de hacerlo: [!UICONTROL Eventos personalizados o] reglas [!UICONTROL de llamadas] directas.

* [!UICONTROL Directas llamadas] [!UICONTROL reglas]: en [!DNL Experience Platform Launch], puede configurar una [!UICONTROL regla] de llamada  directa que se ejecute cuando se llame directamente desde la página. Si la carga de la página o la acción en el sitio es muy sencilla, o si es única y puede ejecutar un conjunto específico de instrucciones cada vez (configurado [!DNL eVar4] en X y activarse [!DNL event2] cada vez), puede utilizar una [!UICONTROL regla] de llamada directa. Consulte [!DNL Experience Platform Launch] la documentación relativa a la creación de [!UICONTROL reglas] de llamada directa.
* Eventos personalizados: Para obtener más funcionalidad y poder adjuntar dinámicamente una carga útil con diferentes valores, debe establecer eventos JavaScript personalizados y escucharlos en [!DNL Experience Platform Launch], donde puede utilizar la carga útil para configurar variables y enviar los datos a Adobe Analytics. Es más probable que necesite esta funcionalidad, por lo que esta opción se considera la práctica recomendada. Sin embargo, cada función del sitio puede determinar qué método es el más adecuado. Avanzaremos en este documento suponiendo que tendrá que utilizar este método de eventos personalizado.

**Ejemplos:** En [ESTE](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) documento de ayuda, hay vínculos a sitios de SPA de muestra que han implementado [!DNL Analytics] (y otras soluciones de Experience Cloud), así como documentos que describen lo que se ha implementado. En estos ejemplos de SPA se han utilizado los siguientes eventos personalizados:

* [!DNL event-view-start]:: Este evento debe activarse en el inicio de vista de la vista/estado que se está cargando.
* [!DNL event-view-end]:: Este evento debe activarse incluso cuando se ha producido un cambio de vista o estado y todos los componentes de SPA de la página han terminado de cargarse. Este es el evento que generalmente activa una llamada a Adobe Analytics.
* [!DNL event-action-trigger]:: Este evento debe activarse cuando se produzca cualquier evento en la página excepto la carga de estado o vista. Podría ser un evento de clics o un cambio de contenido más pequeño sin un cambio de vista.

Consulte los documentos o páginas a los que se hace referencia para obtener más información sobre cómo y cuándo se activan. No es necesario que utilice estos mismos nombres de evento, pero se recomiendan las funciones enumeradas aquí. El siguiente vídeo muestra un sitio de muestra y dónde se encuentra [!DNL Experience Platform Launch] para escuchar los eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ejecución de s.t() o s.tl() en la [!DNL Experience Platform Launch] [!UICONTROL regla] {#running-s-t-or-s-tl-in-the-launch-rule}

Una de las cosas más importantes para entender [!DNL Analytics] al trabajar con un SPA es la diferencia entre `s.t()` y `s.tl()`. Va a activar uno de estos métodos [!DNL Experience Platform Launch] para enviar datos a [!DNL Analytics], pero necesita saber cuándo enviar cada uno.

* **s.t()** : &quot;t&quot; significa &quot;track&quot; y es una vista de página normal. Aunque la dirección URL no cambie, ¿cambia la vista lo suficiente como para *considerarla* una nueva &quot;página&quot;? Si es así, configure la variable s.[!DNL pageName] y usar `s.t()` para enviar la llamada a [!DNL Analytics]

* **s.tl()** : &quot;tl&quot; significa &quot;vínculo de seguimiento&quot; y se utiliza normalmente para rastrear clics o pequeños cambios en el contenido de la página, a diferencia de un cambio en la pantalla completa. Si el cambio en la página es pequeño, para que no lo considere una &quot;página&quot; nueva completa, utilice `s.tl()` y no se preocupe por configurar la variable s.pageName, ya que la [!DNL Analytics] ignorará.

**SUGERENCIA:** Algunas personas utilizan una directriz general según la cual si la pantalla cambia más del 50 %, debe considerarse una vista de página y un uso `s.t()`. Si el cambio en la pantalla es inferior al 50 %, utilice `s.tl()`. Sin embargo, depende totalmente de usted y de lo que considere una nueva &quot;página&quot; y de cómo le gustaría rastrear su sitio en Adobe Analytics.

El siguiente vídeo muestra dónde y cómo activar `s.t()` o `s.tl()` en Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Borrado de variables {#clearing-variables}

Al rastrear su sitio con Adobe Analytics, por supuesto que sólo desea enviar los datos correctos en el [!DNL Analytics] momento adecuado. En un entorno de SPA, un valor rastreado en una [!DNL Analytics] variable puede persistir y ser reenviado a [!DNL Analytics], potencialmente cuando ya no lo queremos. Por este motivo, existe una función en la [!DNL Analytics] extensión para borrar las variables, de modo que tenga una pizarra nueva cuando ejecute la siguiente solicitud de imagen y envíe datos a [!DNL Launch] [!DNL Analytics].

En el diagrama anterior, se muestra al final del proceso, borrando las variables *después* de enviar la visita. En realidad, se puede hacer antes o después de que se envíe la visita, pero debe ser coherente en las [!DNL Experience Platform Launch] reglas, de modo que siempre borre antes o después de configurar las variables y enviarlas. Recuerde que si va a borrar las variables *antes* de ejecutarlas `s.t()`, asegúrese de borrar primero las variables, luego configure las nuevas variables y, finalmente, envíe los nuevos datos a [!DNL Analytics].

**NOTA:** No siempre es necesario borrar variables al ejecutarse `s.tl()`, ya que `s.tl()` requiere el uso de la [!DNL linkTrackVars] variable junto a ella cada vez para indicar [!DNL Analytics] qué variables se van a establecer (se agregan automáticamente entre bastidores en [!DNL Experience Platform Launch]). Esto significa que las variables errantes no suelen aparecer al usar `s.tl()`, pero se recomienda mucho cuando se usan `s.t()` en un entorno SPA. Dicho esto, me gustaría recomendarlo como una práctica recomendada utilizar la función Borrar variables tanto para `s.t()` como para `s.tl()` un entorno SPA, sólo para garantizar la recopilación de datos de calidad.

El siguiente vídeo muestra dónde y cómo borrar las variables en [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Consideraciones adicionales {#additional-considerations}

### Ventanas de código personalizado en [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

En la [!DNL Launch] [!DNL Analytics] extensión, hay dos lugares en los que puede insertar código personalizado: La sección Administración [!UICONTROL de] biblioteca y la sección adicional &quot;[!UICONTROL Configurar rastreador usando código]personalizado&quot;.

![Iniciar ventanas de código personalizado de Analytics](assets/launch_analyticscustomcodewindows.png)

Es importante saber que cualquiera de estas ubicaciones solo va a ejecutar el código una vez, cuando la carga de página inicial se produce en la página de SPA. Si necesita que el código se ejecute en un cambio de vista o en una acción del sitio, debe agregar una acción adicional a la **[!UICONTROL regla]** correspondiente (por ejemplo, en la &quot;carga de página: &quot;Fin de vista de evento&quot; ( [!UICONTROL regla]), de modo que el código se ejecute cada vez que se ejecute la [!UICONTROL regla] . Al crear esa acción en la [!UICONTROL regla], establezca *Extension = Core* y Tipo de *acción = Código* personalizado.

### SPA &quot;híbrida&quot;/Sitios regulares {#hybrid-spa-regular-sites}

Algunos sitios son una combinación de páginas &quot;regulares&quot; y páginas de SPA. En este caso, deberá utilizar una estrategia que funcione para ambos tipos de página. Al configurar los eventos personalizados en el sitio y activar las reglas en [!DNL Experience Platform Launch], tenga cuidado de que no haya visitas de doble que entren [!DNL Analytics] desde la página, en base a los cambios de hash, etc. (si así es como ha elegido activar la [!DNL Experience Platform Launch] regla). En este caso, deberá suprimir una de las vistas de página para que no le proporcione datos defectuosos en Adobe Analytics.

Si decide desglosar la funcionalidad en [!UICONTROL reglas] separadas para que tenga más control sobre ella, asegúrese de recordar/documento de que lo ha hecho, para que cualquier cambio en una [!UICONTROL regla] también se pueda realizar en la otra [!UICONTROL regla] , protegiendo así la integridad [!DNL Analytics] de los datos.

### Integración con [!DNL Target] mediante A4T {#integration-with-target-via-a4t}

Sólo una llamada rápida aquí. Si está realizando la integración con [!DNL Target] A4T, asegúrese de que la [!DNL Target] solicitud y la [!DNL Analytics] solicitud del mismo cambio de vista tengan el mismo SDID. Esto garantizará que los datos se sincronicen correctamente en las soluciones.

Para ver las visitas, utilice un depurador o un programa de husmeador de paquetes. También puede utilizar el Experience Cloud Debugger, una extensión de Chrome que se puede descargar [AQUÍ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] debe activarse primero en la página, así que también puede comprobarlo en la consola de JavaScript o en el depurador.

## Recursos adicionales {#additional-resources}

* [Debate de la SPA en los foros de Adobe](https://forums.adobe.com/thread/2451022)
* [Sitios de arquitectura de referencia para mostrar cómo implementar SPA en Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)