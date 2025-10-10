---
title: Una guía completa para la transición a Adobe Analytics desde Google Analytics
description: Obtenga información acerca de la ubicación de funcionalidades equivalentes y cómo utilizarlas de forma eficiente al pasar de Google Analytics a Adobe Analytics
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '3403'
ht-degree: 97%

---

# Una guía completa para la transición a Adobe Analytics desde Google Analytics{#comprehensive-guide-for-transitioning-to-Adobe-Analytics}

## &#x200B;1. Introducción

Uno de los mayores desafíos en la transición entre cualquier herramienta es aprender dónde encontrar una funcionalidad equivalente y utilizarla de manera eficiente. Este debate forma parte de una guía más amplia para ayudar a los usuarios a realizar la transición a Adobe Analytics (como nuevo usuario o como proveniente de Google Analytics) con mayor facilidad. Se proporciona una comparación detallada con GA, como herramienta con la que es más probable que la mayoría de los usuarios estén familiarizados, para ayudarlos a correlacionar los conocimientos existentes con el nuevo conjunto de herramientas. Cuando no haya sustituto en la práctica, esto le ayuda a empezar y a reducir las frustraciones que puedan afectarle.

También deberíamos hacer una comparación terminológica rápida:

| **Descripción** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Se ha visto una métrica de evento que representa una página (o pantalla de una aplicación). | Vista de páginas | Pageview |
| Una métrica que representa un grupo de interacciones en su sitio web o aplicación que se producen en el mismo lapso de tiempo | Visita | Sesión |
| Una métrica que define un dispositivo identificado (en función de varios criterios, incluidas las cookies y otros patrones de comportamiento, para unir información del usuario) | Visitante único | Usuario |

## &#x200B;2. Las interfaces

Cuando la gente compara Adobe Analytics con Google Analytics, comentan que la interfaz de Adobe es desalentadora al principio. Esto es cierto, pero, aunque no lo crea, es una fortaleza más que una debilidad. Adobe proporciona una amplia gama de herramientas y flexibilidades en la visualización de datos, lo que le permite tener mucha más libertad para construir lo que necesita.

Empecemos por ver la creación de informes “en el sitio”.

### 2.1. Creación de informes en el sitio

#### 2.1.1. Pantalla de inicio

Tanto Adobe Analytics como Google Analytics permiten personalizar la primera vista que ve un usuario cuando inicia sesión.

##### 2.1.1.1. Workspace / Pantalla de inicio personalizada (Adobe Analytics)

Adobe Analytics no presume de crear un informe generado previamente para que todos los usuarios lo vean en el inicio de sesión. La página principal predeterminada lleva al usuario a la pantalla de aterrizaje del Espacio de trabajo, que muestra a cada usuario todos los informes del espacio de trabajo que han creado o que se han compartido con él. Además, cada uno puede establecer cualquiera de estos informes como su pantalla de inicio si así lo desea.

![workspace-create-project](assets/ga-to-aa_1.png)

Más adelante, en esta guía, hay más detalles sobre el espacio de trabajo. Ver sección 2.1.2.1

>[!TIP]
>
>Cree o comparta algunos informes estándar para su organización de modo que tengan un punto de partida para ver la información sin tener que sumergirse en la creación de sus propios informes de inmediato.



##### 2.1.1.2. Perspectivas de la pantalla de inicio (Google Analytics)

* La pantalla de inicio de Google Analytics tiene algunas visualizaciones generadas previamente para usted. Estas cubren cosas como las siguientes:
* Usuarios, Sesiones, Tasa de salida hacia otro sitio y Duración de la sesión en los últimos siete días
* Usuarios por hora del día en los últimos 30 días
* Usuarios actuales en este momento y Páginas activas principales
* Canal de tráfico, Fuente/medio y Referencias en los últimos siete días
* Sesiones por país en los últimos siete días
* Páginas principales de los últimos siete días
* Tendencia de usuarios activos de los últimos 30 días
* y más

Los usuarios de GA4 tienen más opciones para personalizar y añadir sus propios informes a la pantalla de inicio.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Probablemente, esto es lo que más se echa de menos en Adobe Analytics. No tiene una pantalla de inicio generada previamente. Sin embargo, puede configurar fácilmente un Espacio de trabajo personalizado para replicar lo que necesita de la lista anterior y establecerlo como su pantalla de aterrizaje. Hay más información más adelante (o consulte la sección 2.1.2.1 de Adobe Workspace).

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

