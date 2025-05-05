---
title: Explicación del panel de atribución de Adobe Analytics y las ventanas retroactivas
description: Aprenda a utilizar el panel de atribución y la ventana retrospectiva para comprender el comportamiento del cliente y personalizar cómo los elementos de dimensión obtienen crédito por los eventos de éxito.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
exl-id: 1da9334b-0edb-4237-b7ca-57640865208c
source-git-commit: f1bb981a83eb698f4185a22c367346a9ddd0c755
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 1%

---

# Explicación del panel de atribución de Adobe Analytics y las ventanas retroactivas

Cuando pensé por primera vez en el [panel de atribución](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=es) y en la **ventana retrospectiva**, inmediatamente me recordaron el concepto de &quot;*viaje en el tiempo&#39;*; entonces, por supuesto, también me recordaron que nuestra respuesta típica a muchas herramientas nuevas como estas es simplemente dejar de intentar usarlo, porque se ven muy complicadas.

Honestamente, miren todas esas opciones, interruptores, paneles, lecturas y botones.  Y en serio, hablemos de esas complicadas luces parpadeantes, mangueras, medidores... ESPERA!!  No es el momento de distraernos hablando de máquinas del tiempo, simplemente no tenemos tiempo... ¿o sí?

Admitiré que el **panel de atribución** es una herramienta bastante compleja; sin embargo, nuestro trabajo típico como analistas, día tras día, es usar otra de nuestras herramientas favoritas y altamente complejas para también echar un vistazo a lo que sucedió en el pasado. ¡Esa herramienta se llama ***Adobe Analytics***!  Así que sí, para responder a nuestra muy relevante pregunta, creo que estas dos cosas dicen que tenemos mucho tiempo.

Por lo tanto, ¿por qué deberíamos permitir que algo como un poco de miedo se interponga en el camino de herramientas tan asombrosas, sofisticadas y poderosas como estas que literalmente nos permiten mirar *hacia atrás* a tiempo, todos y cada uno de los días?

Después de todo - esto es VIAJE EN EL TIEMPO, amigos!!  Estamos hablando de ese tipo de cosas.  Correcto???!!

Entonces, ¿qué estamos esperando - un coche de metal brillante, una caja de policía, o una cabina telefónica vintage utilizando el cableado de un paraguas viejo como su antena para aparecer en nuestra puerta?

¡No!  Tenemos algo aún mejor, así que vamos a atarnos y aguantar!

Bueno... se te ocurre la idea.


Ahora que todos estamos entusiasmados con el viaje en el tiempo, respiremos profundo, retrocedamos un poco, establecamos lo que es **el panel de atribución** *realmente* y desglosemos las cosas un poco:

![Atribución](assets/attribution.png)

*Figura 1 - Los números mostrados están alineados con el texto más abajo*

En **Attribution**, considere simplemente cómo los eventos o las acciones pueden ser causados por un individuo, varios individuos o uno de cualquier número de eventos diferentes a lo largo del tiempo.

Según el [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=es), *Attribution* permite a los analistas personalizar la forma en que los elementos de *Dimension* reciben crédito por *eventos de éxito*.


>[!WARNING]
>
>**Los modelos de atribución** se asocian con tanta frecuencia con **canales de mercadotecnia** que *taché* ❷ CANAL a propósito en la imagen anterior para ilustrar que es posible realizar análisis de **atribución** con casi cualquier otra ***dimensión***.


De hecho, rara vez un recorrido determinado del cliente es verdaderamente lineal y con menor frecuencia aún predecible.  Además, cada cliente seguirá su propio ritmo; a menudo, puede duplicarse, paralizarse, abandonarse o participar en otro comportamiento no lineal. Estas acciones orgánicas hacen que sea difícil o prácticamente imposible conocer el impacto de los esfuerzos de marketing en todo el recorrido del cliente. También obstaculiza los esfuerzos por unir múltiples canales de datos.

Eso es correcto.  Deje sus analogías de &quot;dominó&quot; en la puerta y abra sus mentes a conceptos más a lo largo de las líneas del efecto mariposa y la teoría de cuerdas - pero como todo lo demás, necesitamos comenzar con algunos de los conceptos básicos.

