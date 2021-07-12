---
title: 'Explicación y uso de Recorrido IQ: Análisis entre dispositivos'
description: Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varios dispositivos. El análisis entre dispositivos se integra con el servicio de identidad de Adobe Experience Platform para identificar cómo se asignan los dispositivos a las personas. A continuación, aprovecha esta inteligencia para crear una vista entre dispositivos del comportamiento del usuario. Esto resulta en poder realizar análisis en personas, no en dispositivos.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: User
level: Intermediate
exl-id: 3748d5d7-d250-4057-8131-afdc66c80200
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 6%

---

# Explicación y uso de [!DNL Journey IQ]: análisis entre dispositivos

Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varios dispositivos. El análisis entre dispositivos se integra con [!DNL Adobe Experience Platform Identity Service] para identificar cómo se asignan los dispositivos a las personas. A continuación, aprovecha esta inteligencia para crear una vista entre dispositivos del comportamiento del usuario. Esto resulta en poder realizar análisis en personas, no en dispositivos.

## Información general sobre análisis entre dispositivos

### No soy mi dispositivo

Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varias &quot;superficies&quot; o &quot;dispositivos&quot;. Pueden utilizar un explorador web en un equipo o dispositivo móvil, o bien una aplicación móvil. En el análisis digital tradicional, que creció en la recopilación de datos basada en cookies, cada una de estas superficies se representa como un &quot;visitante&quot; único. Esto significa que cada uno de los usuarios humanos se representa como un visitante único múltiple.

A continuación, se muestra un ejemplo. Supongamos que Isabelle interactuó con su marca de la siguiente manera:

*Isabelle es tres*
![visitantesRecorrido tradicional de Analytics](assets/cda-isabelle-journey-traditional-analytics.png)

Utilizando análisis tradicionales, el recorrido de Isabelle se fractura en tres piezas. Está representada como tres visitantes únicos, cada uno de los cuales utilizó un dispositivo diferente para realizar tareas aisladas. Lo que se necesita es una visión unificada y entre dispositivos de las interacciones de Isabelle. [!DNL Journey IQ: Cross-Device Analytics] proporciona esta vista.

*Isabelle es una*
![personaRecorrido de análisis entre dispositivos](assets/cda-isabelle-journey-cross-device-analytics.png)

### Una Vista Entre Dispositivos Proporciona Mejores Análisis

Tener una visión de la conducta de Isabelle centrada en las personas y entre dispositivos puede marcar una diferencia significativa en su análisis. Por ejemplo, el enfoque tradicional basado en visitantes no le ofrece una imagen completa de la eficacia del canal de marketing. Veamos una vez más el recorrido de Isabelle, centrándonos en qué canal recibe crédito por su vista de producto y por su compra. Utilizaremos la atribución [!UICONTROL last-touch] para simplificar, pero el mismo problema ocurre cuando se utiliza cualquier modelo de atribución cuando se divide el comportamiento de Isabelle en visitantes separados. El uso de la visión tradicional del mundo basada en visitantes da resultados muy diferentes e incluso engañosos:

*Atribución de canal entre análisis tradicionales y*
![análisis entre dispositivos](assets/channel-attribution.png)

Observe que con la vista entre dispositivos, el canal de correo electrónico recibe crédito tanto por la vista del producto como por la compra, lo que representa con mayor precisión la experiencia real de Isabelle en el mundo.

Siga leyendo para obtener más información:

* Cómo funciona [!DNL Cross-Device Analytics]
* Requisitos previos para [!DNL Cross-Device Analytics]
* Interpretación de datos entre dispositivos
* Análisis de datos entre dispositivos en Analysis Workspace

## Cómo funciona [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] se integra con  [!DNL Adobe Experience Platform Identity Service], utilizando  [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/es-ES/device-co-op/using/home.html) o  [!DNL Private Graph] para identificar cómo los dispositivos se asignan a las personas. A continuación, aprovecha esta inteligencia para crear una vista entre dispositivos del comportamiento del usuario. CDA incluye funcionalidades y herramientas sin igual para ayudar a su empresa a comprender el uso de varios dispositivos y la experiencia del cliente en dichos dispositivos en sus interacciones con su marca. Se encuentra como una capa debajo de Analysis Workspace para proporcionar una perspectiva profunda del análisis de audiencia basado en personas y la atribución, segmentación y análisis de recorrido entre dispositivos mediante herramientas poderosas como [!UICONTROL Visitas en el orden previsto], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] y [!DNL Attribution IQ].

### [!DNL Cross-Device Virtual Report Suite]