![analytics-page-views-report](assets/ga-to-aa_3.png)

Las tablas de forma libre permiten tener varias columnas y utilizar la segmentación, según sea necesario, para visualizar los datos como desee.

Si no desea ver un desglose por fecha, simplemente, arrastre y suelte allí otra dimensión o segmento para visualizar los datos de una manera diferente. Por ejemplo, use segmentos para Tipo de dispositivo y, a continuación, agregue un desglose por sistema operativo para los usuarios de móviles o tabletas:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

El espacio de trabajo le permite dejar volar su creatividad, no se limita a desgloses “estándar”. Puede crear las visualizaciones que necesita para profundizar en las comparaciones que necesita ejecutar.

>[!TIP]
>
>No tenga miedo de jugar y explorar. Hay muchas maneras de pensar distinto. Además, compruebe que lo que ha creado demuestra lo que piensa. La experiencia ayuda.

Puede crear métricas calculadas sobre la marcha o segmentos que solo se encuentren dentro del informe para evitar que se sature el repositorio de segmentos y cálculos. Esto le permite crear elementos centrados que son necesarios para informes específicos sin confundir a su organización con cosas que no se pueden aprovechar en otros contextos.

Esta explicación es solo una introducción a esta herramienta, hay otras guías completas para iniciarse. Una vez que revise estas guías, haga informes completos como los siguientes:

![workspace-dashboard](assets/ga-to-aa_5.png)

Los espacios de trabajo no se guardan automáticamente, por lo que es más fácil hacer un único informe ad hoc sin saturar el repositorio de informes.

Otra funcionalidad potente de los espacios de trabajo es la capacidad de aplicar modificadores interactivos a los informes en forma de menú desplegables. Estos menús desplegables no funcionan en archivos CSV o PDF exportados de los informes. Sin embargo, en el informe en directo, le permiten actualizar todas las visualizaciones de un panel para mostrar el mismo informe en condiciones diferentes. Se pueden utilizar varios desplegables y, siempre que las opciones no sean mutuamente excluyentes, los elementos seleccionados se apilarán para permitir presentar de forma limpia la información.

>[!IMPORTANT]
>
>Para obtener más información acerca del uso de desplegables y desgloses de forma libre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: paneles, informes personalizados e informes guardados

Google tiene algunas herramientas para crear informes dentro de la interfaz, pero siguen teniendo la misma visualización y las mismas limitaciones de la sección de informes.

Ahora, aquellos versados en Google Analytics que lean esto, podrían estar diciendo: “Bueno, espere un segundo, ¿qué pasa con Google Data Studio? ¿No es un mejor equivalente del espacio de trabajo de Adobe?” Sí, pero técnicamente Data Studio no forma parte de la herramienta Analytics y permite conexiones a diferentes fuentes de datos. Esta herramienta se trata más adelante, específicamente en la sección 2.2.3, Acceso ampliado a informes.

Los paneles de control y los informes personalizados de Google le permiten extraer varias visualizaciones en un informe, pero, a diferencia del espacio de trabajo, aún están bloqueados en correlaciones sencillas y en qué datos se pueden colocar en qué columnas.

En los Informes personalizados, uno de los mayores desafíos es, cuando crea un filtro, que se aplique a todas las pestañas del informe. No existe una forma de comparar dos filtros diferentes dentro del mismo informe.

Para las comparaciones superficiales, cumple su función. Todos son similares a los Paneles de control, los Informes personalizados y los Marcadores heredados de Adobe. Herramientas básicas proporcionadas para satisfacer sus necesidades y que residen en el grupo de informes.

#### 2.1.3. Informes

Tanto Google como Adobe tienen algunos informes navegables que son tablas creadas previamente y gráficos básicos de cronología basados en una dimensión.

##### 2.1.3.1. Informes de Adobe Analytics

Adobe Analytics también tiene una sección Informes, aunque se está eliminando gradualmente a favor de Analysis Workspace. De hecho, se ha anunciado el fin de la vida útil de esta interfaz, ya que Espacio de trabajo es una herramienta más potente. La mayoría de estas tablas se pueden crear y modificar con más facilidad. Las secciones de Adobe están mucho más divididas, y esto puede ser desalentador:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Como la mayoría de lo anterior es accesible a través de los espacios de trabajo, hago una breve descripción de estas secciones y cómo se relacionan con Google Analytics, y resalto los informes que siguen siendo relevantes.

