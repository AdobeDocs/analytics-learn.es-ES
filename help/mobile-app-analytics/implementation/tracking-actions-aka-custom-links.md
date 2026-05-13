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
role: Developer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
TQID: https://experienceleague.adobe.com/msvft7mQiNGjLqGEezPIbwruvSbsunPGUIFF1q7vlT0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 73%

---

# Seguimiento de acciones (también conocidos como vínculos personalizados) en una aplicación móvil con el SDK de Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Las acciones son eventos que se producen en la aplicación móvil. En este vídeo aprenderá a utilizar la API trackAction para rastrear y medir una acción.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12&learn=on)

Utilice esta API para rastrear todas las acciones que no sean de carga de pantalla del sitio. Si la pantalla aparece, utilice trackState, que desencadena una visita de vista de página. De lo contrario, utilice trackAction para enviar variables asociadas con la acción que se está llevando a cabo.

Estos datos se incluyen como `contextData`, lo que también significa que tendrá que usar [!UICONTROL Reglas de procesamiento] para tomar los datos móviles de esas `contextData` variables y asignarlos a [!DNL eVars], [!DNL Props], Eventos, etc. en Adobe Analytics.

Para obtener más información sobre trackAction, consulte la [documentación](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
