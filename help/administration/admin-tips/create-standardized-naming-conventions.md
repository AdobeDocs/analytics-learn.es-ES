---
title: Cree convenciones de nomenclatura estandarizada
description: Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en la IU de administración de AA y a los valores pasados a la dimensión.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 0fe3b981-0d9b-4f12-a6ca-63a4140f4baf
TQID: https://experienceleague.adobe.com/nnAluH2AvqNbWEPk3lbthk-xDl-tnqyW8uHg4Beurq0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 78%

---

# Cree convenciones de nomenclatura estandarizada

**QUÉ:** Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en la IU de administración de Adobe Analytics (AA) y a los valores pasados a la dimensión. (es decir, los nombres de página serían “nombre de página (v1)” como nombre de variable y los valores de nombre de página pasados deberían ser uniformes y seguir una estructura o jerarquía específica como “nombre de sitio|página principal” o “nombre de sitio|búsqueda|resultados de búsqueda”).

**POR QUÉ:** Las convenciones de nomenclatura son una buena manera de mantener todo uniforme y que la interfaz sea fácil de entender para los usuarios. Si las crea desde el principio y las aplica en la plataforma y el código, será más fácil escalarlas.

**CÓMO:** La interfaz y el documento de etiquetado deben coincidir tanto en &quot;Nombre&quot; como en &quot;Descripción&quot;. Esto evitará que los usuarios tengan que ir a un documento de Excel y les permitirá comprender los datos directamente en la interfaz. También se recomienda escribir todo en minúsculas para mantener la coherencia.

Siempre es mejor que los nombres de las páginas sean coherentes en toda la plataforma (o los nombres de las pantallas para las aplicaciones). Por ejemplo, puede establecer `property:section:sub section:sub sub section:unique page name` en una variable o dimensión. Si todos estos son campos independientes en la capa de datos, incluso puede crear el nombre de página directamente en el archivo JS/Launch. Tener todos estos elementos configurados también en sus propias dimensiones puede ayudarle a desglosar las propiedades o áreas específicas del sitio o aplicación con mayor facilidad y a comprender mejor el tráfico y los flujos.

Cualquier cosa que facilite a los usuarios encontrar y comprender los datos, incluidas convenciones de nomenclatura tan sencillas, aumentará el uso de Adobe Analytics y proporcionará mejores perspectivas para el negocio.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock
Campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en Adobe
