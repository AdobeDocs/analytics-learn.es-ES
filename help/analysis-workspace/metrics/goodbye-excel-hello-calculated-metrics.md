---
title: Adiós, Excel. Hola, métricas calculadas
description: Conozca las ventajas de utilizar métricas calculadas en Adobe Analytics y cómo pueden proporcionarle una vista dinámica y continua de sus datos en este artículo.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
exl-id: d4f69244-6614-41f3-ac48-70adabb8a8e7
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 2%

---

# Adiós, Excel. Hola, métricas calculadas

Conozca las ventajas de utilizar métricas calculadas en Adobe Analytics y cómo pueden proporcionarle una vista dinámica y continua de sus datos en este artículo.

¡Oye! ¿Por qué está en Excel en este momento? Quiero decir, sé por qué. Tienes que informar para llegar a las personas adecuadas. Está ocupado introduciendo datos de Adobe Analytics y calculando las tasas de conversión, creando gráficos y preparándose para colocarlos en un PowerPoint que se dirige a los responsables de la toma de decisiones. Espero que al menos esté usando Report Builder para hacerlo, pero sé que algunos de ustedes están copiando y pegando manualmente datos de un Workspace a Excel.

¿Por qué?

¿Por qué pasar por un proceso manual todos los meses? ¿Por qué presentar una vista estática una vez al mes en lugar de una vista dinámica y continua? ¿Por qué copiar eso en PowerPoint? ¿Por qué no crear Métricas calculadas directamente en Adobe Analytics?

## Las métricas calculadas son potentes

Las métricas calculadas son potentes, pero incluso las funciones matemáticas básicas son realmente útiles y una mejora importante con respecto a las matemáticas de Excel. Veamos algunos de los beneficios y algunos casos de uso:

1. **Las métricas calculadas son actuales y dinámicas**

   Al exportar números desde Adobe Analytics, se bloquean en un momento dado. Es absolutamente necesario saber el rendimiento de su sitio o aplicación el mes anterior, pero ¿cómo realizan los responsables de la toma de decisiones el seguimiento de cómo van las cosas a mediados de mes? Si la tasa de conversión se desploma durante un día y luego vuelve a la media al final del mes, ¿lo sabrá? Esa caída podría ser datos valiosos que revelen un problema importante de telemetría, o incluso más vital, un cambio en el comportamiento de los visitantes. Con una métrica calculada, puede crear un gráfico de esto y verlo el día que sucede, lo que le permite estar listo para responder.

1. **Las Métricas Calculadas Le Ahorran Tiempo**

   Yo he estado allí. Copie o pegue. Introduzca la fórmula o arrastre la celda sobre ella hacia abajo. Haga clic en el gráfico y cambie el rango para que tenga los últimos doce o trece meses. Ahora copie el gráfico. Ahora hazlo de nuevo. Y otra vez. Y otra vez. Envíe el PowerPoint. Es tedioso y lleva mucho tiempo y se siente como si tuvieras que hacerlo todos los meses para siempre.

   En su lugar, puede crear una Workspace que utilice su métrica calculada, que tenga Doce o Trece últimos meses completos como intervalo de fechas y que los datos y el gráfico se actualicen automáticamente a medianoche del primer día de cada mes. Los destinatarios pueden tener acceso directo a Workspace. Pueden recibir una copia de PDF automáticamente por correo electrónico el primer día del mes o después de usar Visualizaciones de texto para agregar su comentario sobre los datos (ya sabe, la parte divertida de los informes).

1. **Las métricas calculadas se pueden aplicar a grandes conjuntos de datos**

   Puede exportar todos los nombres de productos a Excel y empezar a calcular las tasas de conversión y los ingresos por visitante, pero esto se convierte en una molestia cuando tiene aproximadamente 100 000. No hay problema con las Métricas calculadas. Coloque la dimensión en una tabla como de costumbre y luego utilice las Métricas calculadas como métricas. Ahora tiene una tabla de ordenación dinámica que se actualizará automáticamente a medida que los productos o cualquier dimensión que esté utilizando se añadan al catálogo.

