---
title: Generación de segmentos de Recorrido del cliente
description: Obtenga información sobre cómo crear segmentos de recorrido de clientes basados en el comportamiento en Adobe Analytics y mejorar la experiencia de sus clientes con Adobe Experience Cloud siguiendo esta guía paso a paso.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13180
thumbnail: KT-13180.jpeg
source-git-commit: d7b1fac5c98080f9ca786ea21a3700d2937c7ebc
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---


# Generación de segmentos de Recorrido del cliente

Obtenga información sobre cómo crear segmentos de recorrido de clientes basados en el comportamiento en Adobe Analytics y mejorar la experiencia de sus clientes con Adobe Experience Cloud siguiendo esta guía paso a paso.

Vamos a crear mejores segmentos de recorrido de clientes! En esta serie, utilizaremos Adobe Analytics para definir segmentos basados en el comportamiento, estimar el tamaño de la audiencia y rastrear el movimiento del usuario. Al final, podrá personalizar los medios y mejorar la experiencia de sus clientes con Adobe Experience Cloud. Tenga en cuenta que estos segmentos están activos y que deben actualizarse a medida que obtenga más información sobre sus clientes. Aunque los informes pueden presentar algunos desafíos, no se preocupen, ¡les guiaré a través de ellos! Comencemos por crear nuestro primer conjunto de segmentos de Recorrido de clientes, empezando por el segmento &quot;Maravillas de una visita&quot;.

Hoy, crearemos marcadores de posición para nuestro primer conjunto de segmentos de Recorrido de clientes, crearemos un espacio de trabajo de Adobe Analytics para ayudarnos a definir nuestros segmentos y definiremos nuestro primer segmento, &quot;One Hit Wonders&quot;.

Al final de esta serie, podrá crear segmentos de recorrido de clientes en Adobe Analytics basados en señales de comportamiento. Podrá estimar el tamaño de cada audiencia en cada fase del recorrido y comprender a qué velocidad se mueven los usuarios entre esas etapas. Además, podrá exportar esas audiencias de recorrido de clientes a Adobe Experience Cloud para permitir la personalización y la segmentación de medios.

Cada negocio es diferente, lo que significa que los segmentos de recorrido de los clientes se verán diferentes a los míos. Por lo tanto, en lugar de prescribir fórmulas específicas para sus segmentos, sugiera algunas cosas a considerar y un proceso general para crearlos.

También es importante tener en cuenta que los segmentos de recorrido de los clientes serán segmentos vivos. Este no es un ejercicio único. A medida que obtenga más información sobre sus clientes, actualizará estos segmentos. Esto plantea algunos problemas para la presentación de informes. Las personas desean coherencia en sus informes y, si cambian las definiciones de los segmentos, también cambiarán los números de los informes.

## Introducción a los segmentos por intención de visita

El primer paso para crear segmentos de recorrido de clientes es deducir por qué un invitado está en su sitio web utilizando señales de comportamiento y, si está disponible, datos de la Voz del cliente. Generaremos un conjunto de segmentos de Intención de visita para categorizar todas las visitas en el sitio web. En este punto, nuestros segmentos de intención de visita deben ser mutuamente excluyentes y completamente exhaustivos. Cada visita debe pertenecer a un segmento, y solo a uno, Intención de visita .

Los segmentos Intención de visita describen una visita, por lo que utilizaremos el contenedor Visitas en la definición del segmento.

Mi conjunto inicial de segmentos de intención de visita incluía:

* Una visita se pregunta
* Conciencia
* Consideración
* Reserva (compra)
* Retención (administrar una reserva/compra)

Para que mis segmentos de Intención de visita resultaran fáciles de usar, añadí el prefijo &quot;Intención:&quot; a mis nombres de segmento, les di un número para permitir la clasificación y los etiqueté como &quot;intención&quot;. Mis segmentos se veían como la imagen de abajo.

![segmentos de intención](assets/intent-segments.png)

**Continúe y cree los segmentos de intención de la visita utilizando el contenedor de visitas con una definición de marcador de posición de Vistas de página >= 1.**

Como veremos, la creación de estos segmentos es un proceso iterativo e interconectado. Describiré el proceso de crear estos segmentos en una publicación futura.

## El espacio de trabajo de calidad de los datos del segmento de intención de visita

![espacio de trabajo de intención de visita](assets/visit-intent-workspace.png)

Usé un espacio de trabajo simple para asegurarme de que estaba definiendo bien mis segmentos de intención de visita. Recuerde que cada visita debe pertenecer a un segmento, y solo a uno, de Intención de visita. El espacio de trabajo que configuré garantiza que se cuenten todas las visitas y que no haya superposición entre los segmentos.

