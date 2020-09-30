---
title: 'Explicación y uso de IQ de viaje: análisis entre dispositivos'
description: Cuando los usuarios interactúan con su marca, lo hacen de muchas formas y en varios dispositivos. Análisis entre dispositivos se integra con el servicio de identidad de Adobe Experience Platform para identificar cómo se asignan los dispositivos a las personas. A continuación, aprovecha esta inteligencia para crear una vista de comportamiento entre dispositivos. Esto resulta en poder hacer análisis en personas, no en dispositivos.
feature: cda
topics: null
audience: all
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 6%

---


# Explicación y uso [!DNL Journey IQ] : análisis entre dispositivos

Cuando los usuarios interactúan con su marca, lo hacen de muchas formas y en varios dispositivos. Análisis entre dispositivos se integra con el [!DNL Adobe Experience Platform Identity Service] para identificar cómo se asignan los dispositivos a las personas. A continuación, aprovecha esta inteligencia para crear una vista de comportamiento entre dispositivos. Esto resulta en poder hacer análisis en personas, no en dispositivos.

## Información general sobre los análisis entre dispositivos

### No soy mi dispositivo

Cuando los usuarios interactúan con su marca, lo hacen de muchas maneras y en varias &quot;superficies&quot; o &quot;dispositivos&quot;. Pueden utilizar un navegador web en un ordenador o dispositivo móvil, o bien una aplicación móvil. En el análisis digital tradicional, que creció en la recopilación de datos basada en cookies, cada una de estas superficies se representa como un &quot;visitante&quot; único. Esto significa que cada uno de sus usuarios humanos está representado como un visitante único múltiple.

A continuación, se muestra un ejemplo. Supongamos que Isabelle interactuó con su marca de la siguiente manera:

*Isabelle hace tres viajes de análisis*![tradicionales de visitantes](assets/cda-isabelle-journey-traditional-analytics.png)

Utilizando análisis tradicionales, el viaje de Isabelle se fractura en tres piezas. Está representada como tres visitantes únicos, cada uno de los cuales utilizó un dispositivo diferente para realizar tareas aisladas. Lo que se necesita es una vista unificada y entre dispositivos de las interacciones de Isabelle. [!DNL Journey IQ: Cross-Device Analytics] proporciona esta vista.

*Isabelle es una persona* que realiza un viaje de análisis![entre dispositivos](assets/cda-isabelle-journey-cross-device-analytics.png)

### Una Vista entre dispositivos ofrece mejores análisis

Tener una vista personalizada y entre dispositivos de la conducta de Isabelle puede marcar una diferencia significativa en tu análisis. Por ejemplo, el enfoque tradicional basado en el visitante no ofrece una imagen completa de la efectividad del canal de mercadotecnia. Veamos el viaje de Isabelle una vez más, centrándonos en qué canal recibe crédito por su vista de productos y por su compra. Usaremos la atribución de [!UICONTROL último toque] para simplificar, pero el mismo problema ocurre con cualquier modelo de atribución cuando se divide el comportamiento de Isabelle en visitantes separados. El uso de la tradicional vista del mundo basada en el visitante da resultados muy diferentes, incluso engañosos:

*Atribución de Analytics tradicional frente a atribución de*![canales entre dispositivos de Analytics](assets/channel-attribution.png)

Observe que con la vista entre dispositivos, el canal de correo electrónico recibe crédito tanto por la vista del producto como por la compra, lo que representa con mayor precisión la experiencia real de Isabelle.

Siga leyendo para conocer:

* How [!DNL Cross-Device Analytics] Works
* Requisitos Previos Para [!DNL Cross-Device Analytics]
* Interpretación de datos entre dispositivos
* Análisis de datos entre dispositivos en Analysis Workspace

## How [!DNL Cross-Device Analytics] Works

[!DNL Journey IQ: Cross-Device Analytics (CDA)] se integra con el [!DNL Adobe Experience Platform Identity Service], utilizando el [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/es-ES/device-co-op/using/home.html) o [!DNL Private Graph] para identificar cómo los dispositivos se asignan a las personas. A continuación, aprovecha esta inteligencia para crear una vista de comportamiento entre dispositivos. CDA incluye funciones y herramientas sin igual para ayudar a su empresa a comprender el uso de varios dispositivos y la experiencia del cliente en todos ellos en sus interacciones con su marca. Se sitúa bajo Analysis Workspace para proporcionar una perspectiva profunda sobre la análisis de audiencias basada en persona y la atribución, segmentación y análisis del viaje entre dispositivos mediante herramientas poderosas como [!UICONTROL Visitas en el orden previsto], [!DNL Flow], [!DNL Cohort]y [!DNL Segment IQ] [!DNL Attribution IQ].

### The [!DNL Cross-Device Virtual Report Suite]