CDA se presenta a través de un tipo especial de [[!UICONTROL Grupo de informes virtuales]](https://docs.adobe.com/content/help/es-ES/analytics/components/virtual-report-suites/vrs-about.html) entre dispositivos. Esto le permite seguir utilizando el grupo de informes original basado en dispositivos a medida que introduce análisis entre dispositivos en su organización. La configuración de un VRS de CDA es fácil.

En el paso uno del creador de VRS, elija el [!UICONTROL grupo de informes] que ha configurado el Adobe como habilitado para CDA:

*Elegir un grupo de  [!UICONTROL informes base (fuente) habilitado para CDA]*
![[!UICONTROL Grupo de informes ] virtualesPaso uno](assets/cda-vrs-step-one.png)

A continuación, active [!UICONTROL Procesamiento de intervalo de tiempo] y habilite la [!UICONTROL vinculación entre dispositivos]:

*Habilitar el procesamiento  [!UICONTROL de tiempo de los ] informes y la vinculación  [!UICONTROL entre]*
![ dispositivosGrupo de informes virtualesPaso dos](assets/cda-vrs-step-two.png)

Finalice la configuración del VRS y guárdelo. El VRS de CDA aparecerá en Analysis Workspace con un icono especial junto a él, como se muestra a continuación:

*Seleccione el VRS de CDA en Analysis*
![[!UICONTROL WorkspaceGrupo de informes virtualesPaso tres ] ](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Puede crear tantos grupos de informes virtuales [!UICONTROL CDA] como desee sobre el grupo de informes base [!UICONTROL habilitado para CDA].

### Restauración del historial

A veces, sus usuarios tardan un tiempo en iniciar sesión y en que [!DNL Co-op Graph] o [!DNL Private Graph] los identifique y asigne juntos sus dispositivos. CDA utiliza una ventana retrospectiva de 30 días, que le permite reafirmar a un visitante no identificado previamente como una persona hasta 30 días antes.

¿Cómo ayuda esto? Recuerden el recorrido de Isabelle de la discusión anterior:

![[!DNL Cross-Device Analytics] Recorrido](assets/cda-isabelle-journey-cross-device-analytics.png)

Es posible que Isabelle no haya iniciado sesión hasta justo antes de realizar la compra, y que los [!DNL Co-op Graph] o [!DNL Private Graph] no hayan mapeado juntos los dispositivos de Isabelle hasta algún momento después de su compra. Pero el retroceso de 30 días de la CDA permite a la CDA reafirmar el comportamiento pasado de Isabelle a nivel personal, proporcionándole la visión entre dispositivos de su recorrido que usted necesita.

>[!NOTE]
>
>Dado que se puede reafirmar el historial, esto significa que los datos pueden cambiar con el tiempo en un [!UICONTROL grupo de informes virtuales] habilitado para CDA. Tenga esto en cuenta a la hora de comunicar perspectivas desde un análisis basado en CDA.

## Requisitos previos para [!UICONTROL Análisis entre dispositivos]

CDA se incluye con [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). A partir de septiembre de 2019, [!DNL Analytics Ultimate] los clientes que cumplan los requisitos previos enumerados a continuación podrán utilizar CDA. Los requisitos previos para CDA son los siguientes:

* Su empresa debe ser miembro de [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) o utilizar un [!DNL Adobe Experience Platform Identity Service Private Graph].
* Debe implementar todo lo necesario para [!DNL Co-op Graph] o [!DNL Private Graph], incluido [ID de Experience Cloud (ECID)](https://docs.adobe.com/content/help/es-ES/id-service/using/home.html) y la sincronización de ID con el gráfico. Tenga en cuenta que además de los requisitos técnicos, el [!DNL Co-op Graph] tiene otros requisitos legales y contractuales.
* Actualmente no es posible utilizar dos organizaciones IMS con una sola [!DNL Private Graph], por lo que debe estandarizar en una sola organización IMS. En algunos casos, es posible que un cliente con varias organizaciones IMS utilice el [!DNL Co-op Graph] junto con CDA.
* Los [!DNL Co-op graph] y [!DNL Private Graph], así como ciertos componentes de CDA, están alojados en [!DNL Microsoft Azure]. Esto significa que [!DNL Analytics] los datos se copian de un lado a otro entre el centro de procesamiento de datos del Adobe y la presencia del Adobe en [!DNL Microsoft Azure]. Algunos [!DNL Analytics] datos se almacenarán en [!DNL Azure]. Su empresa debe aceptar este acuerdo.
* CDA requiere un [!UICONTROL grupo de informes] entre dispositivos. Es decir, el [!UICONTROL grupo de informes] que utilice para CDA debe incluir datos de varios tipos de dispositivos o &quot;superficies&quot; diferentes, como la web de escritorio, la web móvil y la aplicación móvil. A partir de septiembre de 2019, el volumen de llamadas al servidor para este [!UICONTROL grupo de informes] debe ser de 100 MM de llamadas al servidor al día o menos. (Los límites del volumen de llamadas al servidor aumentarán en los próximos meses).
* A partir de septiembre de 2019, [!DNL Co-op Graph] y [!DNL Private Graph] solo están disponibles en Norteamérica. El calendario de presencia de gráficos en EMEA y APAC se anunciará en el futuro. Si está en esas regiones, le recomendamos que empiece a consultar estos requisitos previos ahora para que esté listo para usar cuando el gráfico esté disponible.

## Interpretación de datos entre dispositivos

### Personas no visitantes

Dentro del grupo de informes virtuales [!UICONTROL CDA], verá algunos cambios. Por ejemplo, la métrica [!UICONTROL Visitantes únicos] se reemplaza por dos métricas nuevas: [!UICONTROL People] y [!UICONTROL Dispositivos únicos]. Estas nuevas métricas le ofrecen una mejor perspectiva del tamaño de la audiencia.

*Personas y*
![dispositivos únicosMétrica  [!UICONTROL Personas CDA]](assets/cda-people-metric.png)

En el [[!UICONTROL Generador de segmentos]](https://docs.adobe.com/content/help/es-ES/analytics/components/segmentation/segmentation-workflow/seg-build.html), el contenedor de segmento [!UICONTROL Visitante] ha sido reemplazado por un contenedor de segmento [!UICONTROL Persona]. Con un VRS de CDA, puede crear segmentos entre dispositivos como:

* Personas que utilizan más de un dispositivo
* Personas que empiezan su recorrido en un dispositivo móvil y luego compran más tarde en un dispositivo de escritorio
* Visitas en las que las personas utilizan más de un dispositivo para realizar una tarea

*Segmentos de nivel*
![[!DNL Segment Builder]  personalPersonContainer](assets/cda-segment-builder-person-container.png)

### Persistencia del Dimension

Dentro de un VRS de CDA, dimensiones como [!DNL eVars] ahora persisten automáticamente entre dispositivos. Por ejemplo, un [!DNL eVar] que esté configurado como:

* Asignación: Más reciente (último)
* Caduca después de: Compra

ahora persistirá automáticamente de un dispositivo a otro hasta que se active el evento de compra.

## Análisis de datos entre dispositivos en Analysis Workspace

### Análisis de audiencias basadas en personas

¿Alguna vez te has preguntado cuántas personas están interactuando con tu marca? ¿Ha querido comprender cuántos y qué tipo de dispositivos utilizan? ¿Cómo se superpone su uso? Con un VRS de CDA, puede crear [diagramas de Venn](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/venn.html) entre dispositivos y [histogramas](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/histogram.html) por persona.

*Análisis de audiencia basado en*
![personasVenn e Histograma](assets/cda-venn-and-histogram.png)

### Entre dispositivos [!DNL Flow]

Con CDA y Analysis Workspace, puede visualizar cómo se mueven las personas de un dispositivo a otro a lo largo del tiempo en [[!DNL Flow visualization]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Pueden ver dónde abandonan en su recorrido y dónde siguen.

*[!DNL Flow]con CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Entre dispositivos [!DNL Fallout]

Es probable que utilice varios [[!DNL Fallout visualizations]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) para analizar en qué medida los usuarios avanzan a través de una serie determinada de pasos antes de lograr el éxito. ¿Sabía que su vista de esos [!DNL Fallout visualizations] es limitada al utilizar análisis tradicionales basados en dispositivos? Para que la visita en el orden previsto se realice correctamente, el siguiente paso debe producirse en el mismo explorador o aplicación que el paso anterior. En los análisis basados en dispositivos, no ve a las personas que completan correctamente el siguiente paso en otro dispositivo.

No hay que preocuparse, CDA te ha cubierto. CDA crea la vista entre dispositivos que hace que [!DNL Fallout visualizations] sea mucho más útil. Después de todo, lo que realmente importa es si la persona tuvo éxito en su tarea en algún lugar.

*[!DNL Fallout]con CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Dado que CDA crea una capa de datos entre dispositivos debajo de Analysis Workspace, todo su análisis se verá condimentado con una perspectiva entre dispositivos. Un ejemplo eficaz es a través de [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] en Analysis Workspace permite comparar varios modelos de atribución en paralelo. Con esta capacidad con CDA, ahora puede comparar cómo los distintos dispositivos contribuyen al éxito.

Por ejemplo, supongamos que desea comprender con qué frecuencia un teléfono móvil es el primer dispositivo utilizado en una interacción que, en última instancia, conduce al éxito. Representa la &quot;tasa de adquisición&quot; del teléfono móvil. CDA + [!DNL Attribution IQ] le permite realizar este análisis:

*[!DNL Attribution IQ]con CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Para obtener más información, consulte la [[!DNL Cross-Device Analytics] documentación de ayuda](https://docs.adobe.com/content/help/es-ES/analytics/components/cda/cda-home.html).
