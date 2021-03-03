---
title: Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform
description: 'Las acciones son eventos que se producen en su aplicación móvil. En este vídeo, aprenderá a utilizar la API trackAction para realizar el seguimiento y medir una acción. '
feature: SDK móvil
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: '"Desarrollador, ingeniero de datos"'
level: Con experiencia
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Las acciones son eventos que se producen en su aplicación móvil. En este vídeo, aprenderá a utilizar la API trackAction para realizar el seguimiento y medir una acción.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Esta es la API que debe utilizar para rastrear todas las acciones que no sean de carga de pantalla en el sitio. Si aparece la pantalla, utilice trackState, que activa una visita de vista de página. De lo contrario, utilice trackAction para enviar variables asociadas con la acción que se está realizando.

Estos datos aparecen como `contextData`, lo que también significa que tendrá que utilizar [!UICONTROL Reglas de procesamiento] para tomar los datos móviles de esas `contextData` variables y asignarlos a [!DNL eVars], [!DNL Props], eventos, etc. en Adobe Analytics.

Para obtener más información sobre trackAction, consulte la [documentación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