1. **Las Métricas Calculadas Evitan Errores**

   Se producen errores de Excel. Todos hemos estado allí. Diablos, toda la economía de Grecia y la reputación de dos académicos estimados se arruinaron debido a un error de fórmula de Excel. Probablemente no tengas una economía europea basada en tus habilidades con Excel, pero definitivamente hay alguna decisión sobre los presupuestos que va a cambiar en función de tus números. Usar métricas calculadas significa que puede crear una métrica, hacer que realice un control de calidad y, después, no volver a preocuparse por ella.

### Ahora que hemos repasado los beneficios de utilizar métricas calculadas, veamos cómo podemos ponerlas en práctica

**Caso de uso 1 : Tasas de conversión**

La mayoría de las tasas de conversión son solo una división simple. Divida el número de conversiones por el número de visitantes o visitas. Divida el número de vistas de página de la última página de un funnel entre el número de vistas de páginas de la primera página de un funnel. Divida el número de clics en campañas internas entre el número de impresiones. Todas estas acciones se pueden realizar fácilmente como métricas calculadas y colocadas en un panel que disfrute de una baja latencia de datos, visualizaciones de actualización y una mayor facilidad de uso compartido.

**Caso de uso 2: búsqueda interna**

La búsqueda interna es una de las herramientas más importantes para comprender el sitio. Los resultados de la búsqueda del sitio le indican qué les interesa a los visitantes y si pueden encontrarlo fácilmente a través de la navegación o no. Usted tiene que ser capaz de decir si su búsqueda del sitio está funcionando bien y el uso de un poco de adición básica y división puede darle esa respuesta.

Empecemos con los resultados de búsqueda. Desea saber si un término de búsqueda obtiene resultados o no genera nada. Esos suelen ser eventos separados. ¿Desea tener la molestia de obtener un tercer evento para todas las búsquedas internas del sitio agregadas? En su lugar, dé un respiro a sus desarrolladores y utilice Métricas calculadas para agregar Búsqueda interna: Resultados y Búsqueda interna: Sin resultados juntos para obtener Búsquedas internas totales.

¿Qué porcentaje de búsquedas no arroja resultados? Dividir búsqueda interna: no hay resultados por la nueva métrica calculada Búsquedas internas totales. Ahora sabe si es urgente crear contenido nuevo que coincida con esos términos de búsqueda, o si tal vez su equipo de contenido puede abordar prioridades más altas.

Queremos saber cuántas de esas búsquedas con resultados obtienen clics y, por lo general, también tienen una métrica separada para eso. Utilice Métricas calculadas para dividir el número de clics por el número de veces que ese término trajo resultados de búsqueda y mostrarlos como un porcentaje. Ahora tiene la tasa de clics para cada término de búsqueda interna del sitio. Puede aislar los términos de búsqueda que producen resultados no útiles. Tiene todos los datos históricos disponibles para que pueda graficarlos, y a medida que hace mejoras, puede ver fácilmente si funcionan viendo cómo esa tasa sube o baja.

Divida el número de búsquedas internas por el número de visitantes que realizan la búsqueda. Tiene búsquedas por visitante de cada término. Si ese número es alto (cuanto más cerca esté de 1,0 mejor), tiene uno de los dos posibles problemas. Los resultados en los que se hace clic son malos y los visitantes hacen varias búsquedas para encontrar los mejores resultados, o no pueden encontrar las páginas que buscan mediante la navegación.

¿Cómo puede medir si esas páginas clave se pueden encontrar a través de la navegación? Cree una métrica calculada para las vistas de página que siguen a una vista de página de resultados de búsqueda. Divídalo por el total de vistas de página de esa página. Ahora sabe el porcentaje de vistas de página que provino de los resultados de búsqueda. Si tiene un porcentaje alto, probablemente tenga que trabajar en la navegación.

### Las Métricas Calculadas Son Potentes

Espero que esto le haya mostrado algunas de las posibilidades de utilizar funciones matemáticas básicas en Métricas calculadas y que empiece a crear algunas por su cuenta. Esto solo comienza a describir las posibilidades de la matemática que se puede hacer en Métricas calculadas, incluso con cuatro funciones simples. Las métricas calculadas pueden ayudarle a comprender el comportamiento de los visitantes en un nivel completamente nuevo y, una vez que lo haya entendido, ha abierto la puerta al uso de funciones más complejas que también están disponibles para usted.

## Autor

Este documento fue escrito por:

![Toma de Gittai](assets/gittai.png)

**Gitai Ben-Ammi**, consultor principal en Concentrix Catalyst

Campeona de Adobe Analytics
