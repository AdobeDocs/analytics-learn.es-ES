---
title: Lleve el análisis de datos al siguiente nivel con Métricas calculadas
description: Conozca cómo un experto homólogo utiliza las métricas calculadas para crear nuevas métricas sin cambiar su implementación y utilizando los datos ya recopilados para ayudar a responder preguntas comerciales complejas.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
source-git-commit: c64f2fde1b91edd9f3d6c0f87aa889ed2c613d9b
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 1%

---


# Lleve el análisis de datos al siguiente nivel con Métricas calculadas

La mayoría de los usuarios nuevos de Adobe Analytics están familiarizados con los segmentos como una forma de cortar y fragmentar sus datos. Hoy, quiero presentarles las métricas calculadas, la siguiente mejor herramienta de su caja de herramientas de analistas.

Como característica avanzada de Adobe Analytics, las métricas calculadas le permiten crear métricas nuevas sin cambiar la implementación con los datos que ya ha recopilado. El Creador de métricas calculadas puede utilizar muchas funciones matemáticas y estadísticas diferentes, por lo que puede crear métricas que respondan incluso a las preguntas comerciales más complejas.

## Introducción a las métricas calculadas

Para comenzar con las métricas calculadas, veamos un ejemplo sencillo. Imagine que desea comprender si los usuarios de autoservicio en línea tienen un valor de pedido promedio (AOV) mayor que los usuarios asistidos por llamadas. Para crear una métrica calculada que responda a esta pregunta, haga lo siguiente:

Para abrir el Creador de métricas calculadas, utilice la navegación superior para hacer clic en → **Componentes** → **Métricas calculadas** → **+ Agregar.** O bien, puede hacer clic en el botón **Signo +** above **Métricas** en el panel Componentes .


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descripciones a continuación de los elementos de la interfaz de usuario*

Una vez que se abra el Creador de métricas calculadas, agregue o haga lo siguiente:

**A.** Un nombre para la métrica calculada. Este nombre se muestra en la lista de componentes de métricas, así que asegúrese de que sea algo que quede claro para usted y para otros, como *AOV del centro de llamadas*.

**B.** Descripción de la métrica calculada. Esta descripción aparece cuando los usuarios hacen clic en el botón **i**&#39; al lado de la métrica en la lista de componentes, asegúrese de que sea informativa. Por ejemplo, para el centro de llamadas AOV, podríamos añadir *Calcula la AOV para los pedidos asistidos del centro de llamadas*.

**C.** El formato de la métrica: Elija decimal, tiempo, porcentaje o moneda, y agregue lugares decimales y polaridad. Aquí, elegiremos *Moneda para el formato, 0 para el número de decimales y* ⬆ *Bueno (verde) para la polaridad.*

**D**. Si está usando etiquetas, que le permiten aplicar temas y localizar rápidamente métricas calculadas, agregue las etiquetas aplicables aquí. Hemos añadido *AOV* y *Centro de llamadas* etiquetas.

**E.** Esta sección es para visualización : a medida que crea la métrica calculada en la sección F, la fórmula se muestra aquí.

**F.** Aquí, puede arrastrar y soltar dimensiones (H), métricas (I) o segmentos (J) para crear su métrica calculada, así como los operadores para la fórmula. Para cada métrica, si hace clic en la rueda de engranaje, puede cambiar el Tipo de métrica (Estándar/Total) y el Modelo de atribución. *Arrastraremos y soltaremos los ingresos del centro de llamadas, y debajo de eso,*÷ ￼*. Aceptaremos el tipo de métrica predeterminado y el modelo de atribución.*

**G**. Utilice esta **+Añadir** para agregar condiciones adicionales o números estáticos, que no necesitamos aquí.

**K.** Y por último, a medida que crea su cálculo, puede obtener una vista previa de los datos de los últimos 90 días aquí.

Ahora que hemos creado Call Center AOV, también necesitamos una métrica calculada para AOV en línea. Haríamos esto siguiendo los mismos pasos descritos anteriormente.

