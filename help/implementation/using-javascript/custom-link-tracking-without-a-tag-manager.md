---
title: Seguimiento de vínculos personalizados sin un Administrador de etiquetas
description: Para muchas acciones de la página, el seguimiento no debe tratarse como una vista de páginas. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como un Experience Platform Launch). Consulte el código, así como esta sugerencia importante.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
TQID: https://experienceleague.adobe.com/BU98KM1JAq3v6Gd7SRU0FNT3qW-4a9UvP0M-ffFqJIA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 100%

---

# Seguimiento de vínculos personalizados sin un Administrador de etiquetas {#custom-link-tracking-without-a-tag-manager}

Para muchas acciones de la página, el seguimiento no debe tratarse como una vista de páginas. En este vídeo, aprenderá a codificar una señalización de seguimiento de vínculos en Analytics si no utiliza un administrador de etiquetas (como Adobe [!DNL Experience Platform Launch]). Consulte el código, así como esta sugerencia importante.

## Envío de una señalización s.tl() {#sending-an-s-tl-beacon}

Existen dos funciones que envían datos a Adobe Analytics:

1. s.t() - una señalización de “seguimiento”, que es una visita de vista de páginas, que incrementa las vistas de página para el nombre de página dado, así como otras variables
1. s.tl() - una señalización de “seguimiento de vínculos”, que a menudo se denomina visita/señalización de “vínculo personalizado”, que no incrementa las vistas de página, e ignora la variable pageName. Esto se utiliza comúnmente para rastrear acciones más pequeñas en la página que no cargan una nueva página o pantalla, u otras acciones que no resultan en una nueva carga de página.

>[!NOTE]
>
>En este vídeo, le mostramos cómo codificar una visita de vínculo personalizado cuando NO está utilizando un administrador de etiquetas como Adobe [!DNL Experience Platform Launch]. Le recomendamos que utilice [!DNL Experience Platform Launch], nuestras prácticas recomendadas para la implementación. Sin embargo, si necesita codificar en un `s.tl()`, así es como hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/34536/?captions=spa&quality=12&learn=on)

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
