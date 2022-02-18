---
title: 'Explicación y uso de Journey IQ: análisis multidispositivo'
description: Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varios dispositivos. El análisis multidispositivo se integra con el servicio de identidad de Adobe Experience Platform para identificar cómo se asignan los dispositivos a las personas. Entonces, aprovecha esta inteligencia para crear una vista multidispositivo del comportamiento del usuario. Esto resulta en poder realizar análisis sobre personas, no sobre dispositivos.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: User
level: Intermediate
exl-id: 3748d5d7-d250-4057-8131-afdc66c80200
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: ht
source-wordcount: '1641'
ht-degree: 100%

---

# Explicación y uso de [!DNL Journey IQ]: análisis multidispositivo

Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varios dispositivos. El análisis multidispositivo se integra con el [!DNL Adobe Experience Platform Identity Service] para identificar cómo se asignan los dispositivos a las personas. Entonces, aprovecha esta inteligencia para crear una vista multidispositivo del comportamiento del usuario. Esto resulta en poder realizar análisis sobre personas, no sobre dispositivos.

## Información general del análisis multidispositivo

### No soy mis dispositivos

Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varias “superficies” o “dispositivos”. Pueden utilizar un explorador web en un equipo o dispositivo móvil, o bien una aplicación móvil. En el análisis digital tradicional, que creció en la recopilación de datos basada en cookies, cada una de estas superficies se representa como un “visitante” único. Esto significa que cada uno de los usuarios humanos se representa como un visitante único múltiple.

A continuación, se muestra un ejemplo. Supongamos que Isabelle interactuó con su marca de la siguiente manera:

*Isabelle son tres visitantes*
![Recorrido tradicional de Analytics](assets/cda-isabelle-journey-traditional-analytics.png)

Utilizando el análisis tradicional, el recorrido de Isabelle se divide en tres partes. Está representada como tres visitantes únicos, cada uno de los cuales utilizó un dispositivo diferente para realizar tareas aisladas. Lo que se necesita es una vista unificada y multidispositivo de las interacciones de Isabelle. [!DNL Journey IQ: Cross-Device Analytics] proporciona esta vista.

*Isabelle es solo una persona*
![Recorrido de análisis multidispositivo](assets/cda-isabelle-journey-cross-device-analytics.png)

### Una vista multidispositivo proporciona mejores análisis

Tener una visión de la conducta de Isabelle centrada en las personas y multidispositivo puede marcar una diferencia significativa en su análisis. Por ejemplo, el enfoque tradicional basado en visitantes no le ofrece una imagen completa de la eficacia del canal de marketing. Veamos una vez más el recorrido de Isabelle, centrándonos en qué canal recibe crédito por su vista del producto y por su compra. Usaremos la atribución de [!UICONTROL último contacto] por simplicidad, pero ocurre el mismo problema usando cualquier modelo de atribución cuando se divide el comportamiento de Isabelle en visitantes separados. El uso de la visión tradicional del mundo basada en visitantes da resultados muy diferentes e incluso engañosos:

*Análisis tradicional frente a análisis multidispositivo*
![atribución de canal](assets/channel-attribution.png)

Observe que, con la vista multidispositivo, el canal de correo electrónico recibe crédito tanto por la vista del producto como por la compra, lo que representa con mayor precisión la experiencia de Isabelle en el mundo real.

Siga leyendo para obtener más información sobre lo siguiente:

* Funcionamiento del [!DNL Cross-Device Analytics]
* Requisitos previos para el [!DNL Cross-Device Analytics]
* Interpretación de datos multidispositivo
* Análisis de datos multidispositivo en Analysis Workspace

## Funcionamiento del [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] se integra con [!DNL Adobe Experience Platform Identity Service], utilizando [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=es) o [!DNL Private Graph] para identificar cómo se asignan los dispositivos a las personas. Entonces, aprovecha esta inteligencia para crear una vista multidispositivo del comportamiento del usuario. El análisis multidispositivo incluye funcionalidades y herramientas sin igual para ayudar a su empresa a comprender el uso de varios dispositivos y la experiencia del cliente en dichos dispositivos en sus interacciones con su marca. Se encuentra como una capa debajo de Analysis Workspace para proporcionar un conocimiento profundo del análisis de audiencias basado en personas y la atribución, segmentación y análisis de recorrido multidispositivo mediante herramientas potentes como [!UICONTROL visita en orden previsto], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] y [!DNL Attribution IQ].

### El [!DNL Cross-Device Virtual Report Suite]

El análisis multidispositivo se presenta a través de un tipo especial de [[!UICONTROL grupo de informes virtuales]](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=es) multidispositivo. Esto le permite seguir utilizando el grupo de informes original basado en dispositivos a medida que introduce el análisis multidispositivo en su organización. La configuración de un grupo de informes virtuales de análisis multidispositivo es fácil.

En el primer paso del generador del grupo de informes virtuales, seleccione el [!UICONTROL grupo de informes] que ha configurado Adobe como habilitado para análisis multidispositivo:

