---
title: Uso de una capa de datos para establecer el nombre de la página y otras variables en Adobe Analytics mediante Launch
description: Se considera una práctica recomendada utilizar una capa de datos para Analytics y otras soluciones de Experience Cloud. En este vídeo, verá cómo extraer los valores de la capa de datos y utilizarlos en Launch para rellenar variables en Adobe Analytics.
feature: launch implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
translation-type: tm+mt
source-git-commit: ee6c03cff5b051d9293d75965e9fd98f151d7fce
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 4%

---


# Uso de una capa de datos para establecer el nombre de la página y otras variables mediante [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Se considera una práctica recomendada utilizar una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud. En este vídeo, verá cómo extraer los valores de la capa de datos y utilizarlos en [!DNL Experience Platform Launch] para rellenar variables en Adobe Analytics.

## Capas de datos {#data-layers}

Se recomienda utilizar una capa de datos cuando se trabaja con datos en el sitio y en las soluciones de Adobe Experience Cloud, especialmente con Adobe Analytics. Una _capa de datos_ es un marco de objetos JavaScript que los desarrolladores insertan en las páginas. The data layers can be used by tracking tools (including tag management systems like [!DNL Experience Platform Launch]) to populate reports. Busque información adicional sobre las capas de datos en la documentación [del](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) Experience Cloud o en el sitio [](https://www.w3.org/)W3C.

Además, consulte el blog Capas [de datos: De Buzzword a la Práctica recomendada,](https://theblog.adobe.com/data-layers-buzzword-best-practice/)que proporciona información buena sobre las capas de datos, así como un par de ejemplos.

## Capas de datos [!DNL Experience Platform Launch], y Adobe Analytics (oh mi?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Cree un estándar de capa de datos para utilizarlo en el sitio, al que se puede hacer referencia mediante [!DNL Experience Platform Launch].

   1. Coloque esta capa de datos lo más alto posible en el encabezado de la página, antes de la llamada a [!DNL Experience Platform Launch], de modo que los valores puedan ser utilizados inmediatamente por [!DNL Launch]las soluciones de Adobe que necesitan estar en la parte superior de la página, como Adobe Target.

1. Rellene los datos en la capa de datos.
1. En [!DNL Experience Platform Launch], cree &quot;elementos[!UICONTROL de]datos&quot; que hagan referencia a los puntos de datos en la capa de datos y que se puedan utilizar [!DNL Experience Platform Launch] en [!UICONTROL reglas], [!UICONTROL extensiones], etc.
1. Utilice los elementos [!UICONTROL de] datos en las variables globales de [!DNL Analytics] extensión o en una regla, asignando los valores a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]u otras [!DNL Analytics] variables.
1. Active una señalización que envíe los datos a [!DNL Analytics].

El siguiente vídeo lo acompaña durante todo el proceso.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
