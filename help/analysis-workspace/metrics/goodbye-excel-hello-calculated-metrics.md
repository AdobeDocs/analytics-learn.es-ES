---
title: Adiós Excel, saludar métricas calculadas
description: Descubra las ventajas de utilizar métricas calculadas en Adobe Analytics y cómo pueden proporcionarle una vista dinámica y continua de sus datos en este artículo.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
source-git-commit: 28db96c38e5318942ddc9f39ec0a2d561e14200c
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---


# Adiós Excel, saludar métricas calculadas

Descubra las ventajas de utilizar métricas calculadas en Adobe Analytics y cómo pueden proporcionarle una vista dinámica y continua de sus datos en este artículo.

¡Oye! ¿Por qué estás en Excel ahora mismo? Quiero decir, sé por qué. Tienes que informar para llegar a la gente correcta. Está ocupado introduciendo datos de Adobe Analytics y calculando tasas de conversión, trazándolos y preparándolos para colocarlos todos en un PowerPoint que se dirija a quienes toman decisiones. Espero que al menos esté utilizando Report Builder para hacerlo, pero sé que algunos de ustedes están copiando y pegando manualmente datos de un Workspace a Excel.

¿Por qué?

¿Por qué pasar por un proceso manual cada mes? ¿Por qué presentar una vista estática una vez al mes en lugar de una vista dinámica continua? ¿Por qué copiarlo en PowerPoint? ¿Por qué no crear métricas calculadas directamente en Adobe Analytics?

## Las métricas calculadas son potentes

Las métricas calculadas son potentes, pero incluso las funciones matemáticas básicas son una mejora muy útil y seria en comparación con hacer las matemáticas en Excel. Veamos algunos de los beneficios y algunos casos de uso:

1. **Las métricas calculadas son actuales y dinámicas**

   Al exportar números desde Adobe Analytics, se bloquean en un momento dado. Es absolutamente necesario que conozca el rendimiento de su sitio o aplicación el mes anterior, pero ¿cómo hacen los responsables de la toma de decisiones para realizar un seguimiento de cómo van las cosas a mediados de mes? Si la tasa de conversión se desploma durante un día y luego vuelve a la media antes de fin de mes, ¿lo sabe? Esa caída podría ser datos valiosos que revelen un problema importante de telemetría, o incluso más vital, un cambio en el comportamiento de los visitantes. Con una métrica calculada, puede graficarla y verla el día en que se produzca, lo que le permite responder.

1. **Las Métricas calculadas le ahorran tiempo**

   He estado allí. Copiar/pegar. Introduzca la fórmula o arrastre abajo la celda que se encuentra encima. Haga clic en el gráfico y cambie el intervalo para que tenga los últimos doce o trece meses. Ahora copie el gráfico. Ahora hágalo de nuevo. Y de nuevo. Y de nuevo. Envíe PowerPoint. Es tedioso y consume mucho tiempo y se siente como si tuvieras que hacerlo cada mes para siempre.

   En su lugar, puede crear un espacio de trabajo que utilice su métrica calculada, tenga los últimos doce o trece meses completos como intervalo de fechas, y hacer que los datos y el gráfico se actualicen automáticamente al trazo de la medianoche del primer día de cada mes. Los destinatarios pueden tener acceso directo al espacio de trabajo. Pueden tener una copia del PDF que se les envíe automáticamente por correo electrónico el primer día del mes o después de usar las visualizaciones de texto para agregar su comentario sobre los datos (ya sabe, la parte divertida de los informes).

1. **Las métricas calculadas se pueden aplicar a grandes conjuntos de datos**

   Puede exportar todos los nombres de producto a Excel y empezar a calcular las tasas de conversión y los ingresos por visitante, pero esto supone un problema cuando tiene aproximadamente 100.000. No es un problema con las métricas calculadas. Coloque la dimensión en una tabla de la forma habitual y, a continuación, utilice las métricas calculadas como métricas. Ahora tiene una tabla ordenable dinámica que se actualizará automáticamente cuando los productos o cualquier dimensión que esté utilizando se agreguen a su catálogo.

1. **Métricas calculadas para evitar errores**

   Se producen errores de Excel. Todos hemos estado allí. Caramba, toda la economía de Grecia y la reputación de dos estimados académicos fueron arruinadas debido a un error de fórmula de Excel. Probablemente no tengan una economía europea basada en sus habilidades con Excel, pero definitivamente hay alguna decisión sobre presupuestos que van a cambiar según sus números. El uso de métricas calculadas significa que puede crear una métrica, hacer que sea un control de calidad y luego no preocuparse por ella de nuevo.

