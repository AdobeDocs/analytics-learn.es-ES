---
title: Descargue el manual de implementación de Adobe Analytics
description: Un Documento de requisitos empresariales (denominado comúnmente BRD) es una documentación muy importante en la que los principales actores, los usuarios empresariales y los usuarios tecnológicos querrán colaborar. Es un sitio para documentar todos los KPI deseados, los requisitos de creación de informes y cualquier punto de datos que desee ver cuando se complete la implementación de AA.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
exl-id: aab53a12-3f11-49c9-aba4-dc926bcf776b
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '1802'
ht-degree: 99%

---

# Descargue el manual de implementación de Adobe Analytics

Antes de empezar, [descargue el manual de implementación](assets/aa-implementation-playbook.xlsx).

## Pestaña Requisitos empresariales

**QUÉ:** Un Documento de requisitos empresariales (denominado comúnmente BRD) es una documentación muy importante en la que los principales actores, los usuarios empresariales y los usuarios tecnológicos querrán colaborar. Es un sitio para documentar todos los KPI deseados, los requisitos de creación de informes y cualquier punto de datos que desee ver cuando se complete la implementación de Adobe Analytics (AA).

**POR QUÉ:** Esto sirve como punto de partida para la documentación siguiente (SDR, especificaciones técnicas, etc.) y es una fuente fiable común para un estado final de AA acordado. Este documento organiza las ideas entre los equipos de la organización para formar una guía que le lleve a avanzar en la creación o mejora de su implementación.

**CÓMO:** La documentación de los requisitos empresariales la suelen elaborar los usuarios empresariales finales de AA, pero es importante recibir comentarios de los usuarios tecnológicos, ya que puede haber desafíos técnicos que tener en cuenta y algunos puntos de datos pueden requerir más esfuerzo que otros, lo que influye en la priorización.

Pregúntese “qué que queremos rastrear en nuestro sitio”, “qué puntos de datos serán importantes para mí en el uso de los informes” y, lo más importante, “cómo informarán estos puntos de datos las decisiones”. Es importante asegurarse de que cada uno de los requisitos empresariales esté relacionado con un punto de datos que pueda utilizarse para informar las decisiones empresariales. Por ejemplo, puede ser tentador querer rastrear cada clic en el sitio, pero, al final, ¿qué datos se obtienen de ese informe?

Comience por rellenar la columna C en la captura de pantalla siguiente (Requisito empresarial). Esto debería ser algo como “Cuántas búsquedas internas se completan en nuestro sitio” o “Qué campaña interna es más efectiva en términos de impresiones”. Después de completar este nivel de detalle, puede volver atrás y rellenar la columna B (Categoría) y agrupar los requisitos en categorías como “Búsqueda” o “Promoción interna”, que deberían corresponder perfectamente con las secciones de especificaciones técnicas.

También indicará si cree que el uso de un eVar, evento, propiedad o combinación logrará lo que busca rastrear.

Y, por último, la columna Estado de implementación servirá como una comprobación de estado cuando comience a añadir cosas al sitio.

![Documento de requisitos empresariales](assets/brd-template.png)

## Pestaña Mapa de variables (documentación de etiquetado/SDR)

**QUÉ:** Un documento de etiquetado (conocido comúnmente como SDR) es una documentación fundamental que resulta útil tanto para los usuarios técnicos como para los usuarios empresariales de AA. Enumera todas las variables que utilizan los grupos de informes junto con todos los detalles relevantes para la configuración de variables, cómo se implementa la variable y cuál es su propósito en la creación de informes. Al igual que el documento de propiedades, debe ser un documento de Excel activo y bien controlado, con una persona responsable de mantenerlo actualizado a medida que se introduzcan mejoras de etiquetado o cambios de implementación.

**POR QUÉ:** Este documento tendrá muchos propósitos, pero los más importantes son los siguientes:

* Para cualquier persona nueva en su implementación (nuevo empleado, propietario del negocio que busque comprender mejor los informes disponibles, etc.), este documento proporciona la mejor vista de todas las variables implementadas y cuál es su propósito para que las personas puedan autoabastecerse en términos de aprendizaje de la configuración de AA.
* Para el propietario/usuario técnico del producto de AA, este documento sirve como recordatorio de cómo se configuran otras variables y cuáles están disponibles para usarse al añadir una nueva dimensión.

**CÓMO:** Comience enumerando todas las variables de Adobe predeterminadas (página, producto, ubicación geográfica, etc.), así como eVars, props, eventos y variables de lista en un documento de Excel. Debe tener una pestaña por sitio o grupo de informes.
Para cada una de estas dimensiones, añado las siguientes columnas:
* **Nombre:** proporcione un nombre sencillo y corto que la mayoría pueda entender. Debería ser lo bastante intuitivo como para que un nuevo usuario pueda leerlo y comprender qué es lo que pretende capturar la variable.
* **Descripción:** más información sobre para qué se utiliza la variable y qué datos rastrea. Lo dejo corto y simple y hago que coincida con la descripción utilizada en la interfaz. Lo ideal es que mis usuarios no necesiten consultar el documento de etiquetado. Por lo tanto, cuando se configura una nueva dimensión en el servidor de administración, añado la misma descripción allí. De este modo, el usuario puede pulsar el icono de información directamente en el espacio de trabajo para comprender qué es una dimensión: no es necesario ir a un documento de Excel.

![URL de página simplificada](assets/page-url-simplified.png)

* **Código:** el código del servidor que establece el valor. Puede ser el campo de la capa de datos de la página o puede llamar para que esto se haga con una regla de Launch, una regla de procesamiento, etc.
* **Informes de clasificación:** llame a cualquier informe de clasificación que se ejecute con el Importador de clasificaciones o el Generador de reglas de clasificación
* **Ámbito de la solución:** encuentro útil enumerar todas las propiedades (al menos las que usan más que variables estándar) en columnas pequeñas y añadir una marca de verificación para cada dimensión configurada en esa propiedad. Esto le permitirá filtrar con facilidad por una propiedad específica, así como ver rápidamente dónde se está configurando una dimensión en particular.
* **Configuración:** configuración de la IU de administración para cada variable (es decir, para eVars: caducidad, asignación, comercialización, etc.)

Captura de pantalla de la muestra de SDR:
![Muestra de SDR](assets/sample-sdr.png)

También se recomienda utilizar este documento de etiquetado para llevar a cabo un seguimiento de cualquier variable gratuita y cualquiera “no deseada”. Cuando una dimensión ya no es útil, el desarrollador suele necesitar un tiempo para eliminarla. Incluso después de eso, puede almacenarse en caché, o puede que se dé cuenta de que la dimensión también se estaba configurando en otra parte. Limpiar las dimensiones no es fácil y, a menudo, requiere paciencia. Aquí hay algunos consejos para esconder la basura debajo de la alfombra y que sus usuarios no se confundan, al tiempo que mantiene un seguimiento.

* Todas las dimensiones/eventos que no se utilizan están “libres” o “en proceso de eliminación”
   * Si la dimensión tiene valores no deseados en los últimos 90 días, está “en proceso de eliminación”
   * Si la dimensión está libre y limpia durante al menos los últimos 90 días, está “libre”
   * Márquelas como tal en “Nombre”, en el documento de etiquetado, para que pueda filtrarlas fácilmente. Yo tengo estas etiquetas desmarcadas en el documento de etiquetado (filtro de datos de Excel) para que los usuarios no las vean
   * Márquelas como el nombre del eVar en la interfaz para que los usuarios no las encuentren en una búsqueda (como “(v6)”) y elimine la descripción
* Al hacer esto, cuando se necesita una nueva dimensión, se puede filtrar fácilmente por “libre” en la columna Nombre para encontrar una limpia que utilizar
* Para las dimensiones y eventos “en proceso de eliminación”, recomiendo que realice un seguimiento de estos eventos mediante el espacio de trabajo:
   * Cree un proyecto visible para los administradores solo con 3 tablas: eVars, props y eventos. Utilizo “instancias” para eVars específicos y, para las props, creo segmentos VISITA con “prop5 existe”, por ejemplo.
   * Establezca la fecha en Últimos 90 días
   * Utilice lo anterior como filas en las 3 tablas, junto con ocurrencias
   * Tan pronto como algo llega a “0”, lo marco como “libre” en el documento de etiquetado y lo elimino del proyecto del espacio de trabajo

