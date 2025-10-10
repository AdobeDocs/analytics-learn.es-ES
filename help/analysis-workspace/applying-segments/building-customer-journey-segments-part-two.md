---
title: 'Creación de segmentos de recorrido del cliente: segunda parte'
description: En la segunda parte, aprenda a crear segmentos de intención de visita de compra y retención para comprender el recorrido de compra de los clientes y personalizar el contenido. Mediante señales como clics o inicios de sesión en el modo "Reservar ahora", identificamos la intención de compra y retención para realizar un análisis eficaz y un marketing dirigido.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21T00:00:00Z
jira: KT-13476
thumbnail: KT-13476.jpeg
exl-id: 2db73010-5cd0-4454-a4ba-fc1667a50cba
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1997'
ht-degree: 0%

---

# Creación de segmentos de recorrido del cliente: segunda parte

En la segunda parte, aprenda a crear segmentos de intención de visita de compra y retención para comprender el recorrido de compra de los clientes y personalizar el contenido. Mediante señales como clics o inicios de sesión en el modo &quot;Reservar ahora&quot;, identificamos la intención de compra y retención para realizar un análisis eficaz y un marketing dirigido.

## Creación de segmentos de intención de visita de compra y retención

En nuestra última publicación, describimos el proceso de creación de segmentos de intención de visita y creamos nuestro primer segmento de intención de visita, One Hit Wonders. Hoy vamos a construir nuestros segmentos de compra y retención. Habíamos segmentado alrededor del 23% de nuestras visitas y creamos nuestros marcadores de posición para los segmentos de intención de visita restantes.

![Imagen 1](assets/Image-1.png)

Los segmentos de intención de visita que estamos creando ahora son la base para crear segmentos de recorrido de clientes basados en los visitantes. Generaremos esos segmentos de recorrido basados en visitantes después de crear los segmentos de intención de visita.

Recuerde que la creación de segmentos de intención de visita es un proceso de eliminación. Por lo tanto, no vamos a crear estos segmentos en orden cronológico. Estamos creando nuestros segmentos de intención de visita para que sean más fáciles de definir y más difíciles de definir:

1. Intención: 0 - Una visita maravillas
1. Intención: 3 - Compra
1. Intención: 4 - Retención
1. Intención: 2 - Consideración
1. Intención: 1 - Conocimiento

En nuestro último post, llamé al segmento &quot;Comprar&quot; &quot;Reserva&quot; ya que estoy en el negocio de viajes. Pero en adelante lo llamaremos el segmento de compra para facilitar su aplicación en múltiples industrias.

Cuanto más clara sea la señal, más fácil será crear el segmento. En nuestro último post, creamos nuestro segmento One Hit Wonders, que era el más fácil de definir ya que solo es tráfico devuelto. Verá que los segmentos de intención de compra y retención también son muy fáciles de definir, ya que se basan en señales muy claras.

## El Recorrido del cliente es diferente a la tendencia a comprar

A medida que analizamos la creación de nuestro segmento de intención de compra, es importante recordar que identificar dónde se encuentra un cliente en su recorrido es diferente a la tendencia. Es posible que tenga algunos modelos de tendencia a la compra que puntúan a los visitantes web para predecir la probabilidad de que realicen una compra. Estos modelos son muy útiles, pero son diferentes al segmento de intención de compra que vamos a crear hoy.

Mientras que un modelo de tendencia busca predecir si un visitante comprará, nuestros segmentos de intención de visita buscan comprender dónde se encuentra una persona en su recorrido de compra. El uso de segmentos de intención para comprender el estado de ánimo de un cliente nos ayuda a personalizar el contenido y el marketing personalizado para impulsar el tráfico adecuado y alimentar nuestro canal de ventas. Por lo tanto, nuestro segmento de intención de compra busca señales de comportamiento explícitas que indiquen que un visitante está buscando realizar una compra.

## Creación del segmento de intención de visita de compra

El segmento Propósito de la visita de compra es fácil de definir. En mi caso, cualquiera que haga clic en el botón &quot;Reservar ahora&quot; está indicando algún tipo de intención de reservar un crucero. Es similar a hacer clic en &quot;Finalizar compra&quot; para un retailer en línea o en un vínculo de &quot;Suscribirse&quot; en un contexto multimedia.

Tendrá que actuar con criterio a la hora de decidir qué señal utilizar para deducir la intención de compra. Queremos que nuestro segmento de intención de compra contenga todas las compras, pero la tasa de conversión no debe ser del 100 %. Por lo tanto, no queremos utilizar la página de confirmación de compra o de agradecimiento para este segmento.

Del mismo modo, la página Revisar tu compra (o lo que sea inmediatamente antes de la confirmación de la compra) probablemente esté demasiado lejos en funnel como para ser útil para el análisis y el direccionamiento.