Las métricas del sitio son lo que cabría esperar: abarcan las métricas estándar (vistas de página, visitantes únicos, visitas y eventos personalizados que haya configurado). Esto es similar al informe de comportamiento de GA, pero también incluye algo de lo que encontraría en el de público (ya que Adobe no divide los tipos de métricas).

Aquí, encontrará los informes de “bots”. El tráfico de bots se excluye de todos los informes estándar. Sin embargo, hay dos que ofrecen una perspectiva de lo que está sucediendo y de los bots que llegan al sitio. Esto es especialmente bueno si configura reglas de bots personalizadas para excluir los de spam conocidos que visitan con frecuencia el sitio. Puede obtener información sobre lo que están haciendo esos bots sin que los informes principales se inunden de ese tráfico. Actualmente, los informes de bots no están disponibles a través del Espacio de trabajo (pero las nuevas funcionalidades de creación de informes que se lanzarán próximamente también permitirán a los usuarios obtener esta información).

Contenido del sitio es una agrupación de dimensiones estándar de Adobe: Nombre de página, Secciones de sitio, Jerarquías, Servidores y más. Todas estas dimensiones están disponibles en el Espacio de trabajo.

Móvil es una agrupación de datos específicos de dispositivos móviles, incluidos dispositivos, tipos de dispositivos y mucho más. Están disponibles en el Espacio de trabajo.

Las rutas no están disponibles en el Espacio de trabajo. El Espacio de trabajo tiene un diagrama de flujo en el que puede ver los flujos de entrada y salida para una sola página o valor. Por el contrario, las rutas permiten ver las rutas más comunes utilizadas en el sitio web. De forma predeterminada, Páginas es el primer informe de ruta configurado para usted. Sin embargo, puede activarlo para props personalizados como un valor de Tipo de página. Puede observar las rutas dentro de los tipos de página. La otra cosa que personalmente me gusta de las Rutas es la forma sencilla en que se presenta la información... El diagrama de flujo del espacio de trabajo (dependiendo de cuánto esté tratando de ver) puede ser abrumador. Recomiendo probar ambos... cada uno tiene un uso y valor dependiendo de lo que quiera lograr. Debe tenerse en cuenta que cualquier dimensión se puede utilizar en Flujos, mientras que las Rutas deben configurarse en un prop en el panel Administración.

Los informes Fuentes de tráfico, Campañas y Canales de marketing son todos similares al informe Adquisición del producto de Google. Las Fuentes de tráfico se centran en los remitentes del reenvío reales, Campañas, en los códigos de campaña y Canales de marketing, también en estos, pero además aplican una lógica adicional (según determine el usuario) sobre cómo procesar la información. Adobe proporciona más libertad sobre cómo configurar las reglas. Por el contrario, Google hace muchas cosas por usted; es un cambio en la forma de pensar. De forma predeterminada, la atribución de Google para códigos de campaña es de seis meses. La atribución de Adobe se fija en una semana de forma predeterminada. Esto puede cambiarse en la configuración de administración, pero en el espacio de trabajo puede aplicar una atribución personalizada sobre cualquier dimensión, lo que le ofrece una mayor flexibilidad sobre la marcha.

Los informes Retención de visitantes y Perfil del visitante son similares a los informes Público de Google Analytics. Retención de visitantes se centra más en la frecuencia de retorno, mientras que Perfil del visitante, en la geografía y la tecnología de los usuarios.

Los informes Conversión personalizada y Tráfico personalizado son informes de dimensión personalizados. Las conversiones son eVars. Puede establecer una caducidad personalizada en el valor, como visita individual, visita, mes y año. Este valor queda en la persistencia de un usuario durante el lapso de tiempo configurado, a menos que se sobrescriba. Las variables de tráfico son props. También puede configurarlas para informes de rutas o como elementos de lista que separan varios valores según un delimitador de su elección.

Medios es para elementos como vídeos o archivos de audio en los que ha configurado un seguimiento de medios especial.

