---
title: Cómo identificar el servidor de seguimiento y el ID del grupo de informes de Analytics
description: Al configurar Adobe Analytics o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el "servidor de seguimiento" de Analytics que está utilizando o incluso el "grupo de informes" al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 42bf16df9585d1f41206b81bf509a72c10f1d7f2
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 18%

---

# Cómo identificar el análisis [!DNL tracking server] y [!UICONTROL ID del grupo de informes] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Al configurar Adobe Analytics o al hacer referencia a él en otras soluciones de Experience Cloud, a menudo resulta útil o incluso necesario conocer el &quot;servidor de seguimiento&quot; de Analytics que está utilizando, o incluso el &quot;[!UICONTROL grupo de informes]&quot; al que está enviando datos. Este vídeo muestra cómo localizar ambos valores, haya implementado o no Adobe Analytics.

>[!IMPORTANT]
>
>Este artículo y vídeo se aplican a una implementación de &quot;AppMeasurement&quot; de Adobe Analytics y no a una implementación que utiliza el SDK web.

## Después de la implementación {#after-implementation}

Después de implementar Analytics en un sitio, puede encontrar lo siguiente [!DNL tracking server] y el [!DNL report suite ID] directamente en la señalización de seguimiento de. El [!DNL tracking server] es el nombre del host en la baliza, por lo que es fácil encontrarlo. El [!UICONTROL grupo de informes] Los ID son una lista separada por comas justo después de &quot;/b/ss/&quot; en el nombre de ruta de la señalización.

Para ver la baliza, así como toda otra información que llegue a Analytics y a otras soluciones de Experience Cloud, instale [Extensión de Chrome &quot;Experience Cloud Debugger&quot;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=es).

## Antes de la implementación {#before-implementation}

**[!DNL Tracking server]** : Si aún no ha comenzado la implementación de Adobe Analytics, elegirá un subdominio para el de &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Por ejemplo, supongamos que tengo una tienda de sombreros en línea llamada Jim&#39;s Brims. Puedo simplemente configurar mi [!DNL tracking server] en:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Grupo de informes]** - Para encontrar una lista de sus [!UICONTROL grupos de informes] que se han creado, inicie sesión en [!DNL Analytics] y vaya a [!UICONTROL Administrador] > [!UICONTROL Grupos de informes] en el menú superior para ver una lista de [!UICONTROL grupos de informes], incluidos su ID y título.

Consulte el siguiente vídeo para obtener más información.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
