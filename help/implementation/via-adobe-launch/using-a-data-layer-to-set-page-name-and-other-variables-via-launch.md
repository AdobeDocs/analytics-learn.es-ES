---
title: Uso de una capa de datos para establecer el nombre de la página y otras variables en Adobe Analytics mediante Launch
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
workflow-type: ht
source-wordcount: '365'
ht-degree: 100%

---

# Uso de una capa de datos para establecer el nombre de la página y otras variables mediante [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Se considera una práctica recomendada el uso de una capa de datos para [!DNL Analytics] y otras soluciones de Experience Cloud. En este vídeo, verá cómo extraer sus valores de la capa de datos y utilizarlos en [!DNL Experience Platform Launch] para rellenar variables en Adobe Analytics.

## Capas de datos {#data-layers}

Una práctica recomendada es utilizar una capa de datos cuando se trabaja con datos en el sitio y en las soluciones de Adobe Experience Cloud, especialmente con Adobe Analytics. Una _capa de datos_ es un marco de objetos JavaScript que los desarrolladores insertan en las páginas. Las herramientas de seguimiento (incluidos los sistemas de administración de etiquetas como [!DNL Experience Platform Launch]) pueden utilizar las capas de datos para rellenar informes. Busque información adicional acerca de las capas de datos en la [documentación de Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=es) o en el [sitio W3C](https://www.w3.org/).

Además, consulte la entrada de blog [Capas de datos: de palabra de moda a práctica recomendada](https://theblog.adobe.com/data-layers-buzzword-best-practice/), que proporciona información interesante sobre las capas de datos y un par de ejemplos.

## Capas de datos, [!DNL Experience Platform Launch] y Adobe Analytics {#data-layers-launch-and-adobe-analytics-oh-my}

1. Cree un estándar de capa de datos para usar en el sitio, al que se pueda hacer referencia mediante [!DNL Experience Platform Launch].

   1. Coloque esta capa de datos lo más alto posible en el encabezado de la página, antes de la llamada a [!DNL Experience Platform Launch], de modo que los valores se puedan usar inmediatamente por parte de [!DNL Launch], y por soluciones de Adobe que deben estar arriba en la página, como Adobe Target.

1. Rellene los datos en la capa de datos.
1. En [!DNL Experience Platform Launch], cree [!UICONTROL elementos de datos] que hagan referencia a los puntos de datos de la capa de datos y que puedan utilizarse en [!DNL Experience Platform Launch] en [!UICONTROL reglas], [!UICONTROL extensiones], etc.
1. Utilice la variable [!UICONTROL elementos de datos] en las variables globales de la extensión de [!DNL Analytics] o en una regla, y asigne los valores a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] u otras variables de [!DNL Analytics].
1. Active una baliza que envíe los datos a [!DNL Analytics].

El siguiente vídeo le muestra el proceso.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
