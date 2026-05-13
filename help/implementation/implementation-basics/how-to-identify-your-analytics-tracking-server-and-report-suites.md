---
title: Cómo identificar el servidor de seguimiento y el ID del grupo de informes de Analytics
description: Al configurar Adobe Analytics, o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el "servidor de seguimiento" de Analytics que está utilizando, o incluso el "grupo de informes" al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, tanto si ya ha implementado Adobe Analytics como si no.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
TQID: https://experienceleague.adobe.com/DRy-lxNuEQR9Tb-nIoev0Mu1OzSiCcLcqve1eDf7p6Q
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 334
ht-degree: 100%

---

# Cómo identificar el [!DNL tracking server] y el [!UICONTROL grupo de informes] de Analytics {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Al configurar Adobe Analytics o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el &quot;servidor de seguimiento&quot; de Analytics que está utilizando o también el &quot;[!UICONTROL grupo de informes]&quot; al que va a enviar datos. Este vídeo muestra cómo localizar ambos valores, tanto si ya ha implementado Adobe Analytics como si no.

>[!IMPORTANT]
>
>Este artículo y vídeo hacen referencia a una implementación de &quot;AppMeasurement&quot; de Adobe Analytics y no a una implementación que utiliza el SDK web.

## Después de la implementación {#after-implementation}

Después de implementar Analytics en un sitio, puede encontrar el [!DNL tracking server] y el [!DNL report suite ID] justo en la baliza de seguimiento. [!DNL tracking server] es el nombre del servidor de la baliza, por lo que es fácil encontrarlo. Los ID del [!UICONTROL grupo de informes] son una lista separada por comas justo después de “/b/ss/” en el nombre de ruta de la baliza.

Para ver la baliza, así como toda la información que llegue a Analytics y a otras soluciones de Experience Cloud, instale la [extensión de chrome de Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=es).

## Antes de la implementación {#before-implementation}

**[!DNL Tracking server]**: si todavía no ha comenzado con la implementación de Adobe Analytics, elegirá un subdominio para “.sc.omtrdc.net”[!DNL tracking server]. Por ejemplo, supongamos que tengo una tienda de sombreros en línea que se llama &quot;Jim’s Brims&quot;. Puedo simplemente configurar mi [!DNL tracking server] en:

“jimsbrims.sc.omtrdc.net”.

**[!UICONTROL Grupo de informes]**: para encontrar una lista de los [!UICONTROL grupos de informes] que se han creado, inicie sesión en [!DNL Analytics] y vaya a [!UICONTROL Administración] > [!UICONTROL Grupos de informes] en el menú superior para ver una lista de los [!UICONTROL grupos de informes], incluidos su ID y título.

Consulte el siguiente vídeo para obtener más información.

>[!VIDEO](https://video.tv.adobe.com/v/40897/?captions=spa&quality=12&learn=on)