He llamado a este espacio de trabajo &quot;CALIDAD DE DATOS: Visitar segmentos de intención&quot; con las etiquetas &quot;calidad de datos&quot;, &quot;intención de visita&quot; y &quot;recorrido del cliente&quot;. Más adelante, crearemos un &quot;Tablero de intenciones de visita&quot;, de modo que el prefijo &quot;CALIDAD DE DATOS&quot; indica que este espacio de trabajo sirve para configurar y mantener los segmentos. Es un tablero administrativo que tiene poca perspectiva comercial pero es importante para garantizar el mantenimiento de los segmentos. Es aconsejable volver a este tablero de forma rutinaria, o configurar alertas, para asegurarse de que los segmentos siguen definidos correctamente.

La visualización más importante de este espacio de trabajo es la visualización de forma libre Superposición de segmento en el centro izquierdo. Con la métrica Visitas, cree filtros de columna para cada uno de los segmentos de Intención de visita, además del segmento Todas las visitas en la columna más a la derecha. Cree filas para cada segmento de Intención de visita a la izquierda. Ahora tendrá una visualización entre fichas. Cuando los segmentos estén correctamente configurados, solo habrá datos en una columna y una fila, en la intersección de cada segmento de intención de visita consigo mismo.

Las siguientes visualizaciones más importantes son las métricas de resumen en la parte superior izquierda. El resumen de visitas segmentadas toma su valor de la columna Todas las visitas en la visualización Superposición de segmento inmediatamente inferior. El resumen de todas las visitas tiene su propia tabla oculta.

![todas las visitas](assets/all-visits.png)

En la parte superior derecha, he añadido métricas adicionales a cada uno de los segmentos para darle un poco de &quot;sabor&quot; a cómo se están formando los segmentos. En concreto, dado que estos segmentos son mutuamente excluyentes, solo espero ver las reservas para el segmento Intención de reserva (tenga cuidado, no veremos tasas de conversión cuando hagamos que estos segmentos de Intención de visita estén basados en visitantes).

Recuerde que acabamos de crear segmentos de marcador de posición. Así que, inicialmente, su espacio de trabajo se verá maravilloso. Todos los segmentos de intención de visita se superpondrán al 100% porque tienen la misma definición. Esto es correcto y exactamente lo que desea ver en este punto del proceso. A medida que creamos las definiciones de segmentos, verá que estos segmentos empiezan a tomar forma.

![Definiciones de segmentos de intención de visita](assets/visit-intent-segment-defs.png)

## Generación del primer segmento de intención de visita

Definir los segmentos de intención de visita es un proceso de eliminación y hay mucha interdependencia entre ellos. Así que no construí estos segmentos en el orden del recorrido, los construí en orden de los más fácilmente definidos a los más desafiantes. Eso me dio esta orden:

1. Intención: 0 - Una maravilla de visita
1. Intención: 3 - Reserva
1. Intención: 4 - Retención
1. Intención: 2 - Consideración
1. Intención: 1 - Sensibilización

Bastante aleatorio, ¿eh? La definición de estos segmentos de intención de visita era un proceso iterativo, de ida y vuelta, y a menudo un ajuste a un segmento requería actualizaciones para otros segmentos. Esto resultará más claro a medida que describa cómo definí cada uno de estos segmentos.

Hoy, definiremos nuestro primer segmento, y el más sencillo, &quot;One Hit Wonders&quot;

## Generación del segmento &quot;One Hit Wonders&quot;

Mi primer segmento, &quot;One Hit Wonders&quot;, fue fácil de definir. Es simplemente cualquier visita con una sola vista de página. Realmente no sabemos por qué ese usuario estaba en el sitio web, porque rebotaron. Supongo que podríamos adivinar una intención basada en su página de entrada, pero con solo una vista de página, simplemente no hay suficiente información para hacer una suposición informada sobre la intención.

![Definición del segmento](assets/segment-def.png)

Después de definir este segmento, empezará a ver que el espacio de trabajo de intención de la visita está tomando forma.

![Más definiciones de segmentos](assets/more-segment-defs.png)

La creación de segmentos de recorrido de clientes mediante Adobe Analytics es un proceso desafiante pero gratificante. Mediante la creación de segmentos basados en el comportamiento, la estimación del tamaño de las audiencias y el seguimiento de los movimientos de los usuarios, las empresas pueden personalizar los medios y mejorar la experiencia del cliente. Cada empresa es única y no hay fórmulas específicas para crear segmentos, pero sí directrices y un proceso a seguir. Los segmentos deben actualizarse a medida que las empresas aprendan más sobre sus clientes, lo que presenta desafíos en materia de informes. Al seguir el proceso de creación de segmentos de intención de visita, las empresas pueden mejorar la experiencia general del cliente.

## Autor

Este documento fue escrito por:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, análisis digital

Campeona de Adobe Analytics