Informes personalizados es una sección en la que un usuario puede personalizar las columnas y desgloses que ha creado en la interfaz de informes y guardarlos como un informe personalizado. Sin embargo, como se ha mencionado anteriormente, dado que el Espacio de trabajo permite desgloses y correlaciones mucho más potentes, cualquier personalización debería realizarse allí. Esta era una buena solución antes de que existiera el espacio de trabajo.

La sección Marcadores es similar a los Informes personalizados, donde los informes usados con frecuencia se pueden añadir como marcador en la interfaz de informes para que se puedan encontrar más fácilmente.

El tablero era un producto heredado que permitía a las personas combinar informes breves de datos en una sola visualización. Sin embargo, la funcionalidad de Workspace (sección 2.1.2.1) es mucho más fácil de usar, ya que solo existe como punto de acceso a los informes heredados que deben reconstruirse antes de que esta función se cierre.

Los objetivos permiten a las personas crear un informe basado en un objetivo dentro de un periodo de tiempo determinado. Los equipos monitorizan las campañas para ver si van por buen camino para alcanzar sus objetivos de tráfico.

Todos los informes aquí permiten varias columnas de métricas y desgloses de dimensiones. No obstante, la simplicidad de las visualizaciones y parte de la lógica detrás de qué elementos podrían correlacionarse pueden ser frustrantes a veces.

##### 2.1.3.2. Informes de Google Analytics

Google Analytics divide estos informes en las siguientes secciones: Tiempo real, Público, Adquisición, Comportamiento y Conversaciones (en GA3) y en Ciclo vital (con las subsecciones Adquisición, Participación, Monetización y Retención) y Usuario (con las subsecciones Grupos demográficos y Tecnología).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

Puede llevar a cabo algunos ajustes menores en estas visualizaciones, agregar un desglose de dimensión secundario, cambiar la visualización, crear un filtro en los datos y más. Puede guardar las personalizaciones como un informe guardado.

Estos ofrecen una visión rápida y sencilla de sus datos. Sin embargo, no puede comparar cosas como usuarios con vistas de página para una página de la misma tabla y no puede añadir más de una dimensión adicional para ver datos adicionales.

Son buenos para obtener datos analíticos rápidos, pero si realmente necesita profundizar, sufren de limitaciones.

### 2.2. Acceso ampliado a los informes

Además de la Creación de informes en el sitio, la mayoría de las herramientas ofrecen una funcionalidad ampliada que le permite sacar el análisis de las herramientas y crear algo un poco más personalizado.

#### 2.2.1. Report Builder de Adobe Analytics (extensión de Microsoft® Excel)

El espacio de trabajo es una buena herramienta, pero a veces es necesario poner los datos en una hoja de cálculo personalizada, posiblemente para poder unir varias fuentes de datos. Aquí es donde Report Builder entra en juego.

Report Builder es un complemento para Microsoft® Excel que le permite crear conexiones con los datos de Adobe Analytics para extraer datos de tablas que puede manipular en Excel. Por lo general, para utilizarlo de forma eficaz, extraiga los datos en algunas pestañas de datos sin procesar, luego use las referencias de celdas de Excel para sacar datos de estas pestañas en un solo informe consolidado y, a continuación, cree gráficos y visualizaciones.

>[!NOTE]
>
>Report Builder tiene un permiso especial que debe aplicarse a los usuarios para acceder a este complemento. Debería concederse a los usuarios que hayan aprendido a utilizar bien la herramienta.

#### 2.2.2. Conexión de la API de Adobe Analytics

Si necesita que los datos de Adobe Analytics se digieran con algo distinto a Excel y quiere los datos procesados, incluidas las exclusiones de reglas de bots, utilice la API de Adobe para extraer los datos directamente. A continuación, procese los datos mediante un script o agréguelos a una base de datos para su uso con otro sistema.

Debe tenerse en cuenta que la API sigue extrayendo datos de correlación aplicando los desgloses y segmentos según se especifican en la solicitud de extracción.

Workspace de Adobe (sección 2.1.2.1) utiliza la API para generar los informes y, si habilita el modo de depuración en Workspace, le mostrará las llamadas de API exactas que se han usado. Esta es una forma rápida de generar sus llamadas de API. Al utilizar el Espacio de trabajo para generar y validar los datos que quiere extraer, emplee esas llamadas de API para sacar los datos a su propio procesamiento.


#### 2.2.3. Data Studio de Google Analytics