## **Modelos de atribución**

Cuando usamos el **panel de atribución**, es posible que empecemos a observar diferentes cosas.  Por ejemplo, los **modelos de atribución** nos muestran cómo nuestras *conversiones* (es decir, ❶ **métricas de éxito**) pueden distribuirse entre *visitas* en un grupo determinado.

En pocas palabras, si **10 personas** presionan un **BOTÓN ROJO GRANDE** para cruzar una puerta, nuestros **modelos de atribución** nos dirán cuál de esas **10 personas** queremos asignar &quot;crédito&quot; - o mejor dicho, cuánto *crédito* queremos asignarles - por presionar dicho botón.

![Botón](assets/button.png)

Con esto en mente, aquí hay algunos ejemplos de cómo los ❸ **modelos de atribución** podrían afectar a esas **10 personas**:

- **Primer contacto**: este modelo funciona exactamente como suena al dar **100% de crédito** a la *primera* persona que entró por la puerta.  Es más probable que los especialistas en marketing usen este método para tácticas como ***medios sociales*** o ***visualización***; sin embargo, también es una buena táctica para usar con frecuencia para la efectividad de recomendaciones de productos en el sitio.
- **Último contacto**: esta táctica también funciona exactamente como suena, pero en su lugar da **100% de crédito** a la ÚLTIMA persona que entró por la puerta.  Este modelo se usa generalmente para analizar cosas como la ***búsqueda natural (orgánica)*** y otras campañas de *corto plazo* del ciclo de marketing.
- **Lineal**: Este modelo distribuye crédito igual entre TODAS Y CADA UNA DE LAS PERSONAS que entraron por la puerta.

  >[!CAUTION]
  >
  >Sin embargo, se recomienda tener cuidado aquí, ya que tiene el potencial de propagar sus resultados muy finos muy rápidamente al aplicar esta táctica, teniendo en cuenta cuanto más tiempo se ejecuta y mayor es la audiencia a la que llega.

- **Forma de U**: este método asigna el **40%** del crédito a la *primera persona* en la puerta, distribuye el **20%** del crédito entre *todos los que están entre* y, a continuación, otorga el **40%** a la **última** hasta. Este modelo se usará con más frecuencia en situaciones en las que tenga un **ciclo largo de conversión/ventas** que contenga *varios puntos de contacto* a lo largo del camino.  En este caso, el objetivo es resaltar principalmente las tácticas de marketing de ***first*** y ***last*** que contribuyeron a la conversión del cliente.
- **J**-**Forma** y **J inversa**:
   - Piense en **Forma de U**, pero en su lugar este modelo asigna un crédito de **60%** a la *última persona* que camina por la puerta, de **20%** a *primero* y luego *divide* el **20%** restante entre *todos los demás* en el medio.  **J inverso** hace exactamente lo contrario.

     El objetivo aquí es poner la mayor parte de tu énfasis, ya sea al *principio* o al *final* de tu campaña; sin embargo, todavía quieres asignar una cierta cantidad de crédito al elemento que contribuye en el extremo opuesto mientras reconoces a los &quot;chicos pequeños&quot; en el camino.

- **Deterioro de tiempo**: Ahora, sería negligente si no compartiera este. Este modelo tiene literalmente una vida media que decae exponencialmente - ¡con el tiempo!  En este caso, el parámetro *default* para la semivida de este modelo es de **7 días**.  La forma en que funciona es aplicar *weight* a cada **canal de marketing**, *según la cantidad de tiempo* que transcurre después del *punto de contacto inicial* y cuando el cliente se convierte.

  **Deterioro de tiempo** y **modelos de atribución en forma de U** se suelen usar para medir campañas a más largo plazo, pero como puede ver, tienen objetivos ligeramente diferentes, basados en cómo *ponderan* el valor del resultado en última instancia.

- **Personalizado**: Usted elige y elige quién va a obtener crédito.  ¡Es tu campaña!

Para obtener más información sobre estos y otros modelos de atribución, [haga clic aquí](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=es)

Para hacer esto aún más interesante, ¡hablemos de volver atrás el reloj!

## **Ventanas retroactivas**

