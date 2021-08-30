---
title: Uso de una capa de datos para establecer el nombre de página y otras variables en Adobe Analytics mediante Launch
description: Se considera una práctica recomendada el uso de una capa de datos para Analytics y otras soluciones de Experience Cloud. En este vídeo, verá cómo extraer los valores de la capa de datos y utilizarlos en Launch para rellenar variables en Adobe Analytics.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 7%

---

# Uso de una capa de datos para establecer el nombre de la página y otras variables mediante [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

El uso de una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud se considera una práctica recomendada. En este vídeo, verá cómo extraer los valores de la capa de datos y utilizarlos en [!DNL Experience Platform Launch] para rellenar variables en Adobe Analytics.

## Capas de datos {#data-layers}

Se recomienda utilizar una capa de datos cuando se trabaja con datos en el sitio y en las soluciones de Adobe Experience Cloud, especialmente con Adobe Analytics. Una _capa de datos_ es un marco de objetos JavaScript que los desarrolladores insertan en las páginas. Las herramientas de seguimiento (incluidos los sistemas de administración de etiquetas como [!DNL Experience Platform Launch]) pueden usar las capas de datos para rellenar los informes. Encontrará información adicional sobre las capas de datos en la [documentación del Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en) o en el [sitio W3C](https://www.w3.org/).

Además, consulte el blog [Capas de datos: De palabra de moda a práctica recomendada,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), que le proporciona información buena sobre las capas de datos, así como un par de ejemplos.

## Capas de datos, [!DNL Experience Platform Launch] y Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Cree un estándar de capa de datos para usar en el sitio, al que [!DNL Experience Platform Launch] puede hacer referencia.

   1. Coloque esta capa de datos lo más alto posible en el encabezado de la página, antes de la llamada a [!DNL Experience Platform Launch], de modo que [!DNL Launch] pueda usar los valores inmediatamente y las soluciones de Adobe que deben estar en la página, como Adobe Target.

1. Rellene los datos en la capa de datos.
1. En [!DNL Experience Platform Launch], cree &quot;[!UICONTROL elementos de datos]&quot; que hagan referencia a los puntos de datos en la capa de datos y que puedan utilizarse en [!DNL Experience Platform Launch] en [!UICONTROL reglas], [!UICONTROL extensiones], etc.
1. Utilice los [!UICONTROL elementos de datos] en las variables globales de la [!DNL Analytics] extensión o en una regla, asignando los valores a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] u otras variables [!DNL Analytics].
1. Déclencheur una señalización que envía los datos a [!DNL Analytics].

El siguiente vídeo lo acompaña durante el proceso.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
