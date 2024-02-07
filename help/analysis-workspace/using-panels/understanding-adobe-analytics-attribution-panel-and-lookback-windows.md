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

Cuando pensé por primera vez en el [panel de atribución](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) y **ventana retrospectiva**, inmediatamente se me recordó el concepto de &#39;*viaje en el tiempo&#39;*; entonces, por supuesto, también me recordaron que nuestra respuesta típica a muchas herramientas nuevas como estas es simplemente dejar de intentar usarlas, porque se ven muy complicadas.

Honestamente, miren todas esas opciones, interruptores, paneles, lecturas y botones.  Y en serio, hablemos de esas complicadas luces parpadeantes, mangueras, medidores... ESPERA!!  No es el momento de distraernos hablando de máquinas del tiempo, simplemente no tenemos tiempo... ¿o sí?

Admitiré el... **panel de atribución** es una herramienta bastante compleja; sin embargo, nuestro trabajo típico como analistas, día tras día, es usar otra de nuestras herramientas favoritas y altamente complejas para también echar un vistazo a lo que sucedió en el pasado. Esa herramienta se llama ***Adobe Analytics***!  Así que sí, para responder a nuestra muy relevante pregunta, creo que estas dos cosas dicen que tenemos mucho tiempo.

Por lo tanto, ¿por qué deberíamos permitir que algo como un poco de miedo se interponga en el camino de herramientas tan asombrosas, sofisticadas y poderosas como estas que literalmente nos permiten mirar *atrasado* a tiempo, todos y cada uno de los días?

Después de todo - esto es VIAJE EN EL TIEMPO, amigos!!  Estamos hablando de ese tipo de cosas.  Correcto???!!

Entonces, ¿qué estamos esperando - un coche de metal brillante, una caja de policía, o una cabina telefónica vintage utilizando el cableado de un paraguas viejo como su antena para aparecer en nuestra puerta?

¡No!  Tenemos algo aún mejor, así que vamos a atarnos y aguantar!

Bueno... se te ocurre la idea.


Ahora que todos estamos entusiasmados con el viaje en el tiempo, vamos a respirar profundamente, retroceder un poco, establecer lo que el **panel de atribución** *de verdad* es, y desglosar un poco las cosas:

![Atribución](assets/attribution.png)

*Figura 1: Los números mostrados están alineados con el texto más abajo*

Entrada **atribución**, simplemente considere cómo los eventos/acciones pueden ser causados por un individuo, varios individuos o uno de cualquier número de eventos diferentes a lo largo del tiempo.

