---
title: Uso de Report Builder para conocer la API de Adobe Analytics
description: Report Builder es algo que todos conocemos y amamos. ¿Y si les dijera que podrían usar lo que saben sobre Report Builder para avanzar aún más en sus habilidades con Adobe Analytics? En este vídeo, explicaremos cómo realizar solicitudes de Report Builder de depuración y cómo utilizarlas para aprender a crear sus propias consultas de API de Analytics.
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
source-wordcount: '274'
ht-degree: 100%

---

# Uso de [!UICONTROL Report Builder] para conocer la API de Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report Builder] es algo que todos conocemos y amamos. ¿Y si les dijera que podrían usar lo que saben sobre [!UICONTROL Report Builder] para avanzar aún más en sus habilidades con Adobe Analytics? En este vídeo, explicaremos cómo realizar solicitudes de [!UICONTROL Report Builder] de depuración y utilizarlas para aprender a crear sus propias consultas de [!DNL Analytics] API.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**ACTUALIZACIÓN**: [!UICONTROL Report Builder] ha actualizado el modo en que solicita los datos ligeramente. Puede seguir utilizando el enfoque de este vídeo, pero la información será ligeramente diferente en un depurador.

En un depurador:

1 - Busque api5.omniture.com. El número puede variar de 1 a 5 según el centro de datos.

2 - Vaya a la pestaña [!UICONTROL Solicitud].

3 - Busque [!DNL Report.Queue] en la solicitud.

También hay un método alternativo para depurar solicitudes como esta, y funciona igual de bien. Puede activar el inicio de sesión de [!UICONTROL Report Builder] desde el menú [!UICONTROL Opciones] y se registrará la misma información que haría un depurador. Los registros se encuentran en [!UICONTROL Documentos] > [!UICONTROL ReportBuilderLogs] y se organizarán por día. Puede buscar en el archivo Report.Queue para encontrar cada una de sus solicitudes. Los registros también ayudan a solucionar cualquier problema.

Para obtener más información acerca de esta funcionalidad, visite la [documentación](https://www.adobe.io/).
