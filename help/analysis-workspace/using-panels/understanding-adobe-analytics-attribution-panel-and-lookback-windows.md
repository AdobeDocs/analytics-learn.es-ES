---
title: Explicación del panel Atribución de Adobe Analytics y las ventanas de retrospectiva
description: Aprenda a utilizar el panel Atribución y la ventana de retrospectiva para comprender el comportamiento del cliente y personalizar cómo los elementos de dimensión obtienen crédito por los eventos de éxito.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: 5d20da6a06c9395f56bccbc97ba1d7fb8bb49ff8
workflow-type: tm+mt
source-wordcount: '1883'
ht-degree: 2%

---


# Explicación del panel Atribución de Adobe Analytics y las ventanas de retrospectiva

Aprenda a utilizar el panel Atribución y la ventana de retrospectiva para comprender el comportamiento del cliente y personalizar cómo los elementos de dimensión obtienen crédito por los eventos de éxito.

## Uso del panel de Attribution 

![Delorean](assets/delorean.png)

&#39;¡Bueno Scott!&#39;

Tan pronto como pensé en la [Panel de Attribution](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html) y **Ventana retroactiva**, me recordó la canción &quot;Back in Time&quot; de Huey Lewis y the News; entonces, por supuesto, también me recordaron que nuestra respuesta típica a muchas herramientas nuevas como estas es simplemente dejar de tratar de usarlas, porque parecen tan complicadas.

Quiero decir, sólo miren todas esas opciones, conmutadores, paneles, lectores y mandos.  Y en serio, hablemos de ese condensador de flujo.  Espera, ¿acabo de decir condensador de flujo?

OK, admitiré el **Panel de Attribution** es una herramienta bastante compleja; sin embargo, nuestro trabajo típico como analistas, día tras día, es usar una herramienta muy compleja para ver lo que pasó en el pasado.  Esa herramienta se llama **Adobe Analytics**!

Por lo tanto, ¿por qué deberíamos permitir que algo como un poco de miedo se interponga en el camino de una herramienta tan poderosa y fresca que nos permita, literalmente, mirar hacia atrás en el tiempo todos los días?

Todo se trata de eso, ¿verdad?  ¡¿¿¿¿¿¿DE ACUERDO???!! (Quiero decir, vamos, estoy bastante seguro de que sigue siendo correcto y &quot;políticamente correcto&quot; llamarnos &quot;geeks&quot;?)

Ah, ¿a quién le importa?  Gear up, Geeks, Nerds, Goobers, Dweebs, and Techies (sí, incluso los Trekkies), puedo escuchar el estéreo del auto ahora:

&quot;¡Así que llévame, no me importa!  Pero es mejor que me prometas... ¡VOLVERÉ A HACER TIEMPO!&quot;

Ahora tengo tu atención, ¿verdad?  ¡bueno!


Descompongamos un poco las cosas.  Ahora que estamos todos emocionados **viaje de tiempo**, vamos a dar un paso atrás y establecer cuál es la variable **Panel de Attribution** realmente es:

![Control de tiempo](assets/time-control.gif)

No, no, no, no.  Todavía no nos distraigamos.  Tal vez, intentemos eso de nuevo:

![Ventana Atribución](assets/attribution-window.png)

En **Atribución**, simplemente considere cómo los eventos/acciones pueden ser causados por un individuo, varias personas, o una o varias cosas diferentes a lo largo del tiempo.

Según [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/attribution.html), la atribución permite a los analistas personalizar la forma en que los elementos de dimensión obtienen crédito por los eventos de éxito.  De hecho, ningún recorrido de cliente dado es nunca verdaderamente lineal y es menos predecible a menudo.  Moreso, cada cliente procederá a su propio ritmo; a menudo pueden duplicar, paralizar, abandonar o participar en otro comportamiento no lineal. Estas acciones orgánicas hacen que sea difícil o prácticamente imposible conocer el impacto de los esfuerzos de marketing en el recorrido del cliente. También obstaculiza los esfuerzos por unir múltiples canales de datos.

¿Te suena familiar algo de esto?  Piénsenlo en el contexto del recorrido de Marty McFly:

![Volver al futuro 1](assets/back-to-the-future1.png)![Volver al futuro 2](assets/back-to-the-future2.png)

Desde el momento en que huyó del estacionamiento del centro comercial Twin Pines hasta cuando literalmente se echó del DeLorean antes de que fuera borrado por una locomotora de 210 toneladas parece lejos de ser lineal, y no es nada que nadie hubiera podido predecir.

