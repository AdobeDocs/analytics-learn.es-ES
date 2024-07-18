---
title: Diferencias entre el generador de segmentos y los segmentos rápidos en Analysis Workspace
description: Los segmentos pueden ser una de las herramientas más potentes de su kit de herramientas de análisis de datos. Conozca las diferencias entre el uso del generador de segmentos y los segmentos rápidos en Analysis Workspace para que sean más eficientes.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
exl-id: 144e71fd-8d42-4d20-b55e-3d81ad992a79
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 100%

---

# Diferencias entre el generador de segmentos y los segmentos rápidos en Analysis Workspace

Los segmentos pueden ser una de las herramientas más potentes de su kit de herramientas de análisis de datos. Conozca las diferencias entre el uso del generador de segmentos y los segmentos rápidos en Analysis Workspace para que sean más eficientes.

>[!TIP]
>
> Haga clic en la imagen situada en la parte inferior de la página para descargar un recordatorio útil sobre cuándo utilizar cada herramienta en Analysis Workspace.

Los segmentos pueden ser una de las herramientas más potentes de su kit de herramientas de análisis de datos. Si desea ver grupos específicos de tráfico, secciones del sitio o recorridos de clientes, el uso de segmentos puede ser una buena manera de enfocar el análisis en un subconjunto particular de tráfico hacia el sitio. Dado que provengo de un entorno de venta minorista, algunos de los segmentos más útiles que he realizado son para distintos tipos de grupos de clientes, por ejemplo clientes nuevos frente a clientes existentes, clientes que iniciaron sesión en una cuenta frente a invitados, etc. Pero también puede utilizarlos para diferentes secciones del sitio, clientes que realizan acciones específicas o cualquier otra cosa que pueda imaginar.

**Existen dos formas principales de generar segmentos:**

* Uso del generador de segmentos en el menú de componentes
* Uso de segmentos rápidos en la parte superior de un panel

Si crea el segmento con el generador de segmentos, puede guardarlo para reutilizarlo en otros proyectos. Esta es una buena manera de poder centrarse en grupos específicos de clientes, por ejemplo, personas que visitan determinadas secciones del sitio y luego realizan una compra. Por otro lado, si está realizando un análisis de exploración y desea probar diferentes configuraciones de segmentos, el generador rápido de segmentos puede ser una buena ayuda. Veamos algunos de los principales beneficios de cada método.

## Segmentos rápidos

En la parte superior de cada panel, puede hacer clic en el icono de segmento rápido (un canal con el símbolo +) para abrir el generador. Esto le permite generar un segmento en cualquier nivel (visita individual, visita o visitante) con hasta tres condiciones. Al igual que el generador de segmentos principal, esto le proporciona una indicación en el lado derecho que indica si el segmento devuelve datos y el % de la población de tráfico total incluida en el segmento, aunque esta es una versión más simplificada que la vista de volumen de segmentos completa mostrada en el generador de segmentos. Al agregar más de una condición, puede utilizar los operadores &quot;y&quot; y &quot;o&quot;. Lamentablemente, no hay una opción &quot;then&quot; para segmentos rápidos, por lo que si necesita segmentos secuenciales tendrá que usar el generador de segmentos completo. También hay un límite de un contenedor en un segmento rápido. Ya que en realidad está pensado para utilizarse en segmentos básicos que se pueden crear y editar rápidamente. Una vez que un segmento rápido se aplica a un panel o se guarda, ya no se puede editar dentro del panel.

Al hacer un análisis exploratorio, y desea probar diferentes tipos de segmentos para ver cómo reaccionan los distintos grupos de clientes o el rendimiento de las distintas categorías: el uso de segmentos rápidos es mucho más rápido que el uso del generador de segmentos. Además, estos segmentos solo están disponibles en el proyecto en el que se crearon, por lo que si resulta que no proporciona los resultados que desea, no tiene que preocuparse de eliminar el segmento guardado de la lista maestra. Si, después de probar los segmentos, se da cuenta de que será útil en otros proyectos, siempre puede hacer clic en el botón &quot;abrir generador&quot; para abrir el segmento en el generador de segmentos completo y guardarlo como segmento normal. Sin embargo, una vez que lo haga, ya no podrá editarlo en el generador rápido de segmentos.

