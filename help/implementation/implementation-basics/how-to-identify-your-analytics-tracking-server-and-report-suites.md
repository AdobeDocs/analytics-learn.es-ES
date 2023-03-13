---
title: Cómo identificar el servidor de seguimiento y los grupos de informes de Analytics
description: Al configurar Adobe Analytics, o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el servidor de seguimiento de Analytics que está utilizando, o incluso el grupo de informes al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 100%

---

# Cómo identificar el [!DNL Tracking Server] y el [!UICONTROL grupo de informes] de Analytics {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Al configurar Adobe Analytics o al hacer referencia a este en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el [!DNL Analytics] “[!DNL Tracking Server]” que está utilizando o incluso el “[!UICONTROL grupo de informes]” al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.

## Después de la implementación {#after-implementation}

Después de implementar [!DNL Analytics] en un sitio, puede encontrar el [!DNL tracking server] y el [!DNL report suite ID] en la baliza de seguimiento. El [!DNL tracking server] es el nombre del servidor en la baliza, por lo que es fácil encontrarlo. Los ID del [!UICONTROL grupo de informes] son una lista separada por comas justo después de “/b/ss/” en el nombre de ruta de la baliza.

Para ver la baliza, así como toda otra información que llegue a [!DNL Analytics] y a otras soluciones de Experience Cloud, instale la extensión de Chrome [Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=es).

## Antes de la implementación {#before-implementation}

**[!DNL Tracking Server]**: Si todavía no ha comenzado la implementación de Adobe Analytics, elegirá un subdominio para el [!DNL tracking server] de “.sc.omtrdc.net”. Por ejemplo, supongamos que tengo una tienda de sombreros en línea llamada Jim’s Brims. Puedo simplemente configurar mi [!DNL tracking server] en:

“jimsbrims.sc.omtrdc.net”.

**[!UICONTROL Grupo de informes]**: Para encontrar una lista de los [!UICONTROL grupos de informes] que se han creado, inicie sesión en [!DNL Analytics] y vaya a [!UICONTROL Administración] > [!UICONTROL Grupos de informes] en el menú superior para ver una lista de los [!UICONTROL grupos de informes], incluidos su ID y título.

Consulte el siguiente vídeo para obtener más información.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
