---
title: Una guía completa para la transición a Adobe Analytics desde Google Analytics
description: Uno de los mayores desafíos en la transición entre cualquier herramienta es aprender dónde encontrar una funcionalidad equivalente y utilizarla de manera eficiente. Esta discusión forma parte de una guía más amplia para ayudar a los usuarios a realizar la transición a Adobe Analytics con mayor facilidad.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: de78868e07b0fa59a7babc092c463bbe4d8e2da7
workflow-type: tm+mt
source-wordcount: '3690'
ht-degree: 96%

---

# Una guía completa para la transición a Adobe Analytics desde Google Analytics

## 1. Introducción

Uno de los mayores desafíos en la transición entre cualquier herramienta es aprender dónde encontrar una funcionalidad equivalente y utilizarla de manera eficiente. Este debate forma parte de una guía más amplia para ayudar a los usuarios a realizar la transición a Adobe Analytics (como nuevo usuario o como proveniente de Google Analytics) con mayor facilidad. Se proporciona una comparación detallada con GA, como herramienta con la que es más probable que la mayoría de los usuarios estén familiarizados, para ayudarlos a correlacionar los conocimientos existentes con el nuevo conjunto de herramientas. Aunque no hay sustituto para la práctica, esto le ayudará a empezar y, con suerte, reducirá las frustraciones que pueda sentir durante esta etapa (o incluso puede servirle de repaso una vez que comience a ponerse al día).

También deberíamos hacer una rápida comparación terminológica:

| **Descripción** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Se ha visto una métrica de evento que representa una página (o pantalla de una aplicación). | Vista de páginas | Pageview |
| Una métrica que representa un grupo de interacciones en su sitio web o aplicación que se producen en el mismo lapso de tiempo | Visita | Sesión |
| Una métrica que define un dispositivo identificado (en función de varios criterios, incluidas las cookies y otros patrones de comportamiento, para unir información del usuario) | Visitante único | Usuario |

## 2. Las interfaces

Una de las cosas que veo más a menudo cuando la gente compara Adobe Analytics y Google Analytics es que Adobe tiene muchas cosas; es abrumador para la gente. Esto es cierto, pero, aunque no lo crea, es una fortaleza más que una debilidad. Adobe proporciona una amplia gama de herramientas y flexibilidades en la visualización de datos, lo que le permite tener mucha más libertad para construir lo que necesita.

Empecemos por ver la creación de informes “en el sitio”.

### 2.1. Creación de informes en el sitio

#### 2.1.1. Pantalla de inicio

Tanto Adobe Analytics como Google Analytics permiten personalizar la primera vista que ve un usuario cuando inicia sesión.

##### 2.1.1.1. Espacio de trabajo/Pantalla de inicio personalizada (Adobe Analytics)

Adobe Analytics no presume de crear un informe generado previamente para que todos los usuarios lo vean en el inicio de sesión. La página de inicio predeterminada lleva a la pantalla de aterrizaje del espacio de trabajo, que mostrará a cada usuario todos los informes de espacio de trabajo que ha creado o que se han compartido con él. Además, cada uno tiene la capacidad de establecer cualquiera de estos informes como su pantalla de inicio si así lo desea.

![image1](assets/ga-to-aa_1.png)

Más adelante, en esta guía, se mostrarán más detalles sobre el espacio de trabajo. Consulte la sección 2.1.2.1

>[!TIP]
>
>Cree o comparta algunos informes estándar para su organización de modo que tengan un punto de partida para ver la información sin tener que sumergirse en la creación de sus propios informes de inmediato.



##### 2.1.1.2. Perspectivas de la pantalla de inicio (Google Analytics)

* La pantalla de inicio de Google Analytics tiene algunas visualizaciones creadas previamente para usted.  Estas cubren cosas como las siguientes:
* Usuarios, Sesiones, Tasa de salida hacia otro sitio y Duración de la sesión en los últimos siete días
* Usuarios por hora del día en los últimos 30 días
* Usuarios actuales en este momento y Páginas activas principales
* Canal de tráfico, Fuente/medio y Referencias en los últimos siete días
* Sesiones por país en los últimos siete días
* Páginas principales de los últimos siete días
* Tendencia de usuarios activos de los últimos 30 días
* y más