De este modo, los datos siempre están limpios y tiene una idea clara de qué es basura.

![Información general sobre variables y eventos](assets/variables-and-events-overview.png)

## Pestaña Propiedades

**QUÉ:** Un documento de propiedades debe enumerar todas sus propiedades digitales: sitios web, aplicaciones móviles, otras herramientas (chat, comentarios, etc.), independientemente de si están etiquetadas con Adobe Analytics o no. Esto debería servir como un documento centralizado y vivo entre los usuarios empresariales y tecnológicos.

**POR QUÉ:** Esto le proporcionará una visión clara del recorrido del usuario en todas las propiedades digitales, así como lo que Adobe Analytics cubre y no cubre, para que pueda empezar a priorizar la adición de etiquetado a cualquier propiedad donde falte. Al presentar el ecosistema digital de esta manera, puede identificar posibles oportunidades en la estrategia de etiquetado para obtener una visión completa del recorrido del usuario. Por ejemplo, ¿necesita un grupo de informes globales para seguir varios dominios o sitios? ¿Se necesita un traspaso de ID de visitante entre dominios o aplicaciones para una experiencia híbrida? ¿Es necesario actualizar los filtros de URL internos para el seguimiento entre dominios?

**CÓMO:** Identifique a un propietario del documento para dar control y una única fuente de responsabilidad en la administración de actualizaciones.
Enumere lo siguiente en la pestaña Propiedades:
* **Nombre de la propiedad:** puede ser un nombre de dominio, subdominio, aplicación, etc. Incluso dentro del mismo dominio, si algunas partes se administran por separado (como, por ejemplo, por un equipo o una tecnología diferentes), deberían separarse.
* **Vínculo (URL)** a la propiedad donde esté disponible
* **Propietario y contactos:** enumere el propietario principal o los contactos de la propiedad
* **Método de etiqueta:** muchos tenemos diferentes métodos e implementaciones de código (Launch, archivos JS, AEP, etc.). Puede desglosar esto más si es necesario (por ejemplo, por versión de código o sistema de administración de etiquetas), pero está pensado para ejecutar un seguimiento de todos los métodos y versiones de código diferentes, dónde debe actualizarse el código y cómo debe mantenerse. Si utiliza Adobe Launch, indique el nombre de la propiedad de Launch.

Recuerde incluir todas las propiedades digitales, aunque no estén etiquetadas con Adobe Analytics. Esto le ayudará a comprender su entorno digital y cómo sus usuarios interactúan con todas las propiedades.

Se recomienda mantener este documento lo más simple posible y no saturarlo con demasiada información para que sea fácil de interpretar por diferentes partes de la organización. Los equipos de Analytics, a menudo, comprenden mejor el panorama digital que cualquier otro equipo, por lo que otros equipos y ejecutivos suelen utilizar este documento para facilitar una descripción general exhaustiva.

>[!TIP]
>
>Cree una dimensión de nombre/propiedad de sitio en Adobe Analytics. Tener una dimensión dedicada (normalmente un eVar) en Adobe Analytics que identifique el nombre del sitio o la aplicación facultará la segmentación, la resolución de problemas, la creación de grupos de informes virtuales, etc. Las ventajas son infinitas, sobre todo cuando se combinan varios sitios en un grupo de informes (global). La clave es garantizar que los equipos de desarrollo siempre fijen este valor en la dimensión de propiedades, incluidas todas las cargas de página (llamadas s.t/trackState) y todos los eventos personalizados (llamadas s.tl/trackAction). Las reglas de procesamiento pueden ser una herramienta útil para configurar estos valores de forma correcta y coherente.

[Vea este vídeo de Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=es){target="_blank"} para obtener más información sobre cómo rellenar el manual de implementación.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock, campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en Adobe
