---
title: Utilice el análisis de cohorte para comprender el comportamiento del cliente
description: Para mejorar la experiencia y los ingresos de los clientes, las empresas deben comprender el comportamiento de los clientes. El análisis de cohorte puede ayudar a comprender la participación y la retención, lo que conduce a acciones como mejorar la creación de cuentas y crear campañas para meses de gran volumen.
feature: Cohort Analysis
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13213
thumbnail: KT-13213.jpeg
source-git-commit: 5988e9d68f0c2200168da56373259bdf9f4f901b
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 17%

---


# Utilice el análisis de cohorte para comprender el comportamiento del cliente

Para mejorar la experiencia y los ingresos de los clientes, las empresas deben comprender el comportamiento de los clientes. El análisis de cohorte puede ayudar a comprender la participación y la retención, lo que conduce a acciones como mejorar la creación de cuentas y crear campañas para meses de gran volumen.

El análisis del rendimiento digital es crucial para comprender cómo interactúan los clientes con una empresa y qué acciones se pueden llevar a cabo para mejorar su experiencia. En esta entrada de blog, exploraremos cómo utilizar el análisis de cohorte para comprender mejor el comportamiento de los clientes.

## Parte 1: Comparación del rendimiento digital entre visitas de primera y de retorno

### Configuración del escenario

Un cliente busca comprender el rendimiento digital en los últimos 2 años y está considerando desarrollar un programa de fidelidad para impulsar el rendimiento digital. Para empezar, podemos observar la combinación actual del sitio entre usuarios nuevos y repetidos para comprender cómo se comportan hoy los dos grupos de visitantes.

Rendimiento digital actual

1. En 2022, el 62% de los pedidos provenían de visitas por primera vez, en comparación con el 38% de los pedidos de visitas de retorno (sujetos a cookies, múltiples dispositivos).
1. Las visitas por primera vez se convierten a una tasa ligeramente más alta que las visitas de retorno para ambas, un 11,6% vs. un 11,4%.
1. En comparación con 2021, las tasas de conversión se redujeron en ambos segmentos.

![Tabla de visitas](assets/visits-table.png)

## Parte 2: Análisis de cohorte: Visitas: Disposiciones Comestibles, Producto Global

Para comprender la permanencia del canal digital y la oportunidad de impulsar a los compradores repetidos, la siguiente pregunta a responder es: ¿Cuál es el volumen de visitantes que regresan al sitio cada mes en 2022?

### Presentación del análisis de cohorte

El análisis de cohorte es una herramienta útil para comprender cómo las cohortes interactúan con una marca a lo largo del tiempo. Para empezar, determinamos qué preguntas responder:

1. En un año determinado, ¿cuál es el período de retención promedio por mes?
1. ¿Qué volumen de visitantes al sitio regresan cada mes en un año determinado?
1. ¿Cuál es el impacto de los inicios de sesión en la retención?
1. ¿Existen productos específicos que conduzcan a una mayor retención?

Configuración de la tabla de cohorte

1. Establecer intervalo de fechas de enero a diciembre de 2022
1. **Criterios de inclusión:** Visitas
1. **Criterios de devolución:** Visitas
1. **Granularidad:** Mes
1. **Configuración:** Cálculo móvil \*\*Permite calcular la retención en función de la columna anterior, no de la columna incluida. Por lo tanto, esto significa que un usuario se incluye en cada uno de los meses\*\*
1. **Segmentos:** puede seleccionar segmentos específicos para profundizar este análisis
   1. Páginas de aterrizaje específicas
   1. Tipo de dispositivo
   1. Canales de marketing
   1. Etc.

### Interpretación de los resultados

**En 2022:**

1) Los meses con tasas de retención más altas +1 mes incluyen enero, abril y noviembre
1) Los meses con el mayor volumen incluyen febrero y mayo
1) Hay cerca de 1000 visitantes que regresan al sitio cada mes

![Tabla de retención de 2022](assets/2022-retention-table.png)

**En 2021:**

1) Los meses con tasas de retención más altas +1 mes incluyen abril, enero y marzo
1) Los meses con el mayor volumen incluyen febrero y mayo

![Tabla de retención de 2021](assets/2021-retention-table.png)

**Elementos de acción:**

Cree un segmento basado en los ~1000 visitantes y obtenga más información sobre ellos:

- ¿Dónde están ubicados?
- ¿Qué productos compran a lo largo del año?
- ¿De qué tiendas están comprando?

Los meses clave resaltan la oportunidad de impulsar la retención en función del volumen:

- ¿Existen tácticas específicas que puedan impulsar una mayor permanencia durante febrero y mayo para aprovechar el volumen?

Repetir análisis para que los pedidos comprendan el proceso de compra

