---
title: Use un grupo de informes globales
description: Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar de verdad la implementación.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: 490addfd-b810-4f15-b065-e0e58048c882
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: ht
source-wordcount: '763'
ht-degree: 100%

---

# Use un grupo de informes globales

**QUÉ:** Es tentador crear grupos de informes para cada uno de sus sitios, pero esto puede convertirse rápido en su peor pesadilla, tanto en términos de complicar la creación de informes como de la implementación. Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar de verdad la implementación.

**POR QUÉ:** Crear un grupo de informes globales es la única opción para tener una vista unificada de las propiedades digitales y los recorridos de los usuarios en cada propiedad. Si tiene una aplicación móvil y un sitio web, siempre debe combinar los datos de la aplicación y los datos web en un grupo de informes. Así, aprovecha los recorridos multidispositivo y rastrea a quienes visitan ambas propiedades como un único visitante, en lugar de con grupos de informes separados, donde tendría un conjunto de datos desenlazados que mostraría 2 visitantes (1 de cada propiedad), sin forma de conocer el cruce.

Estas son las ventajas y desventajas de tener un único grupo de informes, para ayudarle a sopesar las opciones:

* PROS:
   * Poder entender el panorama digital completo fácilmente. Si ha implementado la dimensión “propiedades” (eVar) a la que se hace referencia en otras sugerencias, podrá obtener con sencillez una sola vista de todos sus sitios y aplicaciones, tráfico y conversiones. Ver este panorama general es clave para comprender su negocio en general.
   * En el mismo sentido, ahora puede ver cómo fluyen los usuarios entre todas las propiedades y comprender su recorrido a través del entorno digital.
   * Facilidad de administración. Cuando utilice varios grupos de informes, deberá mantener la interfaz en varios lugares, así como varios documentos de etiquetado (o uno más complicado). Tener todo en un sitio significa que solo hay que actualizar un sitio. También facilita mucho la concesión de acceso.
   * Mejor facilidad de uso de la interfaz. Si los usuarios solo pueden ir a un lugar, no necesitan pensar qué grupo de informes seleccionar. Tenga en cuenta que no puede usar varios grupos de informes en el mismo panel del espacio de trabajo y que, si hay varios, puede confundir a los usuarios.
   * Menos llamadas al servidor = menos costes. Si ejecuta llamadas a varios grupos de informes, aumenta los costes. Si la implementación es sencilla, también se reducirán los gastos.
   * Puede, simplemente, aprovechar los grupos de informes virtuales (VRS) para dividir los datos específicos del sitio en el grupo de informes globales y disminuir los permisos de usuario basados en un VRS si es necesario. Una vez que los datos se separan en grupos de informes individuales, no se pueden reagrupar. No obstante, si ya se han unido en un conjunto de datos (RS global), se pueden desglosar cómodamente.
* CONTRAS:
   * Si tiene propiedades muy separadas y los usuarios no pasan de una a otra ni se espera que lo hagan, es posible que quiera tener grupos de informes separados.
   * Si las propiedades tienen necesidades de etiquetado y creación de informes muy diferentes, puede ser recomendable configurar grupos de informes separados en aras de la eficiencia de las variables. Tener grupos de informes separados le dará más flexibilidad para usar variables personalizadas (más eVars).
   * Excesos en la cantidad de valores exclusivos: la interfaz de Adobe Analytics solo le permite ver 500 000 valores únicos dentro de una sola dimensión durante un período de tiempo determinado. Una vez superada esta cifra, los valores se agrupan como “excesos en la cantidad de valores exclusivos” o “bajo tráfico” en la interfaz. Estos valores permanecen disponibles en el servidor (es decir, el almacén de datos o fuentes de datos), pero no se pueden visualizar en la interfaz. Si tiene datos muy granulares (como ID de usuario, PSN, etc.), es fácil alcanzar este nivel. Tener grupos de informes separados puede ayudar con este problema.

**CÓMO:** Comenzar con una nueva implementación de AA y utilizar un grupo de informes globales es sencillo y directo. Solo necesita crear el grupo de informes globales (uno para Desarrollo y otro para Producción) en la IU de administración de AA y aplicar los mismos valores de ID del grupo de informes (RSID) en todas sus propiedades.

La migración desde una estrategia de etiquetado múltiple con un grupo de informes único por propiedad requiere más organización y planificación. Algunas de las consideraciones que debe tener en cuenta:

* Alinee las variables (es decir, el eVar1 en la Propiedad A debe capturar el mismo punto de datos que el eVar1 en la Propiedad B)
* Consolide cualquier regla de procesamiento, regla de canal de marketing o clasificación (SAINT y Generador de reglas)
* Migre las fuentes de datos
* Elija una fecha de corte y comuníquela a todos los usuarios de la empresa

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock, campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en Adobe
