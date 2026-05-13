---
title: Espere un segmento... Utilice la segmentación para descubrir nuevas perspectivas en Analysis Workspace
description: Aprenda a utilizar segmentos en Adobe Analytics para descubrir nuevas perspectivas desde las visualizaciones de Analysis Workspace y las tablas de forma libre.
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00.000Z
jira: KT-13268
thumbnail: KT-13268.jpeg
exl-id: 7743debd-57d8-4c79-a332-187180fc9701
TQID: https://experienceleague.adobe.com/SqW3fb-f-er2nTJ1FbayhC4MjiYvrU5iEj5UvzfHiqU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b0ca67c6-0a35-482c-ad91-baac1bcb26d6
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: a544b409-2610-410d-a842-474ac1d0d54e
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
  - id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 878
ht-degree: 7%

---

# Espere un segmento... Use segmentos para descubrir nuevas perspectivas en Analysis Workspace

Tanto si es un usuario nuevo de Adobe Analytics como si es un profesional experimentado, aprovechará bastante los segmentos en sus proyectos de Analysis Workspace. Como describe [Adobe Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=es), &quot;los segmentos le permiten identificar subconjuntos de visitantes basándose en sus características o en las interacciones con el sitio web&quot;. Aunque el resultado básico de esta función es aislar grupos de usuarios, visitas o visitas individuales a su sitio, un analista agudo como usted puede ser creativo con esta herramienta y encontrar nuevas formas de obtener información sobre la actividad del sitio. La lista de opciones posibles es amplia, así que no dude en crear la suya propia y compartirla con otros de su organización o en línea en comunidades como la [Comunidad de Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=es) en Experience League o la comunidad de [#Measure Slack](https://www.measure.chat/).

Si necesita un repaso rápido sobre cómo crear un segmento, consulte la documentación de Experience League sobre el uso de [Generador de segmentos](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=es) en Analysis Workspace.

## Comparación y contraste de segmentos

En Analysis Workspace puede comparar dos segmentos usando &quot;[Comparación de segmentos](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=es)&quot;. La comparación de segmentos se puede encontrar en la sección Paneles de la barra de navegación izquierda:

![Segs. 01](assets/seg01.png)

Sin embargo, a veces no necesita un panel de comparación completo para ofrecer perspectivas clave a los usuarios finales. Afortunadamente, algunas funciones también se pueden comparar en un panel estándar.

La [visualización de diagrama de Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=es) puede ayudar a crear una comparación rápida, permitiéndole pasar el ratón por encima y ver las sesiones, pedidos, usuarios, etc. superpuestos entre 2 y 3 segmentos personalizados. También puede generar segmentos rápidamente haciendo clic con el botón derecho en cualquiera de las secciones superpuestas:

![Segs. 02](assets/s02.png)

A veces, la información importante no se encuentra en los datos superpuestos, sino en los datos que no se superponen. Una forma rápida de ver esto es crear una copia de un segmento y convertirlo en un segmento de &quot;Exclusión&quot;:

![Segs. 03](assets/s03.png)

Al apilar el segmento de exclusión con el otro segmento de la comparación, ahora puede calcular rápidamente cuántas visitas llegan a la página del menú sin ver también la página de inicio en la misma sesión:

![Segs. 04](assets/s04.png)

## Ataque de pila

Del mismo modo, puede crear los datos de intersección de un diagrama de Venn simplemente apilando cualquier segmento. No hay límite en cuanto a la cantidad de segmentos o dimensiones individuales que se apilan. Por ejemplo, si quisiera averiguar rápidamente qué días de la semana del mes pasado mi sitio tuvo una visita en un teléfono móvil, específicamente un Samsung Galaxy A52, que sí vio mis páginas de menú y nutrición, pero NO vio mi página de inicio, puedo construirlo rápidamente sobre la marcha de esta manera:

![Segs. 05](assets/s05.png)

Pero aún mejor, una vez que encuentro ese subconjunto perfecto de mi base de usuarios o visitas, puedo seleccionar todos esos valores, hacer clic con el botón derecho y crear un segmento al instante:

![Segs. 06](assets/s06.png)

![Segs. 07](assets/s07.png)

![Segs. 08](assets/s08.png)

Eso es mucho poder en un segmento.

## Un segmento de números para una serie de segmentos

Muchos usuarios suelen observar los valores nominales, ordinales o de intervalo al crear segmentos, como una página visitada, un intervalo de edad de usuarios o el número de visitas que un usuario ha realizado en el pasado. Sin embargo, también puede utilizar datos de proporción al crear un segmento agrupando estos valores, ya sean dimensiones estándar, métricas estándar o variables y métricas personalizadas para su organización.

Por ejemplo, Tiempo empleado en la página o Tiempo empleado por visita tiene bloques creados previamente:

![Segs. 09](assets/s09.png)

Sin embargo, es posible que no siempre se ajusten a las necesidades de su organización; tal vez la mayoría de las visitas al sitio sean de menos de 10 minutos. Puede utilizar la medición granular para crear bloques de distinto tamaño. Este es un informe creado para observar las visitas que duran entre 1 minuto, 1 segundo y 1 minuto, 30 segundos:

![Segs. 10](assets/s10.png)

Una vez creada, ahora puedo empezar a ver mis visitas, pedidos y otros eventos por los diferentes grupos de tiempo agrupados que he personalizado:

![Seg. 11](assets/s11.png)

Incluso puede empezar a examinar cómo cambian los Indicadores clave de rendimiento (KPI) como factor de cuánto tiempo invierte un usuario, cuántas páginas visita en una visita, cuántas veces ha visitado en el pasado o cualquier otro valor numérico, lo que básicamente le permite ver una métrica como factor de otra métrica:

![Seg. 12](assets/s12.png)

Las posibilidades de usar segmentos para encontrar nuevas perspectivas son infinitas. Esto es simplemente un punto de partida. Pruebe algunas por su cuenta y haga saber a la comunidad lo que descubre: [Comunidad de Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=es) en Experience League o la comunidad de [#Measure Slack](https://www.measure.chat/).

¡Feliz segmentación!

## Autor

Este documento fue escrito por:

![Dan Cummings](assets/seg13.png)

**Dan Cummings**, ingeniero de productos senior en Analytics en McDonald&#39;s Corporation

Campeona de Adobe Analytics
