---
title: Usar un grupo de informes globales
description: Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar realmente la implementación.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---


# Usar un grupo de informes globales

**QUÉ:** Es tentador crear grupos de informes para cada uno de sus sitios, pero esto puede convertirse rápidamente en su peor pesadilla, tanto en términos de complicar los informes como de la implementación. Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar realmente la implementación.

**POR QUÉ:** Crear un grupo de informes globales es la única opción para tener una vista unificada de las propiedades digitales y los recorridos de los usuarios en cada propiedad. Si tiene una aplicación móvil y un sitio web, siempre debe combinar los datos de la aplicación y los datos web en un grupo de informes para aprovechar los recorridos entre dispositivos y rastrear a aquellos que visitan ambas propiedades como un único visitante, en lugar de con grupos de informes separados, donde tendría un conjunto de datos desenlazados que mostrara 2 visitantes (1 cada propiedad) sin forma de conocer el cruce.

Estas son las ventajas y desventajas de tener un único grupo de informes para ayudarle a sopesar sus opciones:

* PROS:
   * Poder entender el paisaje digital completo fácilmente. Si ha implementado la dimensión &quot;propiedades&quot; (eVar) a la que se hace referencia en otras sugerencias, podrá obtener fácilmente una sola vista de todos sus sitios y aplicaciones, tráfico y conversiones. Tener este panorama general es clave para comprender su negocio en general.
   * En el mismo sentido, ahora puede ver cómo fluyen los usuarios entre todas sus propiedades y comprender su recorrido a través de su entorno digital.
   * Facilidad de administración. Cuando utilice varios grupos de informes, deberá mantener la interfaz en varios lugares, así como varios documentos de etiquetado (o uno más complicado). Mantener todo en un lugar significa que hay un solo lugar para hacer actualizaciones. También facilita mucho la concesión de acceso.
   * Mejor facilidad de uso en la interfaz. Si los usuarios solo tienen un lugar donde ir, no necesitan pensar en qué grupo de informes seleccionar. Tenga en cuenta que no puede usar varios grupos de informes en el mismo panel del espacio de trabajo, y que varios de ellos pueden confundir a los usuarios.
   * Menos llamadas al servidor = menos costes. Si realiza llamadas a varios grupos de informes, aumente sus costes. Si mantiene la implementación sencilla, también reducirá los costes.
   * Simplemente puede aprovechar los grupos de informes virtuales (VRS) para dividir los datos específicos del sitio en el grupo de informes globales y reducir los permisos de usuario basados en un VRS si es necesario. Una vez que los datos se separan en grupos de informes individuales, no se pueden resumir, pero si ya se han unido en un conjunto de datos (RS global), se pueden desglosar fácilmente.
* CONS:
   * Si tiene propiedades muy independientes en las que los usuarios no se cortan de uno a otro y no se espera que lo hagan nunca, es posible que desee mantener grupos de informes separados.
   * Si las propiedades tienen necesidades de etiquetado y creación de informes muy diferentes, puede ser recomendable configurar grupos de informes separados en aras de la eficiencia de las variables. Tener grupos de informes separados le dará más flexibilidad para usar variables personalizadas (más eVars).
   * Se excedió la cantidad de valores exclusivos: La interfaz de Adobe Analytics solo le permite ver 500 000 valores únicos dentro de una sola dimensión durante un período de tiempo determinado. Una vez superada esta cifra, los valores se agrupan como &quot;únicos excedidos&quot; o &quot;poco tráfico&quot; en la interfaz. Estos valores permanecen disponibles en el servidor (es decir, Data Warehouse, fuentes de datos), pero no se pueden visualizar en la interfaz. Si tiene datos muy granulares (como ID de usuario, PSN, etc.), es fácil alcanzar este nivel. Tener grupos de informes separados puede ayudar con este problema.

**CÓMO:** Comenzar con una nueva implementación AA y utilizar un grupo de informes globales es sencillo y sencillo. Solo necesita crear el grupo de informes globales (uno para Dev y otro para Prod) en la interfaz de usuario de administración de AA y aplicar los mismos valores de ID de grupo de informes (RSID) en todas sus propiedades.

La migración desde una estrategia de etiquetado múltiple con un grupo de informes único por propiedad requiere más estrategia y planificación. Algunas de las consideraciones que debe tener en cuenta:

* Alinear las variables (es decir, el eVar1 en la Propiedad A debe capturar el mismo punto de datos que el eVar1 en la Propiedad B)
* Consolidación de cualquier regla de procesamiento, regla de canal de marketing o clasificación (SAINT y Generador de reglas)
* Migración de fuentes de datos y fuentes de datos
* Elección de una fecha de corte y comunicación con todos los usuarios del negocio

## Autores

Este documento fue coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock, campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora senior en Adobe