- ¿Son las tasas de retención más altas de +1 mes para los mismos meses?
- ¿Los meses más altos de Visitas son los mismos para los pedidos?

## Parte 3: Adición de dos métricas a los criterios de inclusión

### Comprensión del impacto del inicio de sesión

Dado que este cliente busca comprender el valor de un programa de Lealtad, el siguiente paso del análisis incluyó la adición del evento de éxito de inicio de sesión como métrica de inclusión a la cohorte.

Advertencia: El análisis de cohorte no se puede usar para métricas calculadas (como Tasa de conversión) ni para métricas que no sean números enteros (como Ingresos). Solo se pueden usar las métricas de los segmentos en Análisis de cohorte y solo se pueden incrementar en >1 a la vez.

¿Es más probable que el sitio conserve a los usuarios que inician sesión?

¿Cuál sería el impacto si pudiéramos hacer que más usuarios iniciaran sesión? ¿Es una experiencia más difícil?

### Configuración de la tabla de cohorte

1. **Definir intervalo de fechas:** de enero a diciembre de 2022
1. **Criterios de inclusión:** Visitas + Evento de éxito de inicio de sesión
1. **Criterios de devolución:** Visitas
1. **Granularidad:** Mes
1. **Configuración:** Cálculo móvil \*\*Permite calcular la retención en función de la columna anterior, no de la columna incluida. Por lo tanto, esto significa que un usuario se incluye en cada uno de los meses\*\*

### Interpretación de los resultados

**En 2022:**

1) Los meses con tasas de retención más altas +1 mes incluyen enero, abril y noviembre (los mismos meses que la primera tabla de cohorte)
1) Los meses con el mayor volumen incluyen febrero y mayo y diciembre
1) Hay ~2500 visitantes que regresan cada mes \*\*más de dos veces\*\*

**Elementos de acción:**

Investigar la experiencia del usuario del sitio para que los usuarios creen una cuenta durante el cierre de compra

![Tabla de cohorte 4](assets/cohort-table-4.png)

## Parte 4: Cohorte de Dimension personalizada

Cohorte de dimensión personalizada: cree cohortes basadas en la dimensión seleccionada, no en el tiempo (valor predeterminado). Muchos clientes desean analizar sus cohortes en función de un criterio distinto del tiempo. La nueva función de cohorte de dimensión personalizada ofrece la flexibilidad para generar cohortes basadas en dimensiones de su elección. Utilice dimensiones como canal de marketing, campaña, producto, página, región o cualquier otra dimensión de Adobe Analytics para mostrar cómo cambia la retención en función de los distintos valores que adoptan. La variable 

La definición de segmento de cohorte de Dimension personalizado aplica el elemento de dimensión solo como parte del periodo de inclusión, no como parte de la definición de devolución.

Después de elegir la opción Cohorte de dimensión personalizada, puede arrastrar y soltar cualquier dimensión que desee en la zona de colocación. De este modo puede comparar elementos de dimensión similares durante el mismo periodo de tiempo. Por ejemplo, puede comparar el rendimiento de las ciudades una al lado de la otra

del lado, productos, campañas, etc. Devuelve sus 14 elementos de dimensión principales. Sin embargo, puede utilizar un filtro (al que se accede manteniendo el puntero a la derecha de la dimensión que ha arrastrado) para que solo se muestren los elementos de dimensión que desee. No es posible utilizar una cohorte de dimensión personalizada junto a la función de tablas de latencia.

### ¿Qué productos están impulsando la permanencia del sitio?

La tabla Cohorte de Dimension personalizado resalta los productos que generan tasas de retención más altas que la media.  Esta tabla ayuda a identificar los productos principales para impulsar campañas de marketing internas y externas que incluyan productos de mayor relevancia.

**En febrero:** 3 productos destacan con mayores tasas de retención

1) Product 1
1) Product 2
1) Product 3

**En Mar:**

1) Product 1
1) Product 2
1) Product 3 con frecuencia supera el rendimiento con una tasa de retención mayor que la retención media.

![Tabla de cohorte 5](assets/cohort-table-5.png)

## Conclusión

El análisis de cohorte y la cohorte de Dimension personalizado son poderosas herramientas para comprender el comportamiento del cliente y mejorar el rendimiento digital. Al analizar las tasas de retención, las tasas de inicio de sesión y el impacto de productos específicos, las empresas pueden tomar decisiones basadas en datos para mejorar la experiencia del cliente e impulsar el crecimiento.

## Autor

Este documento fue escrito por:

![Jennifer Yacenda](assets/jennifer-yacenda.png)

**Jennifer Yacenda**, Director Senior en Marriott

Campeona de Adobe Analytics