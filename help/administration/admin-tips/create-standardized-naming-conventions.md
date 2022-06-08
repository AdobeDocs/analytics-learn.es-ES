---
title: Crear convenciones de nomenclatura estandarizadas
description: Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en la interfaz de usuario de administración de AA y a los valores pasados a la dimensión.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Crear convenciones de nomenclatura estandarizadas

**QUÉ:** Las convenciones de nomenclatura estandarizadas se aplican al propio nombre de la variable cuando se habilita en la interfaz de administración de Adobe Analytics (AA) y a los valores pasados a la dimensión. (es decir, los nombres de página serían &quot;nombre de página (v1)&quot; como nombre de variable y los valores de nombre de página pasados deberían ser uniformes y seguir una estructura o jerarquía específica como &quot;nombre de sitio|página principal&quot; o &quot;nombre de sitio|búsqueda|resultados de búsqueda&quot;).

**POR QUÉ:** Las convenciones de nomenclatura son una buena manera de mantener todo uniforme y de mantener la interfaz fácil de entender para los usuarios. Si los crea desde el principio y los aplica en la plataforma y el código, será más fácil escalarlos.

**CÓMO:** La interfaz y el documento de etiquetado deben coincidir tanto con &quot;Nombre&quot; como con &quot;Descripción&quot;. Esto evitará que los usuarios tengan que extraer un documento de Excel y les permitirá comprender sus datos directamente en la interfaz. También se recomienda mantener todo en minúsculas para mantener la coherencia.

Siempre es mejor mantener los nombres de página coherentes en toda la plataforma también (o nombres de pantalla para aplicaciones). Por ejemplo, puede establecer la propiedad:section:subsección:subsección:nombre de página único&quot; en una variable o dimensión. Si todos estos son campos independientes en la capa de datos, incluso puede crear el nombre de página directamente en el archivo JS/Launch. Tener todos estos elementos configurados también en sus propias dimensiones puede ayudarle a desglosar las propiedades o áreas específicas del sitio o aplicación más fácilmente, y a comprender mejor el tráfico y los flujos.

Cualquier cosa que facilite a los usuarios encontrar y comprender los datos, incluidas convenciones de nomenclatura tan sencillas, aumentará el uso de Adobe Analytics y proporcionará mejores perspectivas para el negocio.

## Autores

Este documento fue coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock, campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora senior en Adobe
