---
title: Seguimiento de vínculos personalizados sin un Administrador de etiquetas
description: Para muchas acciones en la página, el seguimiento no debe tratarse como una vista de página. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como Experience Platform Launch). Consulte el código, además de aprender una sugerencia importante.
feature: appmeasurement implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
translation-type: tm+mt
source-git-commit: 8276828e9e759a1964ca5ea89bb1395e5e78b500
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 4%

---


# Seguimiento de vínculos personalizados sin un Administrador de etiquetas {#custom-link-tracking-without-a-tag-manager}

Para muchas acciones en la página, el seguimiento no debe tratarse como una vista de página. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como Adobe [!DNL Experience Platform Launch]). Consulte el código, además de aprender una sugerencia importante.

## Envío de una señalización s.tl() {#sending-an-s-tl-beacon}

Existen dos funciones que envían datos a Adobe Analytics:

1. s.t(): señalización de &quot;seguimiento&quot;, que es una visita individual de vista de página, que incrementa las vistas de página para un nombre de página determinado, así como también establece otras variables
1. s.tl(): señalización de &quot;seguimiento de vínculos&quot;, a la que se hace referencia con frecuencia como una señalización/visita de &quot;vínculo personalizado&quot;, que no incrementa las vistas de página y omite la variable pageName. Esto se utiliza generalmente para rastrear acciones más pequeñas en la página que no cargan una nueva página o pantalla, u otras acciones que no resulten en una nueva carga de página.

>[!NOTE]
>
>En este vídeo, le mostramos cómo codificar una visita de vínculo personalizado cuando NO está utilizando un administrador de etiquetas como Adobe [!DNL Experience Platform Launch]. Le recomendamos que utilice [!DNL Experience Platform Launch], nuestra recomendación de mejores prácticas para la implementación. Sin embargo, si necesita codificar en una `s.tl()`, así es como hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Código de muestra {#sample-code}

Este es el código de muestra utilizado en el vínculo personalizado del vídeo:

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```

Para obtener más información sobre los vínculos personalizados, consulte la [documentación](https://marketing.adobe.com/resources/help/es_ES/sc/implement/function_tl.html).