En GA4, los usuarios tienen más opciones para personalizar y añadir sus propios informes a la pantalla de inicio.

![image2](assets/ga-to-aa_2.png)

Esto es probablemente lo que más echará de menos cuando venga a Adobe. No tiene una pantalla de inicio de este tipo que se genera previamente, pero puede configurar fácilmente un espacio de trabajo personalizado para replicar lo que necesita de lo anterior y, si lo desea, establecerlo como pantalla de aterrizaje. Más información más adelante (o consulte la sección 2.1.2.1 del espacio de trabajo de Adobe).

#### 2.1.2. Report Builder en el sitio

Además de los informes simples que proporcionan las herramientas de análisis, cada una de ellas también ofrece herramientas más potentes para crear sus propios informes personalizados.

##### 2.1.2.1. Adobe Analytics Workspace

Este es el centro de Adobe Analytics, ya que se introdujo en 2017 y se ha convertido en el lugar de referencia para el análisis de Analytics. Es la razón principal por la que la sección Informes pronto dejará de funcionar.

Esta herramienta le permite crear informes con una libertad casi completa.

El informe se puede desglosar en paneles y estos pueden contener cualquier cantidad de visualizaciones. Los paneles se pueden configurar como información común, como filtros de intervalo de fecha y de segmento comunes.

Se puede cambiar el tamaño de los paneles y las visualizaciones que los rodean, así como arrastrarlos para mostrar los elementos juntos o apilados. Si desea comparar dos grupos diferentes de datos uno al lado del otro, puede crear paneles que se dividan al 50/50 en el medio para mostrar los dos sitios en paralelo y facilitar la comparación.

Los usuarios tienen a su disposición una gran variedad de visualizaciones:

* Tabla de forma libre
* Tabla de cohortes
* Visita en orden previsto
* Flujo
* Gráficos
   * Área (apilada y sin apilar)
   * Línea
   * Dispersión
   * Barra (apilada y sin apilar)
   * Viñeta
   * Anillo
   * Histograma
   * Barra horizontal (apilada y sin apilar)
* Mapa
* Bloques de resumen
   * Cambio de resumen
   * Texto de resumen
   * Texto (campo de texto libre para introducir información adicional que proporcione contexto)
* Venn

Cada panel y visualización puede tener título y se le puede aplicar una descripción para ayudar a contextualizar lo que muestra la información.
En Adobe, los segmentos (sobre todo los filtros de datos) se aplican de forma retroactiva, y se pueden extraer en columnas de tablas de forma libre para comparar los datos en paralelo. Por ejemplo, si un usuario quisiera comparar dos categorías en el sitio para el tráfico, podría crear un segmento para la categoría A y otro para la B.

![image3](assets/ga-to-aa_3.png)

Las tablas de forma libre permiten tener varias columnas y utilizar la segmentación, según sea necesario, para visualizar los datos como desee.

A partir de lo anterior, ¿no desea ver un desglose por fecha? Basta con arrastrar y soltar otra dimensión o segmento para ver los datos de una manera diferente… como quizá usar segmentos para el tipo de dispositivo y, a continuación, añadir un desglose por sistema operativo para los usuarios de dispositivos móviles/tableta:

![image3](assets/ga-to-aa_4.png)

El espacio de trabajo le permite dejar volar su creatividad, no se limita a desgloses “estándar”. Puede crear las visualizaciones que necesita para profundizar en las comparaciones que necesita ejecutar.

>[!TIP]
>
>No tenga miedo de jugar y explorar, aquí hay muchas maneras de pensar con creatividad. ¡Vea lo que puede hacer! Pero también, asegúrese de intentar verificar que lo que ha creado realmente muestra lo que cree que es. La experiencia aquí le ayudará.

Incluso puede crear métricas calculadas sobre la marcha o segmentos que solo existan dentro del informe, con lo que evita inundar el repositorio de cálculos y segmentos. Al mismo tiempo, también se asegura de que puede generar elementos centrados que son necesarios para informes específicos, sin confundir a su organización con cosas que no son muy utilizables en otros contextos.

Esta discusión es solo una introducción a esta herramienta, habrá otras guías más completas para que se inicie, pero, cuando lo haga, podrá realizar informes completos como los siguientes:

![image3](assets/ga-to-aa_5.png)

También debe tenerse en cuenta que los espacios de trabajo no se guardan automáticamente, por lo que es más fácil hacer un único informe ad hoc sin saturar el repositorio de informes.

Otra característica potente de los espacios de trabajo es la capacidad de aplicar modificadores interactivos a los informes en forma de desplegables. Aunque estos desplegables no funcionarán en archivos CSV o PDF exportados de los informes, en el informe en directo permiten actualizar todas las visualizaciones de un panel para mostrar el mismo informe en condiciones diferentes. Se pueden utilizar varios desplegables y, siempre que las opciones no sean mutuamente excluyentes, los elementos seleccionados se apilarán para permitir presentar de forma limpia la información.

>[!IMPORTANT]
>
>Para obtener más información acerca del uso de desplegables y desgloses de forma libre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: paneles e informes personalizados y guardados

Google tiene algunas herramientas para crear informes dentro de la interfaz, pero siguen teniendo la misma visualización y las mismas limitaciones de la sección de informes.

Ahora, aquellos versados en Google Analytics que lean esto, podrían estar diciendo: “Bueno, espere un segundo, ¿qué pasa con Google Data Studio? ¿No es un mejor equivalente del espacio de trabajo de Adobe?” Sería correcto, pero, como Data Studio técnicamente no forma parte de la herramienta Analytics y permite conexiones a diferentes fuentes de datos, esta se trata más adelante en la sección Acceso ampliado a informes de esta exposición (y, en particular, en la sección 2.2.3)

Los paneles y los informes personalizados de Google le permiten agrupar varias visualizaciones en un informe, pero, a diferencia del espacio de trabajo, aún están bloqueados en correlaciones sencillas y en qué datos se pueden colocar en qué columnas.

En los informes personalizados, uno de los mayores desafíos es el hecho de que cuando crea un filtro se aplica a todas las pestañas del informe… no hay forma de comparar dos filtros diferentes dentro del mismo informe.

Para las comparaciones superficiales, cumple su función. Todos son similares a los paneles, los informes personalizados y los marcadores heredados de Adobe. Herramientas básicas proporcionadas para satisfacer sus necesidades y que residen en el grupo de informes.

#### 2.1.3. Informes

Tanto Google como Adobe tienen algunos informes navegables que son tablas creadas previamente y gráficos básicos de cronología basados en una dimensión.

##### 2.1.3.1. Informes de Adobe Analytics

Adobe Analytics también tiene una sección de Informes, aunque en general se está eliminando gradualmente en favor de Analysis Workspace (y, de hecho, se ha anunciado que la interfaz dejará de funcionar, ya que el espacio de trabajo [sección 2.1.2.1] es una herramienta mucho más potente), donde la mayoría de estas tablas se pueden crear y modificar con mayor facilidad. Las secciones de Adobe están mucho más divididas, y esto puede ser desalentador:

![image3](assets/ga-to-aa_6.png)

Como la mayoría de lo anterior es accesible a través de los espacios de trabajo, daré una breve descripción de estas secciones y cómo se relacionan con Google Analytics, y resaltaré los informes que siguen siendo relevantes.

Las métricas del sitio son lo que cabría esperar: abarcan las métricas estándar (vistas de página, visitantes únicos, visitas, así como los eventos personalizados que haya configurado). Esto es similar al informe de comportamiento de GA, pero también incluye algo de lo que encontraría en el de audiencia (ya que Adobe no divide los tipos de métricas).

Aquí también encontrará informes de “bots”. El tráfico de bots se excluye de todos los informes estándar, pero hay dos informes que le permiten ver qué está sucediendo y qué bots están entrando en su sitio. Esto es especialmente bueno si configura reglas de bots personalizadas para excluir los de spam conocidos que visitan con frecuencia el sitio. Puede obtener información sobre lo que están haciendo esos bots sin que los informes principales se inunden de ese tráfico. Actualmente, los informes de bots no están disponibles a través del espacio de trabajo (pero las nuevas funciones de creación de informes que se lanzarán próximamente también permitirán a los usuarios obtener esta información).

