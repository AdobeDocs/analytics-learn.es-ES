---
title: Cómo identificar el servidor de seguimiento y los grupos de informes de Analytics
description: Al configurar Adobe Analytics o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el "servidor de seguimiento" de Analytics que utiliza, o también el "grupo de informes" al que envía los datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.
feature: Conceptos básicos de implementación
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: '"Desarrollador, ingeniero de datos"'
level: Principiante
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---


# Cómo identificar sus [!DNL Tracking Server] y [!UICONTROL grupos de informes] {#how-to-identify-your-analytics-tracking-server-and-report-suites} de Analytics

Al configurar Adobe Analytics o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que está utilizando o también el &quot;[!UICONTROL Grupo de informes]&quot; al que está enviando los datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.

## Después de la implementación {#after-implementation}

Después de implementar [!DNL Analytics] en un sitio, puede encontrar el [!DNL tracking server] y el [!DNL report suite ID] derecho en la señalización de seguimiento. El [!DNL tracking server] es el nombre de host de la señalización, por lo que es fácil de encontrar. Los [!UICONTROL ID del grupo de informes] son una lista separada por comas justo después de &quot;/b/ss/&quot; en el nombre de ruta de la señalización.

Para ver la señalización, así como toda la información que llega a [!DNL Analytics] y otras soluciones de Experience Cloud, instale la extensión de Chrome [&quot;Experience Cloud Debugger&quot;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=es).

## Antes de la implementación {#before-implementation}

**[!DNL Tracking Server]** - Si todavía no ha empezado con la implementación de Adobe Analytics, debe elegir un subdominio para &quot;.sc.omtrdc.net&quot;  [!DNL tracking server]. Por ejemplo, supongamos que tengo una tienda de sombreros en línea llamada &quot;Jim&#39;s Brims&quot;. Simplemente puedo establecer mi [!DNL tracking server] en:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Grupo de informes]** : para encontrar una lista de los grupos de  [!UICONTROL informes ] que se han creado, inicie sesión  [!DNL Analytics] y vaya a  [!UICONTROL Administración]  >  [!UICONTROL Grupos de ] informes en el menú superior para ver una lista de los grupos de  [!UICONTROL informes], incluidos su ID y título.

Consulte el siguiente vídeo para obtener más información.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