*Elija un [!UICONTROL grupo de informes]* base habilitado para análisis multidispositivo (fuente)
Primer paso del ![[!UICONTROL grupo de informes virtuales]](assets/cda-vrs-step-one.png)

A continuación, active el [!UICONTROL Procesamiento de intervalo de tiempo] y habilite la [!UICONTROL vinculación multidispositivo]:

*Habilite el [!UICONTROL procesamiento de intervalo de tiempo] y la [!UICONTROL vinculación multidispositivo]*
Segundo paso del ![[!UICONTROL grupo de informes virtuales]](assets/cda-vrs-step-two.png)

Finalice la configuración del grupo de informes virtuales y guárdelo. El grupo de informes virtuales de análisis multidispositivo aparecerá en Analysis Workspace con un icono especial junto a él, como se muestra a continuación:

*Seleccione el grupo de informes virtuales de análisis multidispositivo en Analysis Workspace*
Tercer paso del ![[!UICONTROL grupo de informes virtuales]](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Puede crear tantos [!UICONTROL grupos de informes virtuales] de análisis multidispositivo como desee sobre el [!UICONTROL grupo de informes] base habilitado para análisis entre dispositivos.

### Restauración del historial

A veces, sus usuarios tardan un tiempo en iniciar sesión y en que [!DNL Co-op Graph] o [!DNL Private Graph] los identifique y asigne a sus dispositivos. El análisis multidispositivo utiliza una ventana retrospectiva de 30 días, que le permite restaurar a un visitante no identificado previamente como una persona hasta 30 días antes.

¿Cómo ayuda esto? Recuerde el recorrido de Isabelle de la discusión anterior:

![[!DNL Cross-Device Analytics] Recorrido ](assets/cda-isabelle-journey-cross-device-analytics.png)

Es posible que Isabelle no haya iniciado sesión hasta justo antes de realizar la compra, y que el [!DNL Co-op Graph] o [!DNL Private Graph] no haya asignado juntos los dispositivos de Isabelle hasta poco después de su compra. Pero la retrospección de 30 días del análisis multidispositivo le permite restaurar el comportamiento pasado de Isabelle en el nivel de persona, lo que le proporciona la visión multidispositivo de su recorrido que usted necesita.

>[!NOTE]
>
>Dado que se puede restaurar el historial, esto significa que los datos pueden cambiar con el tiempo en un [!UICONTROL grupo de informes virtuales] habilitado para análisis multidispositivo. Tenga esto en cuenta a la hora de comunicar datos de un análisis multidispositivo.

## Requisitos previos para el [!UICONTROL análisis multidispositivo]

El análisis multidispositivo se incluye con [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html?lang=es). A partir de septiembre de 2019, los clientes de [!DNL Analytics Ultimate] que cumplan los requisitos previos enumerados a continuación pueden utilizar el análisis multidispositivo. Los requisitos previos para el análisis multidispositivo son los siguientes:

* Su compañía debe ser abonada de un [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=es) de [!DNL Adobe Experience Platform Identity Service], o usar un [!DNL Adobe Experience Platform Identity Service Private Graph].
* Debe implementar todo lo necesario para el [!DNL Co-op Graph] o el [!DNL Private Graph], incluido [ID de Experience Cloud (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) y sincronización de ID con el gráfico. Tenga en cuenta que, además de los requisitos técnicos, el [!DNL Co-op Graph] tiene otros requisitos legales y contractuales.
* Actualmente, no es posible utilizar dos organizaciones IMS con un solo [!DNL Private Graph], por lo que debe estandarizar una sola organización de IMS. En algunos casos, un cliente con varias organizaciones de IMS puede usar el [!DNL Co-op Graph] conjuntamente con el análisis multidispositivo.
* El [!DNL Co-op graph] y el [!DNL Private Graph], así como ciertos componentes del análisis multidispositivo, están alojados en [!DNL Microsoft Azure]. Esto significa que los datos de [!DNL Analytics] se copian de un lado a otro entre el centro de procesamiento de datos de Adobe y la presencia de Adobe en [!DNL Microsoft Azure]. Algunos datos de [!DNL Analytics] se almacenarán en [!DNL Azure]. Su compañía debe aceptar este acuerdo.
* El análisis multidispositivo requiere un [!UICONTROL grupo de informes] “multidispositivo”. Es decir, el [!UICONTROL grupo de informes] que use para el análisis multidispositivo debe incluir datos de varios tipos de dispositivos o “superficies” diferentes, como la web de escritorio, la web móvil y la aplicación móvil. A partir de septiembre de 2019, el volumen de llamadas al servidor para este [!UICONTROL grupo de informes] debe ser igual o inferior a 100 MM/día de llamadas al servidor. Los límites del volumen de llamadas al servidor aumentarán en los próximos meses.
* Desde septiembre de 2019, el [!DNL Co-op Graph] y el [!DNL Private Graph] solo están disponibles en Norteamérica. La programación de la presencia de gráficos en EMEA y APAC se anunciará en el futuro. Si está en esas regiones, le recomendamos que empiece a consultar estos requisitos previos ahora para que esté listo cuando el gráfico esté disponible.

## Interpretación de datos multidispositivo

### Personas, no visitantes

Dentro del [!UICONTROL grupo de informes virtuales] del análisis multidispositivo, verá algunos cambios. Por ejemplo, la métrica [!UICONTROL Visitantes únicos] se ha sustituido por dos métricas nuevas: [!UICONTROL Personas] y [!UICONTROL Dispositivos únicos]. Estas nuevas métricas le ofrecen un mejor conocimiento del tamaño de la audiencia.

*Personas y Dispositivos únicos*
![[!UICONTROL Métrica Personas]](assets/cda-people-metric.png) del análisis multidispositivo 

En el [[!UICONTROL Generador de segmentos]](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=es), el contenedor de segmentos [!UICONTROL Visitante] se ha reemplazado por un contenedor de segmentos [!UICONTROL Persona]. Con un grupo de informes virtuales de análisis multidispositivo, puede crear segmentos multidispositivo como:

* Personas que utilizan más de un dispositivo
* Usuarios que empezaron su recorrido en un dispositivo móvil y más tarde compraron en uno de escritorio
* Visitas en las que las personas utilizan más de un dispositivo para llevar a cabo una tarea

*Segmentos de nivel de persona*
![[!DNL Segment Builder] [!UICONTROL Persona] Contenedor](assets/cda-segment-builder-person-container.png)

### Persistencia de dimensión

Dentro de un grupo de informes virtuales de análisis multidispositivo, las dimensiones como las [!DNL eVars] ahora persisten automáticamente entre dispositivos. Por ejemplo, una [!DNL eVar] que está configurada como:

* Asignación: Más reciente (último)
* Caduca después de: Compra

ahora persistirá automáticamente de un dispositivo a otro hasta que se active el evento de compra.

## Análisis de datos multidispositivo en Analysis Workspace

### Análisis de audiencias basadas en personas

¿Alguna vez se ha preguntado cuántas personas están interactuando con su marca? ¿Ha querido comprender cuántos dispositivos utilizan y de qué tipo? ¿Cómo se superpone su uso? Con un grupo de informes virtuales de análisis multidispositivo, puede crear [Diagramas de Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=es) multidispositivo e [histogramas](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html?lang=es) de dispositivos por persona.

*Análisis de audiencia basado en personas*
![Venn e Histograma](assets/cda-venn-and-histogram.png)

### [!DNL Flow] multidispositivo

Con análisis multidispositivo y Analysis Workspace, puede visualizar cómo se mueven las personas de un dispositivo a otro a lo largo del tiempo en el [[!DNL Flow visualization]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/flow.html?lang=es). Pueden ver dónde abandonan su recorrido y dónde lo retoman.

*[!DNL Flow]con análisis multidispositivo*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### [!DNL Fallout] multidispositivo

Es probable que use varias [[!DNL Fallout visualizations]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html?lang=es) para analizar el grado de avance de los usuarios en una serie de pasos determinados antes de alcanzar el éxito. ¿Sabía su vista de esas [!DNL Fallout visualizations] está limitada cuando se usa el análisis tradicional basado en dispositivos? Para que la visita en el orden previsto se realice correctamente, el siguiente paso debe producirse en el mismo explorador o aplicación que el anterior. En los análisis basados en dispositivos, no puede ver a las personas que completan correctamente el siguiente paso en otro dispositivo.

No hay que preocuparse, el análisis multidispositivo le cubre. El análisis multidispositivo crea la vista multidispositivo que hace que las [!DNL Fallout visualizations] sean mucho más útiles. Después de todo, lo que realmente importa es si la persona tuvo éxito en su tarea en algún lugar.

*[!DNL Fallout]con análisis multidispositivo*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Dado que el análisis multidispositivo crea una capa de datos multidispositivo debajo de Analysis Workspace, todo su análisis se condimentará con una perspectiva multidispositivo. Un ejemplo valioso es a través de [[!DNL Attribution IQ]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution/attribution.html?lang=es). [!DNL Attribution IQ] en Analysis Workspace permite comparar varios modelos de atribución en paralelo. Usando esta capacidad con análisis multidispositivo, ahora puede comparar cómo los distintos dispositivos contribuyen al éxito.

Por ejemplo, supongamos que desea comprender con qué frecuencia un teléfono móvil es el primer dispositivo utilizado en una interacción que, en última instancia, conduce al éxito. Representa la “tasa de adquisición” del teléfono móvil. Análisis multidispositivo + [!DNL Attribution IQ] le permite realizar este análisis:

*[!DNL Attribution IQ]con análisis multidispositivo*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Para obtener más información, consulte la [[!DNL Cross-Device Analytics] documentación de ayuda](https://experienceleague.adobe.com/docs/analytics/components/cda/cda-home.html?lang=es).