El contenido del sitio es una agrupación de dimensiones estándar de Adobe: Nombre de página, Secciones del sitio (canales), Jerarquías (una forma de crear informes de desglose personalizados de la organización dentro del sitio web), Servidores (esto es especialmente útil si tiene varios subdominios en el sitio o si está etiquetando varios sitios juntos en un grupo de seguimiento), etc. Todas estas opciones están disponibles en el espacio de trabajo.

Móvil es una agrupación de datos específicos de dispositivos móviles, como dispositivos, tipos de dispositivos, etc. Todas estas opciones están disponibles en el espacio de trabajo.

Las rutas son otro de los elementos “no disponibles en los espacios de trabajo”... mientras que estos sí tienen un diagrama de flujo, solo puede ver los flujos de entrada y salida de una sola página o valor... En cambio, las rutas le permiten ver las rutas más comunes utilizadas en su sitio web. De forma predeterminada, Páginas es el primer informe de ruta que se le configura, pero puede activarlo para props personalizados (por ejemplo, si rastreara un valor “Tipo de página”, podría observar las rutas dentro de los tipos de página). La otra cosa que personalmente me gusta de las Rutas es la forma sencilla en que se presenta la información... El diagrama de flujo del espacio de trabajo (dependiendo de cuánto esté tratando de ver) puede ser abrumador. Recomiendo probar ambos... cada uno tiene un uso y valor dependiendo de lo que quiera lograr. Debe tenerse en cuenta que cualquier dimensión se puede utilizar en Flujos, mientras que las Rutas deben configurarse en un prop en el panel Administración.

Los informes Fuentes de tráfico, Campañas y Canales de marketing son todos similares al informe Adquisición de Google. Fuentes de tráfico se centra en los remitentes del reenvío reales, Campañas, en los códigos de campaña y Canales de marketing, también en estos, pero además aplica una lógica adicional (según determine el usuario) sobre cómo procesar la información. Opino que Adobe proporciona mucha más libertad sobre cómo configurar las reglas, Google hace muchas cosas por usted, por lo que será un cambio en la forma de pensar. También debe tenerse en cuenta que, de forma predeterminada, la atribución de Google en los códigos de campaña es de seis meses, mientras que la de Adobe se establece de forma predeterminada en una semana. Esto puede cambiarse en la configuración de administración, pero en el espacio de trabajo puede aplicar una atribución personalizada sobre cualquier dimensión, lo que le ofrece una mayor flexibilidad sobre la marcha.

Los informes Retención de visitantes y Perfil del visitante son similares a los informes Audiencia de Google Analytics. Retención de visitantes se centra más en la frecuencia de retorno, mientras que Perfil del visitante, en la geografía y la tecnología de los usuarios.

Conversión personalizada y Tráfico personalizado son ambos informes de dimensión personalizados, y Conversiones son sus eVars. En estas, puede establecer una caducidad personalizada para el valor (es decir, visitas individuales, visitas, meses, años, etc.) y este permanecerá para ese usuario durante el tiempo especificado, a menos que se sobrescriba. Las variables de tráfico son sus props, pero también puede configurarlas para informes de rutas o como elementos de lista (que separarán varios valores según un delimitador de su elección).

Medios es para elementos como vídeos o archivos de audio en los que ha configurado un seguimiento de medios especial.

Informes personalizados es una sección en la que un usuario puede personalizar las columnas y desgloses que ha creado en la interfaz de informes y guardarlos como un informe personalizado. Sin embargo, como se ha mencionado anteriormente, dado que el espacio de trabajo permite desgloses y correlaciones mucho más potentes, cualquier personalización debería realizarse allí. Esta era una buena solución antes de que existiera el espacio de trabajo.

La sección Marcadores es similar a los Informes personalizados, donde los informes usados con frecuencia se pueden añadir como marcador en la interfaz de informes para que se puedan encontrar más fácilmente.

El tablero era un producto heredado que permitía a las personas combinar informes breves de datos en una sola visualización. Sin embargo, la funcionalidad del espacio de trabajo (sección 2.1.2.1) es mucho más fácil de usar, ya que solo existe como punto de acceso a los informes heredados que deben reconstruirse antes de que esta función se cierre.

