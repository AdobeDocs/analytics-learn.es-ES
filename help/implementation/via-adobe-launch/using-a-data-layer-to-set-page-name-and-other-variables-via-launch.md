---
title: Uso de una capa de datos para establecer variables de Analytics mediante etiquetas
description: Obtenga información sobre cómo usar una capa de datos para obtener datos de Analytics y otras soluciones de Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: 7224af1bd798d447f1b14c61e836f8e5c8af7ea4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 96%

---

# Uso de una capa de datos para establecer variables de Analytics mediante [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Se considera una práctica recomendada el uso de una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud. En este vídeo, aprenderá a extraer sus valores de la capa de datos y utilizarlos en [!DNL Experience Platform Tags] para rellenar variables en Adobe Analytics.

## Capas de datos {#data-layers}

Una _capa de datos_ es un marco de objetos JavaScript que los desarrolladores insertan en páginas web digitales. Básicamente, las soluciones de Analytics utilizan la capa de datos para rellenar informes. Los sistemas de administración de etiquetas, como [!DNL Experience Platform Tags], son los intermediarios que leen la capa de datos, asignan los valores a variables y envían esos datos a las soluciones de experiencia digital.

Consulte información adicional sobre las capas de datos en la [Documentación del Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=es).

## Capas de datos, [!DNL Experience Platform Tags] y Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Defina o identifique un estándar de capa de datos para usar en su sitio.

   1. Coloque la capa de datos lo más alto posible en la sección del encabezado de la página, antes de la llamada a [!DNL Experience Platform Tags]. Esto garantiza que [!DNL Tags] y otras soluciones de Adobe que necesitan estar en la parte superior de la página, como Adobe Target, accedan inmediatamente a estos valores.

1. Rellene los datos en la capa de datos.
1. En [!DNL Experience Platform Tags], cree &quot;[!UICONTROL elementos de datos]&quot; que asignen los puntos de datos de la capa de datos. Estos elementos de datos se utilizan en [!DNL Experience Platform Tags], en [!UICONTROL reglas] y [!UICONTROL extensiones].
1. En la sección de variables globales de la extensión [!DNL Analytics] o en [!DNL Tags rule], asigne los valores de [!UICONTROL elementos de datos] a [!UICONTROL Props], [!UICONTROL eVars], [!UICONTROL pageName] y otras variables de [!DNL Analytics].
1. Active una baliza que envíe los datos a [!DNL Analytics].

El siguiente vídeo le muestra el proceso.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>Es posible que la capa de datos específica utilizada en este vídeo no se considere una práctica recomendada para su organización. La práctica recomendada es utilizar una capa de datos para enviar datos importantes a las soluciones de marketing digital.