Sin embargo, a través del poder de la magia cinematográfica, podemos seguir el camino de Marty a través del tiempo y entender todos sus puntos de contacto, sus puestos, dobles espaldas y deserciones.

## Modelos de atribución

En la vida real, podemos usar el **Panel de Attribution** para ver varias cosas diferentes.  Por ejemplo, la variable **Modelos de atribución** mostrarnos cómo **conversiones** se distribuyen entre **visitas** en cualquier grupo en particular.

En pocas palabras, si 10 personas presionan un botón para atravesar una puerta, nuestros Modelos de Atribución nos dirán cuál de esas 10 personas queremos dar el crédito por presionar ese botón.  Con esto en mente, aquí hay algunos ejemplos de cómo los modelos de atribución podrían afectar a esas 10 personas:
* **Primer toque**: Esta es exactamente como suena.  En este caso, da 100% de crédito a la primera persona que caminó por la puerta.  Para esto, es más probable que los especialistas en marketing usen esto para tácticas como Social o Mostrar, pero a menudo es una buena táctica para la efectividad de recomendaciones de productos en el sitio.
* **Último toque**: También como suena.   Este modelo da 100% de crédito a la última persona que entró por la puerta.  Este modelo se utiliza a menudo para analizar elementos como la búsqueda y campañas de ciclo de marketing a corto plazo.
* **Lineal**: Esto da igual crédito a cada persona que caminó por la puerta.  Así es - tienes un DeLorean, y tienes un DeLorean, y obtienes un DeLorean.  ¡¡¡TODO EL MUNDO TIENE UN DELOREANO!!!
* **Forma de U**: Este da el 40% del crédito al primero de la puerta, distribuye el 20% del crédito a todos los que están entre medias y luego da el 40% al último.  Piense en una situación en la que desee reconocer las conversiones mayoritarias tanto en el front-end como en el back-end, pero también desee rociar una pequeña cantidad de crédito en algunas de las interacciones de contribución intermedias.
* **Deterioro de tiempo**: Sería negligente si no compartiera esta con ustedes antes de enviarles a la documentación oficial para revisar los modelos restantes.  Como el plutonio de Doc Brown, este modelo literalmente tiene una vida media que se desciende exponencialmente.  En este caso, el parámetro predeterminado para la semivida de este modelo es de 7 días.  La forma en que funciona es aplicar peso a cada canal de marketing, en función de la cantidad de tiempo que transcurra después del punto de contacto inicial y de cuándo el cliente se convierte.

Para obtener información adicional sobre esto y el resto de **Modelos de atribución**, [haga clic aquí](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=es).

Para que esto sea aún más interesante, hablemos del **Ventanas retroactivas**.

Sí, aquí vamos - ¡¡VUELVAN EN EL TIEMPO!!  ¡Porque aquí es donde comienza la diversión!

Adobe define **Ventanas retroactivas** como &quot;la cantidad de tiempo que una conversión debe mirar hacia atrás para incluir puntos de contacto. Los modelos de atribución que dan más crédito a las primeras interacciones ven diferencias mayores al tener ventanas retrospectivas distintas.&quot;

* **Ventana retrospectiva de visita**: Busca hasta el principio de una visita cuando se produjo una conversión
* **Ventana retrospectiva de visitante**: Busca todas las visitas hasta el primer día del mes del intervalo de fechas actual.
* **Ventana retrospectiva personalizada**: Permite expandir la ventana de atribución más allá del intervalo de fechas del informe hasta un máximo de **90 días**.

Si han visto TODAS las películas de Back to the Future, entonces saben que Marty McFly regresó en el tiempo más de una vez, y también saben que regresó a 1955 más de una vez.  Si nos apoyamos en la adquisición de &quot;Gray&#39;s Sports Almanac&quot; como nuestro evento de conversión, consideremos lo siguiente:

![Almanaque deportivo](assets/sports-almanac.png)

