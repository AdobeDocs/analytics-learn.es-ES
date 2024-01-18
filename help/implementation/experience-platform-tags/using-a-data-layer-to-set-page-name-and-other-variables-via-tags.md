---
title: Uso de una capa de datos para establecer variables de Analytics en Experience Platform [!DNL tags]
description: Aprenda a utilizar una capa de datos para obtener datos de Analytics y otras soluciones de Experience Cloud.
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: a45667a8d7ccb46b9e33bd11a78fac9714a61df5
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 50%

---

# Uso de una capa de datos para establecer variables de Analytics en Experience Platform [!DNL tags]

Se considera una práctica recomendada el uso de una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud. En este vídeo, aprenderá a extraer valores de la capa de datos y utilizarlos en Experience Platform [!DNL tags] para rellenar variables en Adobe Analytics.

## Capas de datos

Una _capa de datos_ es un marco de objetos JavaScript que los desarrolladores insertan en páginas web digitales. Básicamente, las soluciones de Analytics utilizan la capa de datos para rellenar informes. Sistemas de administración de etiquetas, incluido el Experience Platform [!DNL tags]) son los intermediarios que leen la capa de datos, asignan los valores a variables y envían esos datos a las soluciones de experiencia digital.

Consulte información adicional sobre las capas de datos en la [Documentación del Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=es).

## Capas de datos, Experience Platform [!DNL tags], y ADOBE ANALYTICS

1. Defina o identifique un estándar de capa de datos para usar en su sitio.

   1. Coloque la capa de datos lo más alto posible en la sección del encabezado de la página, antes de la llamada al Experience Platform [!DNL tags]. Esto garantiza que [!DNL tags] y otras soluciones de Adobe que necesitan estar en la parte superior de la página, como Adobe Target, accedan inmediatamente a estos valores.

1. Rellene los datos en la capa de datos.
1. En Experience Platform [!DNL tags], crear &quot;[!UICONTROL elementos de datos]&quot; que asignan los puntos de datos en la capa de datos. Estos elementos de datos se utilizan en Experience Platform [!DNL tags] in [!UICONTROL reglas] y [!UICONTROL extensiones].
1. En la sección de variables globales de la extensión [!DNL Analytics] o en [!DNL Tags rule], asigne los valores de [!UICONTROL elementos de datos] a [!UICONTROL Props], [!UICONTROL eVars], [!UICONTROL pageName] y otras variables de [!DNL Analytics].
1. Active una baliza que envíe los datos a [!DNL Analytics].

El siguiente vídeo le muestra el proceso.

>[!NOTE]
>
> El lanzamiento es ahora **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>Es posible que la capa de datos específica utilizada en este vídeo no se considere una práctica recomendada para su organización. La práctica recomendada es utilizar una capa de datos para enviar datos importantes a las soluciones de marketing digital.