CDA se presenta a través de un tipo especial de grupo [[!UICONTROL de informes]](https://docs.adobe.com/content/help/es-ES/analytics/components/virtual-report-suites/vrs-about.html)virtuales entre dispositivos. Esto le permite seguir utilizando el grupo de informes original basado en dispositivos a medida que introduce análisis entre dispositivos en su organización. La configuración de un VRS CDA es fácil.

En el paso uno del generador de VRS, elija el grupo [!UICONTROL de] informes configurado por Adobe como CDA habilitado:

*Elija un grupo de[!UICONTROL informes base (fuente) habilitado para CDA]* Grupo![[!UICONTROL de informes] virtuales Paso uno](assets/cda-vrs-step-one.png)

A continuación, active Procesamiento [!UICONTROL de intervalo] de tiempo y habilite la vinculación [!UICONTROL entre dispositivos]:

*Habilitar el procesamiento[!UICONTROL de tiempo de]informe y la vinculación[!UICONTROL entre dispositivos y grupos]* de informes![ virtuales Paso dos](assets/cda-vrs-step-two.png)

Finalice la configuración del VRS y guárdelo. El VRS de CDA se mostrará en Analysis Workspace con un icono especial junto al mismo, como se muestra a continuación:

*Seleccione el VRS de CDA en el tercer paso del grupo* de informes![[!UICONTROL virtuales de Analysis Workspace]](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Puede crear tantos grupos [!UICONTROL de informes] virtuales CDA como desee en la parte superior del grupo [!UICONTROL de]informes base habilitado para CDA.

### Restauración del historial

A veces, los usuarios tardan un tiempo en iniciar sesión y en hacerlo [!DNL Co-op Graph] o en [!DNL Private Graph] identificarlos y asignar juntos sus dispositivos. El CDA utiliza una ventana retrospectiva de 30 días, que le permite reafirmar un visitante no identificado anteriormente como una persona hasta 30 días antes.

¿Cómo ayuda esto? Recuerden el viaje de la usuaria Isabelle desde la discusión de arriba:

![[!DNL Cross-Device Analytics] Viaje](assets/cda-isabelle-journey-cross-device-analytics.png)

Es posible que Isabelle no haya iniciado sesión hasta justo antes de realizar la compra, y que el [!DNL Co-op Graph] o [!DNL Private Graph] no haya cartografiado juntos los dispositivos de Isabelle hasta algún momento después de su compra. Pero el retroceso de 30 días de la CDA permite a la CDA reafirmar el comportamiento de Isabelle a nivel personal, proporcionándole la vista entre dispositivos de su viaje que usted necesita.

>[!NOTE]
>
>Debido a que se puede replantear el historial, esto significa que los datos pueden cambiar con el tiempo en un grupo [!UICONTROL de informes]virtuales habilitado para CDA. Tenga esto en cuenta a medida que comunica perspectivas desde una análisis basada en CDA.

## Requisitos Previos Para El Análisis [!UICONTROL Entre Dispositivos]

CDA se incluye con [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). A partir de septiembre de 2019, [!DNL Analytics Ultimate] los clientes que cumplen los requisitos previos enumerados a continuación pueden utilizar CDA. Los requisitos previos para CDA son los siguientes:

* Su compañía debe ser miembro del [!DNL Adobe Experience Platform Identity Service] [!DNL Co-op Graph] [, o usar un](https://docs.adobe.com/content/help/es-ES/device-co-op/using/home.html)[!DNL Adobe Experience Platform Identity Service Private Graph].
* Debe implementar todo lo necesario para [!DNL Co-op Graph] o [!DNL Private Graph] incluir el ID de [Experience Cloud (ECID)](https://docs.adobe.com/content/help/es-ES/id-service/using/home.html) y la sincronización de ID con el gráfico. Tenga en cuenta que, además de los requisitos técnicos, la Comisión [!DNL Co-op Graph] tiene otros requisitos legales y contractuales.
* Actualmente no es posible utilizar dos organizaciones IMS con una sola [!DNL Private Graph], por lo que debe estandarizar en una sola organización IMS. En algunos casos, es posible que un cliente con varias organizaciones IMS utilice la [!DNL Co-op Graph] junto con CDA.
* El [!DNL Co-op graph] y [!DNL Private Graph], así como ciertos componentes del CDA, están alojados en [!DNL Microsoft Azure]. Esto significa que [!DNL Analytics] los datos se copian de un lado a otro entre el centro de procesamiento de datos del Adobe y la presencia del Adobe en [!DNL Microsoft Azure]. Algunos [!DNL Analytics] datos se almacenarán en [!DNL Azure]. Su compañía debe aceptar este acuerdo.
* CDA requiere un grupo [!UICONTROL de]informes &quot;entre dispositivos&quot;. Es decir, el grupo [!UICONTROL de] informes que utilice para CDA debe incluir datos de varios tipos de dispositivos o &quot;superficies&quot; diferentes, como la web de escritorio, la web móvil y la aplicación móvil. A partir de septiembre de 2019, el volumen de llamadas al servidor para este grupo [!UICONTROL de] informes debe ser igual o inferior a 100 millones de llamadas al servidor. (Los límites del volumen de llamadas al servidor aumentarán en los próximos meses).
* A partir de septiembre de 2019, el [!DNL Co-op Graph] y [!DNL Private Graph] solo está disponible en Norteamérica. El calendario para la presencia de gráficos en EMEA y APAC se anunciará en el futuro. Si se encuentra en esas regiones, le animamos a que tenga inicios para ver estos requisitos previos ahora, de modo que esté listo para ir cuando el gráfico esté disponible.

## Interpretación de datos entre dispositivos

### Personas no Visitantes

Dentro del grupo [!UICONTROL de informes]virtuales CDA, verá algunos cambios. Por ejemplo, la métrica Visitantes  únicos se reemplaza por dos métricas nuevas: [!UICONTROL Personas] y dispositivos únicos. Estas nuevas métricas le proporcionan una perspectiva mucho mejor sobre el tamaño de la audiencia.

*Métrica Personas y Dispositivos*&#x200B;únicos![CDA [!UICONTROL Personas]](assets/cda-people-metric.png)

En el Generador [[!UICONTROL de]](https://docs.adobe.com/content/help/es-ES/analytics/components/segmentation/segmentation-workflow/seg-build.html)segmentos, el contenedor de segmentos de [!UICONTROL Visitante] se ha sustituido por un contenedor de segmentos de [!UICONTROL persona] . Con un VRS CDA, puede crear segmentos entre dispositivos como:

* Personas que utilizan más de un dispositivo
* Personas que comienzan su viaje en un dispositivo móvil y luego compran en un dispositivo de escritorio
* Visitas en las que las personas utilizan más de un dispositivo para realizar una tarea

*Contenedor de segmentos*![[!DNL Segment Builder] personales [!UICONTROL Persona]](assets/cda-segment-builder-person-container.png)

### Persistencia del Dimension

Dentro de un VRS CDA, las dimensiones como [!DNL eVars] ahora persisten automáticamente en todos los dispositivos. Por ejemplo, un [!DNL eVar] que esté configurado como:

* Asignación: Más reciente (última)
* Caduca después de: Compra

ahora persistirá automáticamente de un dispositivo a otro hasta que se active el evento de compra.

## Análisis de datos entre dispositivos en Analysis Workspace

### Análisis de Audiencia basada en personas

¿Alguna vez te has preguntado cuántas personas interactúan con tu marca? ¿Ha querido comprender cuántos y qué tipo de dispositivos utilizan? ¿Cómo se superpone su uso? Con un VRS CDA, puede crear diagramas [de](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/venn.html) Venn entre dispositivos e [histogramas](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/histogram.html)de dispositivos por persona.

*Análisis* de audiencia basada en persona![Venn e histograma](assets/cda-venn-and-histogram.png)

### Dispositivo cruzado [!DNL Flow]

Con CDA y Analysis Workspace, puede visualizar cómo se mueven las personas de un dispositivo a otro con el paso del tiempo en la visualización de flujo [[!DNL]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Pueden ver dónde abandonan en su viaje y dónde siguen.

*[!DNL Flow]con CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Dispositivo cruzado [!DNL Fallout]

Es probable que utilice varias [[!Visualizaciones de visitas en el orden previsto de DNL]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) para analizar la eficacia de los usuarios en una serie determinada de pasos antes de lograr el éxito. ¿Sabía que la vista de estos datos [!DNL Fallout visualizations] es limitada al usar análisis tradicionales basados en dispositivos? Para que la visita en el orden previsto se realice correctamente, el siguiente paso debe darse en el mismo navegador o aplicación que el paso anterior. En los análisis basados en dispositivos, no ve a las personas que completan correctamente el siguiente paso en otro dispositivo.

No te preocupes, CDA te ha cubierto. CDA crea la vista entre dispositivos que hace [!DNL Fallout visualizations] mucho más útil. Después de todo, lo que realmente importa es si la persona finalmente tuvo éxito en su tarea en algún lugar.

*[!DNL Fallout]con CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Debido a que CDA crea una capa de datos entre dispositivos debajo de Analysis Workspace, toda la análisis estará condimentada con una perspectiva entre dispositivos. Un ejemplo poderoso es el de [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] en Analysis Workspace permite comparar varios modelos de atribución en paralelo. Con esta capacidad con CDA, ahora puede comparar cómo diferentes dispositivos contribuyen al éxito.

Por ejemplo, supongamos que desea saber con qué frecuencia un teléfono móvil es el primer dispositivo utilizado en una interacción que, en última instancia, conduce al éxito. Esto representa la &quot;tasa de adquisición&quot; del teléfono móvil. CDA + [!DNL Attribution IQ] le permite realizar esta análisis:

*[!DNL Attribution IQ]con CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

For more information, see the [[!DNL Cross-Device Analytics] help documentation](https://docs.adobe.com/content/help/es-ES/analytics/components/cda/cda-home.html).