### Ahora que hemos pasado por los beneficios de usar métricas calculadas, veamos cómo podemos ponerlas en práctica

**Caso de uso 1 : Tasas de conversión**

La mayoría de las tasas de conversión son solo divisiones simples. Divida el número de conversiones por el número de visitantes o visitas. Divida el número de vistas de página de la última página de un canal según el número de vistas de páginas de la primera página de un canal. Divida el número de pulsaciones de campaña internas por el número de impresiones. Todo esto se puede hacer fácilmente como métricas calculadas y colocarse en un tablero que tenga una baja latencia de datos, actualizaciones de visualizaciones y buena facilidad de uso compartido.

**Caso de uso 2: Búsqueda interna**

La búsqueda interna es una de las herramientas más importantes para comprender el sitio. Los resultados de la búsqueda del sitio indican en qué están interesados los visitantes y si pueden encontrarlo fácilmente a través de la navegación o no. Debe poder saber si la búsqueda de su sitio está funcionando bien y usar un poco de adición y división básica puede darle esa respuesta.

Empecemos con los resultados de búsqueda. Desea saber si un término de búsqueda obtiene resultados o no aparece nada. Normalmente son eventos separados. ¿Desea pasar por los problemas de obtener un tercer evento para todas las búsquedas internas del sitio agregadas? En su lugar, dé un descanso a los desarrolladores y utilice Métricas calculadas para agregar la búsqueda interna: Resultados y búsqueda interna: Sin resultados juntos para obtener búsquedas internas totales.

¿Qué porcentaje de búsquedas no arroja ningún resultado? Dividir búsqueda interna: Sin resultados por esa nueva métrica calculada de búsquedas internas totales. Ahora sabe si es urgente crear contenido nuevo que coincida con esos términos de búsqueda, o si tal vez su equipo de contenido puede abordar prioridades más altas.

Queremos saber cuántas de esas búsquedas con resultados obtienen pulsaciones y, por lo general, también tienen una métrica separada para ello. Utilice las métricas calculadas para dividir el número de pulsaciones por el número de veces que ese término trajo resultados de búsqueda y mostrarlos como un porcentaje. Ahora tiene la tasa de pulsaciones para cada término de búsqueda interna del sitio. Puede aislar los términos de búsqueda que muestran resultados no útiles. Tiene todos los datos históricos a su disposición para que los pueda graficar, y a medida que realice mejoras, puede ver fácilmente si están funcionando viendo que esa tasa aumenta o baja.

Divida el número de búsquedas internas por el número de visitantes que realizan búsquedas. Hay búsquedas por visitante para cada término. Si ese número es alto (cuanto más cerca esté a 1,0 mejor), tiene uno de dos problemas posibles. Los resultados en los que se hace clic son malos y los visitantes realizan varias búsquedas para encontrar los mejores resultados, o bien no encuentran las páginas que buscan a través de la navegación.

¿Cómo se puede medir si esas páginas clave son accesibles a través de la navegación? Cree una métrica calculada para vistas de página que siga a una vista de página de resultados de búsqueda. Divida esto por el total de vistas de página para esa página. Ahora sabe el porcentaje de vistas de página que provienen de los resultados de búsqueda. Si tiene un alto porcentaje, probablemente tenga algo de trabajo que hacer en la navegación.

### Las Métricas Calculadas Son Potentes

Espero que esto les haya mostrado algunas de las posibilidades de usar funciones matemáticas básicas en Métricas calculadas y que usted mismo empiece a crear algunas. Esto solo comienza a describir las posibilidades de las matemáticas que se pueden hacer en Métricas calculadas, incluso con cuatro funciones simples. Las métricas calculadas pueden ayudarle a comprender el comportamiento de los visitantes en un nivel completamente nuevo y, una vez que lo haya colgado, ha abierto la puerta para utilizar funciones más complejas que también están disponibles para usted.

## Autor

Este documento fue escrito por:

![Captura de pantalla de Gittai](assets/gittai.png)

**Gitai Ben-Ammi**, Consultor principal en Concentrix Catalyst

Campeona de Adobe Analytics
