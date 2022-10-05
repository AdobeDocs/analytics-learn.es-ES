---
title: Usar una capa de datos para establecer variables de Analytics mediante Etiquetas
description: Obtenga información sobre el uso de una capa de datos para obtener datos de Analytics y otras soluciones de Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 9%

---

# Usar una capa de datos para establecer variables de Analytics mediante [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Uso de una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud es una práctica recomendada. En este vídeo, aprenderá a extraer valores de la capa de datos y utilizarlos en [!DNL Experience Platform Tags] para rellenar variables en Adobe Analytics.

## Capas de datos {#data-layers}

A _capa de datos_ es un marco de objetos JavaScript que los desarrolladores agregan a las páginas web digitales. Las soluciones de Analytics utilizan finalmente la capa de datos para rellenar informes. Sistemas de gestión de etiquetas, incluidos [!DNL Experience Platform Tags]) son los intermediarios que leen la capa de datos, asignan los valores a variables y envían esos datos a soluciones de experiencia digital.

Revise información adicional sobre las capas de datos en la [documentación del Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=es) y el blog [Capas de datos: De palabra de moda a práctica recomendada](https://blog.adobe.com/en/2014/03/13/data-layers-buzzword-best-practice).

## Capas de datos, [!DNL Experience Platform Tags]y Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Defina o identifique un estándar de capa de datos para usar en el sitio.

   1. Coloque la capa de datos lo más alto posible en la sección del encabezado de la página y antes de la llamada a [!DNL Experience Platform Tags]. Esto garantiza que se acceda a los valores inmediatamente mediante [!DNL Tags] y por soluciones de Adobe que necesitan estar en primer plano en la página, como Adobe Target.

1. Rellene los datos en la capa de datos.
1. En [!DNL Experience Platform Tags], crear &quot;[!UICONTROL elementos de datos]&quot; que asignan los puntos de datos de la capa de datos. Estos elementos de datos se utilizan en todas las [!DNL Experience Platform Tags] en [!UICONTROL reglas] y [!UICONTROL extensiones].
1. En [!DNL Analytics] variables globales de la extensión o en una [!DNL Tags rule], asigne los valores de [!UICONTROL elementos de datos] a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]y otros [!DNL Analytics] variables.
1. Active una baliza que envíe los datos a [!DNL Analytics].

El siguiente vídeo le muestra el proceso.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)

>[!NOTE]
>
>Es posible que la capa de datos específica utilizada en este vídeo no se considere una &quot;práctica recomendada&quot; para su organización. Se recomienda utilizar una capa de datos para enviar datos importantes a las soluciones de marketing digital.