Si ha estado leyendo, ya sabe que he mencionado Data Studio como el equivalente al Espacio de trabajo de Adobe. Data Studio le permite extraer datos de Google Analytics, pero también de otras fuentes. Es interesante si desea consolidar los datos de análisis con otros datos recopilados. Sin embargo, con Google Analytics, existen el mismo tipo de limitaciones de visualización. El modo en que se forman las filas y columnas sigue siendo limitado.

Con todo, es una herramienta potente, y no disuadiría a la gente de usarla de ninguna manera. Mi experiencia personal es que el comportamiento rígido es bastante restrictivo.


#### 2.2.4. Extensión de hoja de cálculo de Google

Para mis propios usos, cuando necesito extraer datos de forma extensa de Google Analytics, la herramienta de mi elección es la extensión de hoja de cálculo de Google. Aunque necesito hacer múltiples conexiones a mis tablas de GA, puedo hacer referencia a las celdas de los datos sin procesar y elaborar los informes que necesito. Después, los visualizo utilizando las funcionalidades gráficas de las Hojas de cálculo de Google.


## &#x200B;3. Exportaciones de datos sin procesar

Cuando realmente necesita datos sin procesar, tanto Adobe como Google ofrecen funcionalidades para extraer información de esta manera.

### 3.1. Fuente de datos de Adobe

En la sección 2.2.2, mencioné que la API de Adobe Analytics extraía “datos procesados”. La fuente de datos sin procesar extrae datos procesados por las “reglas de procesamiento” que se han configurado en el panel de administración, pero estos datos sin procesar incluyen todos los datos que se excluyen en cualquier otra parte.

Esto significa que todas las exclusiones de bots, los datos filtrados de IP internos, etc., se incluirán en las fuentes de datos sin procesar. Existen indicadores para identificar estos datos, de modo que si está construyendo un lago de datos, el equipo de ingeniería puede crear lógicas para procesar estos datos en consecuencia.

Las fuentes de datos sin procesar se pueden personalizar para enviar todas las columnas de datos o solo columnas específicas, si necesita una fuente más enfocada.

Las fuentes se pueden enviar directamente a FTP, SFTP o S3.


### 3.2. Google Big Query

Por desgracia, esta es una herramienta de Google con la que no he tenido ninguna experiencia. En teoría debería ser similar a la Fuente de datos de Adobe, lo que permite a su equipo de ingeniería acceder a los datos sin procesar desde su cuenta de Google Analytics.

Sin embargo, en lugar de proporcionar un volcado de datos sin procesar completo, permite a los ingenieros acceder a los datos a través de consultas SQL para extraer datos sin procesar concretos o todas las columnas.

## &#x200B;4. Conclusión

Como cualquier sistema, es necesario practicar para sentirse cómodo con la herramienta. Esperamos que esta guía le ayude a empezar o le proporcione sugerencias para mejorar el uso de Adobe Analytics.

Sin embargo, subrayaré que recomendaría utilizar tanto Adobe Analytics como Google Analytics en su estrategia de implementación (aunque sea solo la versión gratuita de Google Analytics). Esto le permite tener un sistema de copia de seguridad para asegurarse de que tiene datos, ya que ningún sistema es infalible.

Hay muchos recursos disponibles más allá de esta guía, que pueden ayudar a mejorar su estrategia:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=es#home): contiene tutoriales, vídeos, documentación y foros de la comunidad
* [Grupos de usuarios de Adobe](https://analytics-augs.adobe.com/): un centro de eventos de la comunidad para ayudar a los usuarios a conectar entre sí y mejorar sus implementaciones.
* [Canal de YouTube de grupos de usuarios de Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA): ¿no pudo asistir a una sesión de grupo de usuarios de Adobe Analytics? Vuelva a ver las sesiones de grupos de usuarios anteriores en todo el mundo para obtener más información acerca de cómo utilizan la herramienta sus colegas.
* [Canal de Slack de chat de Measure](https://www.measure.chat/): conéctese con usuarios de Adobe Analytics de todo el mundo y comparta las lecciones aprendidas en la industria, haga preguntas de sus colegas y únase a grupos de interés centrados en la medición.
* ¡y más!

## Autor

Este documento fue escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, jefa de optimización de análisis en Torstar

Campeona de Adobe Analytics

