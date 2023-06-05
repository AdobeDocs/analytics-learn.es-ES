---
title: Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform
description: Las acciones son eventos que se producen en la aplicación móvil. En este vídeo aprenderá a utilizar la API trackAction para rastrear y medir una acción.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer, Data Engineer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
source-git-commit: 4d467928756950074620388645523021b21fb0d5
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 95%

---

# Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Las acciones son eventos que se producen en la aplicación móvil. En este vídeo aprenderá a utilizar la API trackAction para rastrear y medir una acción.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12&learn=on)

Utilice esta API para rastrear todas las acciones que no sean de carga de pantalla del sitio. Si la pantalla aparece, utilice trackState, que desencadena una visita de vista de página. De lo contrario, utilice trackAction para enviar variables asociadas con la acción que se está llevando a cabo.

Estos datos se incluyen como `contextData`, lo que también significa que deberá utilizar [!UICONTROL Reglas de procesamiento] para tomar los datos móviles de esas variables `contextData` y asignarlos a [!DNL eVars], [!DNL Props], Eventos, etc. en Adobe Analytics.

Para obtener más información sobre trackAction, consulte la [documentación](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