A medida que se desciende más por la funnel, puede resultar menos claro si la señal es útil o no para indicar que un cliente tiene la intención de realizar una compra. En mi caso, &quot;Reservar ahora&quot; es similar a un enlace de &quot;Pago y envío&quot; minorista, y esa es la señal que usé. Sin embargo, en un contexto minorista, el cierre de compra puede estar demasiado lejos en el funnel y ver carro, o incluso puede que Añadir al carro de compras esté mejor.

Podemos pensar en esto como en una tienda de comestibles. Si alguien recoge un producto del estante eso no significa que tenga la intención de comprarlo. Incluso si lo ponen en su carrito, podrían ponerlo de inmediato en el estante. Pero si ponen el producto en su carro y empiezan a caminar con él, hay una buena probabilidad de que quieran comprarlo. Y si entran en la línea de compra con ese producto es una apuesta bastante buena que van a comprar.

Sugiero utilizar las páginas visitadas u otras señales explícitas de intención de compra y evitar otras señales menos directas para identificar la intención de compra. Por ejemplo, no utilizaría el número de sesiones o el número de páginas en una sesión o similar. Estas señales indirectas indican Consideración, no intención de compra. Recuerde, el propósito de este segmento es deducir la intención del visitante para la visita, no su tendencia.

### Uso de Analytics Workspace para identificar señales de intención de compra

El informe Visitas en el orden previsto es muy útil para identificar una buena señal que indique la intención de compra. Busque un lugar que indique la intención de forma lógica. Puede confirmar que el paso indica intención cuando ve una visita en el orden previsto notable que va a ese paso, seguido a menudo de una visita en el orden previsto más pequeña para el paso inmediatamente después.

![Imagen 2](assets/Image-2.png)

También resulta útil observar las tasas de conversión asociadas con las distintas páginas del sitio. Esto resulta especialmente útil para identificar páginas que indican una intención de compra, pero que pueden no ser necesarias para realizar una compra (como páginas de financiación, páginas de configuración de compra, etc.).

![Imagen 3](assets/Image-3.png)

Por último, es importante incluir todas las páginas entre el inicio de la compra y la confirmación de compra en el segmento. Los visitantes pueden rebotar y volver a introducir el flujo de compra en diferentes puntos.

### Exclusión de otros segmentos

Recuerde de nuestro primer post que nuestros segmentos de Intención de visita deben ser mutuamente excluyentes y completamente exhaustivos. Este es el estribillo que escucharás mucho en esta serie.

Asegúrese de que el segmento Intención de compra excluya el segmento Uno y Listo. Solo debe excluir el segmento Uno y Listo porque las señales que usamos para la intención de compra son muy específicas.

Tenga en cuenta que al excluir los segmentos Uno y Listo, podría excluirse a alguien que vuelva a entrar al sitio en una página de cierre de compra. Esto es correcto. La definición misma de Uno y Listo es una vista de página, lo que significa que aunque un visitante entre o actualice en una página de cierre de compra, su visita no progresó, por lo que no hay expresión de intención de compra.

### El segmento por intención de compra en el Generador de segmentos

La definición del segmento para la intención de compra es muy sencilla.

Si utiliza el contenedor de visita, incluya aquellas páginas u otras acciones que indiquen explícitamente una intención de realizar una compra. Si tiene varias condiciones de inclusión, asegúrese de colocarlas en un contenedor unido por la condición &quot;And&quot;.

Agregue un contenedor de exclusión al segmento unido por la condición &quot;And&quot;. Agregue su definición de segmento Maravillas de una visita (Vistas de página es igual a 1) al contenedor Excluir.

![Imagen 4](assets/Image-4.png)

Se recomienda etiquetar los contenedores como práctica recomendada. Se alegrará de haberlo hecho, especialmente porque nuestras definiciones de segmentos se vuelven más complejas.

Ahora que hemos creado el segmento Calidad de la compra, podemos usar la Workspace de calidad de datos por intención de visita para ver que nuestro segmento Calidad de la compra es mutuamente excluyente con nuestro segmento Uno y Listo.

![Imagen 5](assets/Image-5.png)

## Creación del segmento de intención de visita de retención

En el negocio de cruceros, muchos huéspedes vienen a nuestro sitio web para gestionar una reserva, pero no necesariamente para hacer una compra. Pueden venir al sitio para introducir información sobre el viaje, revisar su itinerario, hacer reservas para la cena u otras cosas, sin comprar un crucero. Nuestros huéspedes también pueden comprar excursiones en tierra u otras mejoras en su experiencia. Consideramos que estas mejoras son parte de la retención, por lo que las mantenemos separadas de nuestro segmento de reservas (que llamamos &quot;compra&quot; en esta serie de blogs).