A continuación, podemos crear una tercera métrica calculada, ya sea mediante el Creador de métricas calculadas o sobre la marcha desde la tabla de forma libre, para comparar el Centro de llamadas y el AOV en línea de modo que tengamos algo así:

![Calc 05](assets/calc05.png)

En nuestro ejemplo, vemos un alza significativa cuando los compradores utilizan el centro de llamadas para ayudarles a realizar una compra. Estos datos pueden entonces informar a nuestras decisiones sobre cómo ayudar a los clientes a obtener asistencia con sus compras a través, por ejemplo, de ofertas emergentes u otras experiencias guiadas.

## Uso de segmentos en métricas calculadas

Ahora, veamos cómo podemos usar segmentos en métricas calculadas para obtener más información sobre el comportamiento de los clientes, las preferencias y las motivaciones. Con los segmentos y las métricas calculadas, podemos aprender lo suficiente sobre los clientes para mejorar su experiencia, aumentar los ingresos y mejorar la satisfacción y lealtad de los clientes.

Ya sabemos por los ejemplos de AOV anteriores que las compras asistidas por el centro de llamadas suelen tener un AOV más alto. Sin embargo, otras métricas nos indican que la mayoría de los usuarios no utilizan el centro de llamadas para compras.

Por lo tanto, ¿qué categorías de minoristas -y rutas de usuario a través de esas categorías- resultan en el AOV más alto?  Podemos averiguarlo combinando segmentos con métricas calculadas.

Para ello, primero necesitamos crear el nivel de visita *include* y *excluir* segmentos para cada categoría de producto. Incluir o excluir se determina haciendo clic en el botón **Opciones** en la esquina derecha del contenedor. El valor predeterminado es Incluir.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Una vez que hayamos creado estos segmentos, podemos crear una métrica calculada para darle la respuesta a su pregunta. Se abre el Creador de métricas calculadas y se hace lo siguiente:

1. Busque los segmentos recién creados y arrastre y suelte los que queremos usar en el área gris de la parte superior del **Definición** en la ventana Por ejemplo, si queremos crear un AOV para los usuarios que visitaron las categorías Mujer y Hombre, pero no para los Niños, podemos arrastrar y soltar estos tres segmentos en esa área: *Incluir*, *Incluir masculino* y *Excluir niño*. Llamamos a esto *apilar segmentos*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. A continuación, arrastramos y soltamos el **Ingresos en línea** en el mismo contenedor, luego **Pedidos en línea**. Dado que los contenedores funcionan como expresiones matemáticas para determinar el orden de las operaciones, los elementos de los contenedores se procesan antes de los procesos subsiguientes, aunque en este cálculo no hay varios contenedores o procesos.
1. Cambiamos el operador entre las dos métricas por división ().
1. Seleccionamos **Moneda** como formato, **0** lugares decimales y **UP** para la polaridad.
1. Asigne un nombre a la métrica calculada e indique una descripción.
1. Guardar.

Cuando terminamos, nuestra métrica calculada tiene este aspecto:

![Calc 10](assets/calc10.png)

Después de crear métricas calculadas usando segmentos apilados para cada combinación de recorrido de categoría del visitante y echar un vistazo a los datos, ¡observe lo que aprendemos! Los usuarios que visitan las categorías de mujeres y hombres durante su visita tienen la AOV más alta y, en comparación con los visitantes de una sola categoría, el alza es significativa:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Al saberlo, podemos optimizar el diseño de la página, las ubicaciones de los productos y los mensajes promocionales para atraer a más gente a estas categorías antes de registrarse.

## Valioso, pero no disponible en todas partes

**Por lo tanto, las métricas calculadas, simples y complejas, son muy valiosas para los analistas.**

Sin embargo, estas métricas no están disponibles en todas las áreas de Adobe Analytics. No puede utilizar métricas calculadas en:

- Secuelas en Analysis Workspace
- Análisis de cohortes en Analysis Workspace
- Data Warehouse
- Informes en tiempo real
- Informes de datos actuales
- Analytics for Target
- Report Builder

## Prácticas recomendadas de métricas calculadas

Ahora que sabe cuán valiosas pueden ser las métricas calculadas, veamos algunas prácticas recomendadas para crearlas.

1. **Compruebe la sintaxis de la fórmula.** Asegúrese de que la sintaxis de la fórmula sea correcta y siga la sintaxis de Adobe Analytics para asegurarse de que obtiene información relevante.
1. **Compruebe el orden de las operaciones.** Asegúrese de utilizar los contenedores con cuidado y ponga las cosas en el orden matemático correcto de las operaciones.
1. **No contar dos veces los datos**. Para evitar los datos de recuento doble, asegúrese de que la fórmula utilizada en la métrica calculada no cuente los mismos datos varias veces. Esto se consigue a menudo combinando *Incluir* y *Excluir* condiciones en la métrica calculada o mediante el uso de segmentos.
1. **Compruebe la granularidad de la hora.** Asegúrese de que la métrica calculada tenga la misma granularidad de tiempo que las métricas de origen utilizadas en la fórmula.
1. **Use datos precisos:** Solo obtendrá resultados valiosos si utiliza datos precisos y fiables en el cálculo.

## Prácticas recomendadas para segmentos personalizados

Al crear segmentos en Adobe Analytics, tenga en cuenta estas prácticas recomendadas:

1. **Manténgalo simple.** Evite complicar demasiado el segmento. Manténgalo lo más sencillo posible y utilice solamente las condiciones necesarias para garantizar la precisión.
1. **Usar los tipos de contenedor correctos**. Asegúrese de utilizar el tipo de contenedor correcto (visitante, visita o visita individual) en la definición del segmento para evitar obtener resultados incorrectos.
1. **No contar dos veces los datos**. Al igual que con las métricas calculadas, asegúrese de que el segmento no cuente los mismos datos varias veces. Los contenedores de inclusión y exclusión pueden ayudar.
   1. Cuando se utiliza un contenedor de inclusión, *incluye* *todo el contenido de la visita* si alguna visita individual coincide con la condición dentro de la visita.
   1. Cuando se utiliza un contenedor de exclusión, *excluye todo el contenido de la visita* si alguna visita individual coincide con la condición dentro de la visita.
1. **Anidar contenedores correctamente**. Determine qué datos se incluyen utilizando el contenedor exterior y, a continuación, aplique reglas anidadas a los datos restantes. A medida que se aplican las reglas anidadas, el flujo de segmentos actúa como un canal y las reglas posteriores no se aplican a ninguna visita individual excluida por la primera regla.
1. **Asegúrese de que los datos estén actualizados.** Asegúrese de utilizar datos precisos y actualizados en la definición del segmento para obtener resultados precisos.
1. **Pruebe el segmento.** Pruebe siempre el segmento para asegurarse de que funciona según lo previsto antes de publicarlo para otros usuarios.
1. **Consideremos el rendimiento.** Los segmentos pueden ralentizar el procesamiento de los informes, por lo que tenga en cuenta su impacto al crearlos.

## Principales conclusiones

La combinación de segmentos y métricas calculadas en Adobe Analytics puede llevar absolutamente a un análisis de datos más robusto y efectivo. Al dividir y editar sus datos y crear cálculos para comparar, puede obtener perspectivas más profundas sobre el comportamiento del cliente que puede utilizar para optimizar sus campañas de marketing y crear paneles e informes personalizados. Sin embargo, recuerde que las métricas calculadas no están disponibles en todas las áreas de Adobe Analytics y asegúrese de seguir las prácticas recomendadas para garantizar que obtiene datos precisos y útiles.


## Autor

Este documento fue escrito por:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, administrador sénior de Adobe Analytics en Adswerve

![Adobe](assets/calc14.png)