Objetivos es un área de informe especial que permite a las personas crear un informe basado en un objetivo dentro de un intervalo de tiempo determinado, para que los equipos puedan monitorizar cosas como campañas y ver si estaban en el camino correcto para alcanzar sus objetivos de tráfico.

Todos los informes aquí permiten varias columnas de métricas y desgloses de dimensiones. No obstante, la simplicidad de las visualizaciones y parte de la lógica detrás de qué elementos podrían correlacionarse pueden ser frustrantes a veces.

##### 2.1.3.2. Informes de Google Analytics

Google Analytics divide estos informes en las siguientes secciones: Tiempo real, Audiencia, Adquisición, Comportamiento y Conversaciones (en GA3) y en Ciclo vital (con las subsecciones Adquisición, Participación, Monetización y Retención) y Usuario (con las subsecciones Demografía y Tecnología).

![image3](assets/ga-to-aa_7.png)

Puede realizar algunos ajustes menores en estas visualizaciones, añadir un desglose de dimensión secundario, cambiar la visualización, crear un filtro en los datos, etc. Puede guardar las personalizaciones como un informe guardado.

Estos le ofrecen una visión rápida y sencilla de sus datos. Sin embargo, no puede comparar cosas como usuarios con vistas de página para una página de la misma tabla y no puede añadir más de una dimensión adicional para ver datos adicionales.

Son buenos para obtener datos analíticos rápidos, pero si realmente necesita profundizar, sufren de limitaciones.

### 2.2. Acceso ampliado a los informes

Además de la Creación de informes en el sitio, la mayoría de las herramientas ofrecen una funcionalidad ampliada que le permite sacar el análisis de las herramientas y crear algo un poco más personalizado.

#### 2.2.1. Report Builder de Adobe Analytics (extensión de Microsoft Excel)

El espacio de trabajo es una buena herramienta, pero a veces es necesario poner los datos en una hoja de cálculo personalizada, posiblemente para poder unir varias fuentes de datos. Aquí es donde Report Builder entra en juego.

Report Builder es un complemento para Microsoft Excel que le permite crear conexiones con los datos de Adobe Analytics para extraer datos de tablas que puede manipular en Excel. Por lo general, para utilizarlo de forma eficaz, extraiga los datos en algunas pestañas de datos sin procesar, luego use las referencias de celdas de Excel para sacar datos de estas pestañas en un solo informe consolidado y, a continuación, cree gráficos y visualizaciones.

>[!NOTE]
>
>Report Builder tiene un permiso especial que debe aplicarse a los usuarios para acceder a este complemento. Probablemente, solo debería concederse a los usuarios que hayan aprendido a utilizar bien la herramienta.

#### 2.2.2. Conexión de la API de Adobe Analytics

Si necesita que Adobe Analytics se digiera con algo distinto a Excel, pero desea obtener los beneficios de los datos procesados (incluidas las exclusiones de reglas de bots), puede utilizar la API de Adobe para extraer datos directamente y, a continuación, procesarlos mediante script o añadirlos a una base de datos para usarlos con otro sistema.

Debe tenerse en cuenta que la API sigue extrayendo datos de correlación aplicando los desgloses y segmentos según se especifican en la solicitud de extracción.

El espacio de trabajo de Adobe (sección 2.1.2.1) utiliza realmente la API para crear todos los informes y, si activa el modo de depuración en él, le mostrará las llamadas de API exactas utilizadas. Esta es una forma rápida de crear sus llamadas a la API mediante el espacio de trabajo para crear y validar los datos que desea extraer y, después, utilizar esas llamadas a la API para sacar los datos a su propio procesamiento.


#### 2.2.3. Data Studio de Google Analytics

Si ha estado leyendo, ya sabrá que hace rato he mencionado Data Studio como el equivalente al espacio de trabajo de Adobe. Data Studio le permite extraer datos de Google Analytics, pero también de otras fuentes. Esto es bueno si desea consolidar los datos de análisis con otros datos recopilados. Con todo, en cuanto a Google Analytics, he encontrado el mismo tipo de limitaciones de visualización que están presentes en Google Analytics. La manera en que se forman las filas y columnas sigue siendo muy limitada respecto a lo que se puede hacer.

Sigue siendo una herramienta potente, y no disuadiría a la gente de usarla de ninguna manera, pero mi experiencia personal es que, habiendo usado el espacio de trabajo durante tanto tiempo, personalmente creo que el comportamiento rígido es bastante limitante.


