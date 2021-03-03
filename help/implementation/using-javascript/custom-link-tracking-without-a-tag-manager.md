---
title: Seguimiento de vínculos personalizados sin un Administrador de etiquetas
description: Para muchas acciones de la página, el seguimiento no debe tratarse como una vista de página. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como Experience Platform Launch). Consulte el código, así como una sugerencia importante.
feature: Implementación De Appmeasurement
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: '"Desarrollador, ingeniero de datos"'
level: Intermedio
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 4%

---


# Seguimiento de vínculos personalizados sin un Administrador de etiquetas {#custom-link-tracking-without-a-tag-manager}

Para muchas acciones de la página, el seguimiento no debe tratarse como una vista de página. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como Adobe [!DNL Experience Platform Launch]). Consulte el código, así como una sugerencia importante.

## Envío de una señalización s.tl() {#sending-an-s-tl-beacon}

Existen dos funciones que envían datos a Adobe Analytics:

1. s.t() : señalización de &quot;seguimiento&quot;, que es una visita de vista de página, que incrementa las vistas de página para el nombre de página dado, así como otras variables
1. s.tl() : señalización de &quot;seguimiento de vínculos&quot;, que a menudo se denomina visita/señalización de &quot;vínculo personalizado&quot;, que no incrementa las vistas de página, e ignora la variable pageName . Esto se utiliza comúnmente para rastrear acciones más pequeñas en la página que no cargan una nueva página o pantalla, u otras acciones que no resultan en una nueva carga de página.

>[!NOTE]
>
>En este vídeo, le mostramos cómo codificar una visita de vínculo personalizado cuando NO está utilizando un administrador de etiquetas como Adobe [!DNL Experience Platform Launch]. Le recomendamos que utilice [!DNL Experience Platform Launch], nuestra recomendación de prácticas recomendadas para la implementación. Sin embargo, si necesita codificar en un `s.tl()`, así es como hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Código de muestra {#sample-code}

Este es un ejemplo de código utilizado en el vínculo personalizado del vídeo:

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