Ahora es el momento de empezar a llevar tu mente al siguiente nivel.  Aquí es donde literalmente agregamos el elemento de viaje en el tiempo a nuestro análisis -y nuevamente, estamos empezando con lo básico.

***Adobe*** define ❹ **ventanas retrospectivas** como &quot;la cantidad de tiempo que una conversión debe devolverse hacia atrás para incluir puntos de contacto. Los modelos de atribución que dan más crédito a las primeras interacciones ven diferencias mayores al ver diferentes ventanas retrospectivas&quot;.


En otras palabras, las **ventanas retrospectivas** determinan el período de tiempo durante el cual se consideran las *conversiones* y proporcionan *contexto* al análisis de atribución. ***Adobe Analytics*** ofrece tres tipos de **ventanas retrospectivas**:

- **Ventana retrospectiva de visita:** Revisa al principio de una ***visita*** cuando se produjo una conversión, proporcionando información sobre las interacciones inmediatas que llevaron a conversiones.

  Recuerde que esta es normalmente la **ventana retrospectiva** más corta de usar.
- **Ventana retrospectiva de visitantes:** Busca todas las ***visitas*** hasta el primer día del mes dentro del **intervalo de fechas** seleccionado, ofreciendo una vista mucho más amplia de las interacciones del cliente y ayudando a identificar patrones a lo largo del tiempo.
- **Ventana retrospectiva personalizada:** Le permite expandir la **ventana de atribución** más allá del **intervalo de fechas** del informe hasta un *máximo* de **90 días**.  Proporciona *flexibilidad* para capturar los puntos de contacto que se produjeron *fuera* del **intervalo de fechas** seleccionado, lo que garantiza un análisis exhaustivo.

Al ajustar una **ventana retrospectiva** determinada, los analistas pueden examinar el impacto de uno o más puntos de contacto en lapsos de tiempo específicos y obtener una mayor perspectiva sobre cómo las diferentes duraciones afectan los resultados de atribución.

## **Reuniéndolo todo**

Entonces, ¿qué significa todo esto para nosotros como analistas?

El **panel de atribución** y la **ventana retrospectiva** nos permiten ver más allá de los datos mundanos de nivel de superficie y profundizar en el recorrido del cliente. Si entendemos qué puntos de contacto tuvieron el mayor impacto en *conversiones*, podemos tomar decisiones informadas sobre nuestras estrategias de marketing y asignar recursos de manera más eficaz.

Recuerde, después de seleccionar los **modelos de atribución** y **ventanas retroactivas**, podrá manipular aún más los datos filtrándolos con un ❺ **segmento,** o cualquier otro componente que desee en este momento.  Además, una vez procesado el panel, tendrá a su disposición todas las funciones de un Workspace tradicional.

## **Por último, poniéndolo en práctica**

Ahora que tiene los conceptos básicos, imagine que está ejecutando una campaña de marketing y trata de determinar qué canal es el *más efectivo* para generar conversiones. Con la ayuda del **panel de atribución**, no solo puedes ver el **último contacto**, sino también el **primer contacto**, **mismo contacto** y cualquier otro **modelo** que elijas para determinar qué **canales** son los *más efectivos* para dirigir tus *conversiones*. Entonces, esta información se puede usar para *optimizar* tus campañas y mejorar el rendimiento general simplemente devolviendo el reloj con la **ventana retrospectiva** de tu elección.

Ahora que ha visto lo que puede hacer, no se deje engañar ni intimidar por las características aparentemente complejas del panel de atribución.  **Acéptalo**.  *Abrazarlo*.  **Comprenderlo**.
PERO SOBRE TODO - *Úsalo a tu favor.* El **panel de atribución** y la **ventana retrospectiva** son claves para desbloquear una comprensión más profunda de sus clientes y su recorrido con su marca.

Ahora, podemos viajar &quot;[atrás en el tiempo](https://youtu.be/gVryJmZNFdU)&quot; con confianza y usar la potencia de nuestra confiable máquina del tiempo (también conocida como ***Adobe Analytics***) para tomar decisiones basadas en datos.

## Autor

Este documento fue escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, gerente de análisis digital en Kroger Personal Finance

Campeona de Adobe Analytics