Es posible que los clientes minoristas puedan realizar devoluciones o administrar su programa de fidelidad. Es posible que los suscriptores de medios o tecnología estén utilizando el producto. Si su invitado está en su sitio web para administrar su relación con usted, eso es una Visita de retención y debemos ver esas señales. Y si proporciona un producto en línea, como Medios, Tecnología, Banca en línea u otros, es probable que haya muchos otros tipos de segmentos de intención de visita que no analizaremos en esta serie.

Al igual que con el segmento Intento de compra, buscamos indicaciones muy explícitas de intención. Para mí, tenemos una sección completa del sitio dedicada a la gestión de un crucero, por lo que es fácil identificar esas páginas. Esto podría ser más complejo para otras empresas. Busque señales como inicios de sesión, administración de cuentas, visitas a páginas de asistencia y similares.

Debo señalar que &quot;Retención&quot; es un nombre un poco incómodo para esta intención de visita, ya que el visitante no está en nuestro sitio, &quot;por lo que puedo ser retenido como cliente&quot;. Retención es nuestra intención para esa visita. Solo recuerde ser empático con nuestros clientes y mantener un enfoque centrado en el cliente.

### Uso de Analytics Workspace para identificar señales de intención de retención

De nuevo, Analytics Workspace nos ayuda a identificar la intención de retención. Puede utilizar las dimensiones páginas, sección del sitio o segmento personalizado para categorizar las páginas. Busque páginas con tasas de conversión de compra bajas. En nuestro caso, encontramos que las páginas de Check-In Online y Shore Excursion (Shorex) tienen tasas de conversión relativamente más bajas que otras páginas que están asociadas más lógicamente con las compras y compras.

![Imagen 6](assets/Image-6.png)

También es buena idea buscar páginas de alto tráfico en Workspace. Analiza la lista de páginas con mucho tráfico y decide si indican una intención de retención.

## Exclusión de otros segmentos

De nuevo, los segmentos por intención de visita deben excluirse mutuamente y ser completamente exhaustivos. ¡Si no estás cansado de leer esto todavía, lo estarás! Para nuestro segmento Intención de retención, es de vital importancia excluir los comportamientos de Intención de compra.

Para la mayoría de nosotros, la intención de compra y la intención de retención no son comportamientos mutuamente excluyentes. Tenemos invitados que vienen al sitio web para administrar su próximo crucero, pero también para reservar su próximo viaje (gracias). Si es un restaurante, un visitante puede comprobar sus puntos de fidelidad y luego realizar un pedido en línea.

Aunque el comportamiento no se excluya mutuamente, nuestros segmentos deben utilizarse para el análisis del Recorrido del cliente. Podemos crear otros segmentos muy interesantes para analizar la superposición entre los comportamientos de compra y lealtad. Pero para nuestros propósitos actuales, necesitamos que estos segmentos sean mutuamente excluyentes.

Dado que la generación de demanda es uno de los principales objetivos de marketing, nuestro segmento Retention Intent excluirá Purchase Intent. En otras palabras, si alguien viene a nuestro sitio para administrar un crucero, pero también indica la intención de reservar un nuevo crucero, esa visita irá al segmento de intención de compra.

### El segmento por intención de retención en el Generador de segmentos

Nuestras definiciones de segmentos se están volviendo un poco más complejas. Incluya visitas en su segmento. Añada las señales de Retention Intent. Para mí, esto fue sencillo. Si el nombre de la página comienza con &quot;bge:&quot; (nuestras páginas de invitado reservadas), usted está en el segmento. He agregado vistas de página es mayor que una para una medida adicional (pero seguiremos excluyendo una de las maravillas de la visita).

A continuación, añada contenedores de exclusión para sus visitas de Maravillas de una visita y Comprar intención. Asegúrese de que los contenedores se unen con la condición &quot;Y&quot;.

![Imagen 7](assets/Image-7.png)

Una vez más, consulte la Workspace de calidad de datos por intención de visita para asegurarse de que los segmentos se excluyan mutuamente. ¡Nuestros segmentos por intención de visita están tomando forma muy bien!

![Imagen 8](assets/Image-8.png)

En este punto, hemos configurado tres de nuestros cinco segmentos de intención de visita. Vemos que estos segmentos son mutuamente excluyentes. En nuestro próximo post, crearemos los segmentos finales de Intención de visita, Consideración y Conocimiento, y todos nuestros segmentos serán completamente exhaustivos. Una vez configurados los segmentos por intención de visita, los reuniremos en segmentos basados en visitantes que le resultarán muy útiles para el análisis y la personalización.

## Autor

Este documento fue escrito por:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, director de análisis digital

Campeona de Adobe Analytics