#### 2.2.4. Extensión de hoja de cálculo de Google

Para mis propios usos, cuando necesito extraer datos de forma extensa de Google Analytics, la herramienta de mi elección es la extensión de hoja de cálculo de Google. Por supuesto, necesito hacer varias conexiones a mis tablas de GA, pero como con Report Builder de Adobe, puedo hacer referencia a las celdas desde los datos sin procesar y crear los informes que necesito, y luego visualizarlos usando las capacidades de gráficos de la hoja de cálculo de Google.


## 3. Exportaciones de datos sin procesar

Para aquellos momentos en los que realmente necesita datos sin procesar, tanto Adobe como Google ofrecen funcionalidades para extraer información de esta manera.

### 3.1. Fuente de datos de Adobe

En la sección 2.2.2, mencioné que la API de Adobe Analytics extraía “datos procesados”. La fuente de datos sin procesar seguirá extrayendo datos procesados por las “reglas de procesamiento” configuradas en el panel de administración (asegúrese de que los datos sin procesar se retrasen para garantizar que todas estas reglas se hayan completado antes del momento en que se extrae la fuente de datos sin procesar), pero estos datos sin procesar incluirán todos los datos que se excluyen en cualquier otro lugar.

Esto significa que todas las exclusiones de bots, los datos filtrados de IP internos, etc., se incluirán en las fuentes de datos sin procesar. Existen indicadores para identificar estos datos, de modo que si está construyendo un lago de datos, su equipo de ingeniería puede crear lógicas para procesar estos datos en consecuencia.

Las fuentes de datos sin procesar se pueden personalizar para enviar todas las columnas de datos o solo columnas específicas, si necesita una fuente más enfocada.

Las fuentes se pueden enviar directamente a FTP, SFTP, S3, etc.


### 3.2. Google Big Query

Desafortunadamente, esta es una herramienta de Google con la que no he tenido ninguna experiencia, pero en teoría debería ser similar a la Fuente de datos de Adobe, lo que permite a su equipo de ingeniería acceder a los datos sin procesar de su cuenta de Google Analytics.

Sin embargo, creo que, en lugar de un volcado completo de datos sin procesar, deja a sus ingenieros acceder a los datos a través de consultas SQL, para que puedan extraer datos sin procesar o, si lo desean, todas las columnas de datos sin procesar para introducirlas en un lago de datos.

## 4. Conclusión

Al igual que con cualquier sistema, se necesita práctica para sentirse cómodo con él, pero esperamos que esta guía le sirva para iniciarse o le dé consejos para mejorar su uso de Adobe Analytics si no ha pasado de la superficie.

Sin embargo, subrayaré que recomendaría utilizar tanto Adobe Analytics como Google Analytics en su estrategia de implementación (aunque sea solo la versión gratuita de Google Analytics). Esto le permite tener un sistema de copia de seguridad para asegurarse de que tiene datos, ya que ningún sistema es infalible.

Hay muchos recursos disponibles más allá de esta guía, que pueden ayudar a mejorar su estrategia:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=es#home) : contiene tutoriales, vídeos, documentación y foros de la comunidad
* [Grupos de usuarios de Adobe](https://analytics-augs.adobe.com/) : centro de eventos de ejecución comunitaria para ayudar a los usuarios a conectarse entre sí y mejorar sus implementaciones. Puesto que estos eventos se basan en un huso horario específico, es mejor comprobar qué otras regiones se están ejecutando también.
* [Canal de YouTube de grupos de usuarios de Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - ¿No se pudo hacer una sesión de grupo de usuarios de Adobe Analytics? Vuelva a ver las sesiones de grupos de usuarios anteriores en todo el mundo para obtener más información sobre cómo utilizan la herramienta sus compañeros.
* [Medir el canal del Slack de chat](https://www.measure.chat/) : conéctese con usuarios de Adobe Analytics de todo el mundo y comparta las lecciones aprendidas en la industria, haga preguntas con sus colegas y únase a grupos de interés centrados en la medición.
* y más!

## Autor

Este documento fue escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, responsable de optimización de Analytics en Torstar

Campeona de Adobe Analytics

