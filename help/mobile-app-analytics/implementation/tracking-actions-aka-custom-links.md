---
title: Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform
description: 'Las acciones son eventos que se producen en la aplicación móvil. En este vídeo, aprenda a utilizar la API trackAction para rastrear y medir una acción. '
feature: mobile sdk
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
translation-type: tm+mt
source-git-commit: a42658cfd4bae7b077ddd48b4cf5c7db54e35c98
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Las acciones son eventos que se producen en la aplicación móvil. En este vídeo, aprenda a utilizar la API trackAction para rastrear y medir una acción.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Ésta es la API que debe utilizar para rastrear todas las acciones que no sean de carga de pantalla del sitio. Si aparece la pantalla, utilice trackState, que activa una visita de vista de página. De lo contrario, utilice trackAction para enviar variables asociadas con la acción que se está llevando a cabo.

Estos datos se incluyen como `contextData`, lo que también significa que deberá utilizar las reglas [!UICONTROL de] procesamiento para tomar los datos móviles de esas `contextData` variables y asignarlos a [!DNL eVars], [!DNL Props], Eventos, etc. en Adobe Analytics.

Para obtener más información sobre trackAction, consulte la [documentación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