1. Un poco antes **1:30 a.m.** en **26 de octubre de 1985**, Marty McFly regresa en el tiempo a **5 de noviembre de 1955**, donde corre por primera vez sobre un pinar en un viejo DeLorean.  A lo largo de la semana y media siguiente, interactúa con varias personas, incluidos sus padres, afectando en última instancia al futuro al influir en su padre para que se enfrente a un matón llamado Biff, para que su padre pueda realizar su propio potencial para convertirse en un autor exitoso de ciencia ficción.
1. Más tarde esa misma mañana el **26 de octubre de 1985**, el doctor Emmett Brown llega a la carretera de Marty McFly para informarle a él y a su novia que algo ha salido terriblemente mal con sus hijos y deben correr hacia el futuro para arreglar sus problemas.  Mientras se van, su partida es presenciada por Biff, que encuentra extraño ver a un volador DeLorean.  Más tarde, en el futuro, mientras Biff vuelve a ser testigo de un volante DeLorean e incluso después ve &quot;dos versiones&quot; de Marty, comienza a juntar cosas.   Cuando escucha a Doc Brown y Marty argumentando cómo la &quot;máquina del tiempo&quot; nunca debería ser usada para beneficio personal y solamente para investigación (porque Marty había estado discutiendo acerca de tomar un almanaque deportivo de vuelta al pasado para hacer algunas apuestas personales), Biff roba la máquina del tiempo mientras que los dos están distraídos para entregar el almanaque deportivo a su yo más joven en el pasado.
1. Después de su viaje al futuro, Doc Brown y Marty regresan a un **26 de octubre de 1985** no reconocen, y deducen la línea de tiempo ha sido alterada por un malvado Biff.  Al darse cuenta que deben arreglar lo que pasó, Doc y Marty deciden regresar a **12 de noviembre de 1955**, la fatídica noche en que todo cambió por Marty cuando visitó por primera vez **1955**.  Doc y Marty finalmente salvaron el día robando el almanaque deportivo que Old Biff del futuro entregó a Young Biff en **1955**, pero no sin otro giro, realmente necesitas ver la trilogía completa de las películas para realmente disfrutar y entender.

Dependiendo de nuestra **Modelo de atribución** y **Ventana retroactiva**, podemos terminar con algunos escenarios interesantes:

* Uso **primer contacto** y **ventana retrospectiva de visita**, atribución mira la visita de Marty donde ocurrió la más reciente &quot;conversión&quot;, que es cuando él y Doc logran robar el almanaque deportivo de Young Biff y mantener su aversión al estiércol.

![Biff 1](assets/biff1.png)![Biff 2](assets/biff2.png)

* Créelo o no, usando **primer contacto** y **ventana retrospectiva de visitante**, la atribución favorecería la conversión donde finalmente gana Biff.
* Aplicación de un **ventana retrospectiva lineal** resultaría en un multiverso donde cada línea de tiempo existe.  Lo siento, esto no es **Marvel** o **Star Trek**!

Y en este punto, espero que estén empezando a tener la idea.

Entonces, ¿qué significa todo esto para nosotros como analistas?

La variable **Panel de Attribution** y **Ventana retroactiva** nos da el poder de mirar más allá de los datos simples y superficiales y profundizar en el recorrido del cliente. Al comprender qué puntos de contacto tuvieron el impacto bueno en las conversiones, podemos tomar decisiones informadas sobre nuestras estrategias de marketing y asignar recursos de manera más efectiva.

Recuerde, después de tener su **Modelos de atribución** y **Ventanas retroactivas** seleccionado, aún tiene la capacidad de manipular aún más los datos filtrándolos con un segmento o con cualquier otro componente que desee.  Además, una vez que se haya presentado el Panel, tendrá toda la funcionalidad de una **Espacio de trabajo**, lo que significa que tienes licencia oficial para conducir 88 mph!

## Finalmente, ponerlo en práctica

Ahora que ya tiene los conceptos, imaginen que está ejecutando una campaña de marketing e intentando determinar qué canal es el más efectivo para generar conversiones. Con la ayuda de **Panel de Attribution**, puede ver no solo el **Último toque**, pero también el **Primer toque**, **Mismo contacto**, y cualquier otro modelo que elija, para determinar qué canales son los más efectivos en la generación de conversiones. A continuación, esta información se puede utilizar para optimizar las campañas y mejorar el rendimiento general.

Ahora que han visto lo que pueden hacer, no se dejen intimidar por las características aparentemente complejas del **Panel de Attribution**.  **Cara** es así.  **Abrazo** es así.  **Comprender** es así.  Sobre todo, utilícelo en su beneficio. La variable **Panel de Attribution** y **Ventana retroactiva** son las claves para desbloquear una comprensión más profunda de sus clientes y su recorrido con su marca.

Ahora, podemos viajar &quot;de vuelta en el tiempo&quot; con confianza y usar el poder de nuestra máquina del tiempo de confianza (también conocida como,  **Adobe Analytics**) para tomar decisiones basadas en datos; y, lo más importante, recuerden, &quot;¡A dónde vamos, no necesitamos carreteras!&quot; (Sólo un condensador de flujo, ¡y un ojo activo para la atribución!)

![Volver al futuro](assets/back-to-the-future3.png)

## Autor

Este documento fue escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, administrador, análisis digital en Kroger Personal Finance

Campeona de Adobe Analytics