![Segmento rápido](assets/quick-segement.png)

## Generador de segmentos

Se puede acceder al generador de segmentos haciendo clic en el símbolo + situado encima de la lista de segmentos en el menú de componentes de la izquierda, o haciendo clic en la lista desplegable de componentes y seleccionando &quot;Crear segmento...&quot; A diferencia de los segmentos rápidos, esta opción tiene todas las opciones disponibles. Para agregar varias condiciones, puede crear segmentos secuenciales utilizando el operador &quot;then&quot;. Los segmentos secuenciales también le permiten utilizar &quot;logic group&quot; (grupo lógico) como nivel (en lugar de visita individual, visita o visitante). El generador de segmentos también le permitirá agregar una descripción a los segmentos, lo que puede añadir contexto sobre quién creó el segmento o qué tipo de datos se ha creado para filtrar, o incluso simplemente añadir &quot;etiquetas&quot; al segmento para propósitos organizativos, los cuales no son posibles en el generador rápido de segmentos.

El uso del generador de segmentos es esencial cuando el segmento va a tener más de 3 condiciones, si necesita utilizar contenedores o desea segmentos secuenciales. El generador de segmentos completo tiene muchas más opciones para crear segmentos más intrincados, lo que puede ayudarle a desglosar diferentes tipos de clientes, categorías, recorridos de clientes, etc. Una vez creados y guardados estos segmentos, se añaden a la lista maestra de segmentos, lo que significa que se pueden etiquetar, aprobar, compartir, utilizar en varios informes y publicarse en el Experience Cloud. La publicación en el Experience Cloud le permite utilizar el segmento en otros productos de Adobe, como en Adobe Target para la segmentación personalizada. Los segmentos creados en el generador de segmentos no se pueden editar en el panel de segmentos rápidos. Deberá abrir el generador de segmentos para realizar cualquier cambio en ellos. Afortunadamente, la visualización de vista previa a la derecha proporciona un análisis más detallado del tráfico que el segmento traería durante los últimos 90 días, lo que significa que es más fácil asegurarse de que el segmento está trayendo lo que desea antes de guardarlo.

![Generador de segmentos](assets/segment-builder-quick.png)

## Casos de uso

En diferentes industrias, los usos para crear segmentos personalizados pueden diferir. Al trabajar para la división de comercio electrónico de un gran minorista, a menudo realizamos análisis exploratorios para determinar qué rutas toman los clientes para comprar. Cuando vemos picos o caídas en acciones como agregar productos al carro de compras o realizar pedidos, aquí es donde el uso de segmentos rápidos puede resultar útil. Durante un análisis, puedo crear rápidamente un segmento para un tipo específico de cliente o para una acción o vínculo en particular en el que hacen clic. Al no tener que abrir el generador de segmentos y guardar cada segmento, puedo agregar las condiciones rápidamente y luego eliminarlas con la misma rapidez. Esto ahorra mucho tiempo al intentar explicar por qué vemos un cambio en nuestro sitio.

Alternativamente, hay ocasiones en las que el generador de segmentos ha sido mi referencia. No todos los clientes son iguales y, a menudo, queremos ver los tipos específicos de clientes identificados por acciones o rutas que toman. Mediante el generador de segmentos, podemos añadir varias condiciones para identificar los distintos tipos de clientes y guardar los segmentos para que puedan compartirlos y usarlos varios analistas. Es importante que estos tipos de segmentos sean coherentes en todos los informes, por lo que tener uno integrado que todos puedan utilizar es mejor que cada persona cree su propia versión, ya que los resultados pueden diferir.

En general, tanto los segmentos rápidos como el generador de segmentos son excelentes herramientas para su análisis. Cada uno tiene sus propósitos, beneficios y desventajas. Para obtener una guía de referencia rápida, consulte nuestra hoja útil de consejos y trucos descargables.

## Autor

Este documento fue escrito por:

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, Analista digital III en Best Buy Canada

Campeona de Adobe Analytics

## Descargar

[![Descarga rápida de segmentos](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