Según [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *atribución* permite a los analistas personalizar el modo *Dimension* los elementos reciben crédito por *eventos de éxito*.


>[!WARNING]
>
>**Modelos de atribución** se asocian con tanta frecuencia con **canales de marketing** que yo a propósito *tachado* ❷ CANAL en la imagen anterior para ilustrar que es posible realizar **atribución** análisis frente a casi cualquier otro ***dimensión***.


De hecho, rara vez un recorrido determinado del cliente es verdaderamente lineal y con menor frecuencia aún predecible.  Además, cada cliente seguirá su propio ritmo; a menudo, puede duplicarse, paralizarse, abandonarse o participar en otro comportamiento no lineal. Estas acciones orgánicas hacen que sea difícil o prácticamente imposible conocer el impacto de los esfuerzos de marketing en todo el recorrido del cliente. También obstaculiza los esfuerzos por unir múltiples canales de datos.

Eso es correcto.  Deje sus analogías de &quot;dominó&quot; en la puerta y abra sus mentes a conceptos más a lo largo de las líneas del efecto mariposa y la teoría de cuerdas - pero como todo lo demás, necesitamos comenzar con algunos de los conceptos básicos.

## **Modelos de atribución**

Cuando usamos el **panel de atribución** Sin embargo, podemos empezar a observar varias cosas diferentes.  Por ejemplo, la variable **modelos de atribución** demuéstrenos cómo nuestros *conversiones* (es decir, ❶ **métricas de éxito**) puede distribuirse entre *visitas* en cualquier grupo determinado.

En pocas palabras, si **10 personas** pulse a **BOTÓN ROJO GRANDE** para atravesar una puerta, nuestro **modelos de atribución** Nos van a decir cuál de ellos **10 personas** queremos asignar &quot;crédito&quot; - o mejor dicho, cómo *mucho* &quot;crédito&quot; que queremos asignarles - por pulsar dicho botón.

![Botón](assets/button.png)

Teniendo esto en cuenta, aquí hay algunos ejemplos de cómo ❸ **modelos de atribución** podría afectar a esos **10 personas**:

- **Primer contacto**: Este modelo funciona exactamente como suena al dar **100% de crédito** a la *primero* la persona que entró por la puerta.  Los especialistas en marketing son más propensos a utilizar este enfoque para tácticas como ***medios sociales*** o ***exhibición***; sin embargo, también es una buena táctica para utilizar a menudo para la eficacia de recomendaciones de productos en el sitio.
- **Último contacto**: Esta táctica también funciona exactamente como suena, pero en su lugar da **100% de crédito** a la ÚLTIMA persona que entró por la puerta.  Este modelo se utiliza generalmente para analizar cosas como ***búsqueda natural (orgánica)*** y otros *a corto plazo* campañas del ciclo de marketing.
- **Lineal**: Este modelo distribuye el crédito igual entre CADA PERSONA QUE entró por la puerta.

  >[!CAUTION]
  >
  >Sin embargo, se recomienda tener cuidado aquí, ya que tiene el potencial de propagar sus resultados muy finos muy rápidamente al aplicar esta táctica, teniendo en cuenta cuanto más tiempo se ejecuta y mayor es la audiencia a la que llega.

- **Forma de U**: este enfoque asigna **40 %** del crédito a la *primera persona* en la puerta, se extiende **20 %** del crédito entre *todos los que están en el medio* y, a continuación, proporciona **40 %** a la **último** mediante. Este modelo se utilizará con mayor frecuencia en situaciones en las que tiene un **largo ciclo de conversión/ventas** conteniendo *varios puntos de contacto* en el camino.  En este caso, el objetivo es resaltar principalmente la variable ***primero*** y ***último*** tácticas de marketing que contribuyeron a la conversión del cliente.
- **J**-**Forma** y **J inversa**:
   - Piense en **Forma de U**, pero en su lugar este modelo asigna **60 %** crédito a la *última persona* caminando por la puerta, **20 %** a la *primero*, y luego *desdoblamientos* el resto **20 %** horizontal *todos los demás* en el medio.  **J inversa** hace exactamente lo contrario.

     El objetivo aquí es poner la mayor parte de su énfasis, ya sea en el *principio* o el *fin* de su campaña; sin embargo, todavía desea asignar una cierta cantidad de crédito al elemento que contribuye en el extremo opuesto, al tiempo que reconoce a los &quot;chicos pequeños&quot; en el camino.

- **Deterioro de tiempo**: Ahora, sería negligente si no compartiera esta. Este modelo tiene literalmente una vida media que decae exponencialmente - ¡con el tiempo!  En este caso, la variable *predeterminado* El parámetro para la semivida de este modelo es **7 días**.  La forma en que funciona es aplicar *peso* a cada uno **canal de marketing**, *en función del tiempo* que pasa después de *punto de contacto inicial* y cuando el cliente convierta.

  **Deterioro de tiempo** y **Modelos de atribución en forma de U** Ambos suelen utilizarse para medir campañas a más largo plazo, pero como puede ver, tienen objetivos ligeramente diferentes, según la forma en que se realicen *pesar* el valor del resultado.

- **Personalizado**: Usted elige y elige quién va a obtener crédito.  ¡Es tu campaña!

Para obtener información adicional sobre estos y otros modelos de atribución, [haga clic aquí](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

Para hacer esto aún más interesante, ¡hablemos de volver atrás el reloj!

## **Ventanas retroactivas**

Ahora es el momento de empezar a llevar tu mente al siguiente nivel.  Aquí es donde literalmente agregamos el elemento de viaje en el tiempo a nuestro análisis -y nuevamente, estamos empezando con lo básico.

***Adobe*** define ❹ **ventanas retrospectivas** como &quot;la cantidad de tiempo que una conversión debe devolverse hacia atrás para incluir los puntos de contacto. Los modelos de atribución que dan más crédito a las primeras interacciones ven diferencias mayores al ver diferentes ventanas retrospectivas&quot;.


En otras palabras, **ventanas retrospectivas** determinar el período de tiempo durante el cual *conversiones* se tienen en cuenta y proporcionan *contexto* al análisis de atribución. ***Adobe Analytics*** ofrece tres tipos de **ventanas retrospectivas**:

- **Ventana retrospectiva de visita:** Se remonta al principio de un ***visita*** cuando se produce una conversión, se proporciona información sobre las interacciones inmediatas que llevan a las conversiones.

  Recuerde que este suele ser el más corto **ventana retrospectiva** para usar.
- **Ventana retrospectiva de visitantes:** Se parece a todo ***visitas*** realizar una copia de seguridad hasta el primer día del mes dentro del **intervalo de fecha**, que ofrece una vista mucho más amplia de las interacciones del cliente y ayuda a identificar patrones a lo largo del tiempo.
- **Ventana retrospectiva personalizada:** Permite expandir el **ventana de atribución** más allá de los informes **intervalo de fecha** hasta un *maximum* de **90 días**.  Proporciona lo siguiente *flexibilidad* al capturar los puntos de contacto que se produjeron *exterior* el seleccionado **intervalo de fecha**, lo que garantiza un análisis exhaustivo.

Ajustando un determinado **ventana retrospectiva** Por lo tanto, los analistas pueden examinar el impacto de uno o más puntos de contacto dentro de marcos de tiempo específicos y obtener una mayor perspectiva sobre cómo las diferentes duraciones afectan a los resultados de atribución.

## **Para juntar todo**

Entonces, ¿qué significa todo esto para nosotros como analistas?

El **panel de atribución** y **ventana retrospectiva** danos el poder de mirar más allá de los datos mundanos y superficiales, y profundizar en el recorrido del cliente. Al comprender qué puntos de contacto tuvieron el mayor impacto en *conversiones*, podemos tomar decisiones informadas sobre nuestras estrategias de marketing y asignar recursos de forma más eficaz.

Recuerde, después de que tenga su **modelos de atribución** y **ventanas retrospectivas** seleccionados, aún puede manipular aún más los datos filtrándolos con una ❺ **segmento,** o cualquier otro componente que desee en este momento.  Además, una vez procesado el panel, tendrá a su disposición toda la funcionalidad de un espacio de trabajo tradicional.

## **Finalmente ponerlo en práctica**

Ahora que tiene los conceptos básicos, imagine que está ejecutando una campaña de marketing e intentando determinar qué canal es el *más eficaz* para generar conversiones. Con la ayuda del **panel de atribución**, no solo puede ver el **último contacto**, pero también el **primer contacto**, **mismo contacto**, y cualquier otro **model** usted decide determinar qué **canales** son las *más eficaz* al conducir su *conversiones*. A continuación, esta información se puede utilizar para *optimizar* sus campañas y mejore el rendimiento general simplemente retrasando el reloj con la **ventana retrospectiva** de su elección!

Ahora que ha visto lo que puede hacer, no se deje engañar ni intimidar por las características aparentemente complejas del panel de atribución.  **Afróntalo.**.  *Abrazo* it.  **Comprender** it.
PERO SOBRE TODO - *Úsalo a tu favor.* El **panel de atribución** y **ventana retrospectiva** son la clave para comprender mejor a sus clientes y su recorrido con su marca.

Ahora, podemos viajar &quot;[atrás en el tiempo](https://youtu.be/gVryJmZNFdU)&quot; con confianza y usar el poder de nuestra máquina del tiempo confiable (también conocida como ***Adobe Analytics***) para tomar decisiones basadas en datos.

## Autor

Este documento fue escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Responsable, Análisis digital en Kroger Personal Finance

Campeona de Adobe Analytics
