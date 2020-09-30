---
title: Cómo identificar el servidor de seguimiento y los grupos de informes de Analytics
description: Al configurar Adobe Analytics, o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el "servidor de seguimiento" de Analytics que está utilizando, o también el "grupo de informes" al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.
feature: implementation basics
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
translation-type: tm+mt
source-git-commit: 60f4ce4f563a990576b3331b01cd87c29d424f43
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 2%

---


# Cómo identificar sus grupos de [!DNL Tracking Server] informes [!UICONTROL y análisis] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Al configurar Adobe Analytics, o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que está utilizando o también el &quot;grupo[!UICONTROL de]informes&quot; al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.

## Después de la implementación {#after-implementation}

Después de realizar la implementación [!DNL Analytics] en un sitio, puede encontrar la señalización de seguimiento [!DNL tracking server] y la [!DNL report suite ID] derecha. El [!DNL tracking server] es el nombre de host en la señalización, por lo que es fácil encontrarlo. Las ID del grupo [!UICONTROL de] informes son una lista separada por comas justo después de &quot;/b/ss/&quot; en el nombre de ruta de la señalización.

Para ver la señalización, así como cualquier otra información que se reciba [!DNL Analytics] y otras soluciones de Experience Cloud, instale la extensión [de Chrome](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=es)&quot;Experience Cloud Debugger&quot;.

## Antes de la implementación {#before-implementation}

**[!DNL Tracking Server]** - Si todavía no ha comenzado la implementación de Adobe Analytics, elegirá un subdominio para &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Por ejemplo, digamos que tengo una sombrerería en línea llamada &quot;Jim’s Brims&quot;. Simplemente puedo establecer mi [!DNL tracking server] objetivo:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Grupo]** de informes: para encontrar una lista de los grupos [!UICONTROL de] informes que se han creado, inicie sesión [!DNL Analytics] y vaya a [!UICONTROL Administración] > Grupos [!UICONTROL de] informes en el menú superior para ver una lista de los grupos de informes, incluyendo su ID y título.

Consulte el siguiente vídeo para obtener más información.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
