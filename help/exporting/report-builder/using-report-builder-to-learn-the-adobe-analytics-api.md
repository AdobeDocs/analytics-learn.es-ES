---
title: Uso de Report Builder para conocer la API de Adobe Analytics
description: Report Builder es algo que todos conocemos y amamos. ¿Y si les dijera que podrían usar lo que saben sobre el Report Builder para avanzar aún más en sus habilidades con Adobe Analytics? En este vídeo, explicaremos cómo realizar solicitudes de Report Builder de depuración y cómo utilizarlas para aprender a crear sus propias consultas de API de Analytics.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---

# Uso del [!UICONTROL Report Builder] para conocer la API de Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report ] Builder es algo que todos conocemos y amamos. ¿Y si le dijera que podría usar lo que sabe sobre [!UICONTROL Report Builder] para avanzar aún más en su conjunto de habilidades de Adobe Analytics? En este vídeo, explicaremos cómo realizar solicitudes de depuración [!UICONTROL Report Builder] y utilizarlas para aprender a crear sus propias consultas de API [!DNL Analytics].

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**ACTUALIZACIÓN**:  [!UICONTROL Report ] Builder actualizó el modo en que solicita los datos ligeramente. Puede seguir utilizando el enfoque de este vídeo, pero la información será ligeramente diferente en un depurador.

En un depurador:

1 - Busque api5.omniture.com. El número puede variar de 1 a 5 según el centro de datos.

2 - Vaya a la pestaña [!UICONTROL Request]

3 - Busque &#39;[!DNL Report.Queue]&#39; en la solicitud.

También hay un método alternativo para depurar solicitudes como esta, y funciona igual de bien. Puede activar el registro de [!UICONTROL Report Builder] desde el menú [!UICONTROL Options] y que registrará la misma información que lo haría un depurador. Los registros se encuentran en [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs] y se organizarán por día. Puede buscar en el archivo &#39;Report.Queue&#39; para encontrar cada una de sus solicitudes. Los registros también ayudan a solucionar cualquier problema.

Para obtener más información sobre esta función, visite la [documentación](https://www.adobe.io/).
