---
title: Cree plantillas de código estandarizadas
description: Para una implementación de línea de base (es decir, lo que su empresa considera como los KPI que debe tener para todos los sitios de Adobe Analytics), su organización debe tener un único método de implementación, siempre que sea posible.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: be00c8c0-a4bc-4380-98da-d1e2a3d31ec5
TQID: https://experienceleague.adobe.com/rmLhZbO6hYtpj1P0q0ZVwXglHVBC-KaHIkxyAF-7i-U
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 87%

---

# Cree plantillas de código estandarizadas

**QUÉ:** Para una implementación de “línea de base” (es decir, lo que su empresa considera como los KPI que debe tener para todos los sitios de Adobe Analytics), su organización debe tener un único método de implementación, siempre que sea posible. Por ejemplo, utilice la misma estructura de capa de datos en todos los sitios y aproveche la misma regla/código personalizado de administrador de etiquetas para capturar cosas como búsquedas internas o información del perfil del visitante.

**POR QUÉ:** Tener una implementación de línea de base repetible y escalable hace que añadir nuevos elementos o nuevos sitios/aplicaciones sea un esfuerzo racionalizado y de bajo esfuerzo, al mismo tiempo que mantiene la implementación limpia y hace que sea fácil solucionar problemas. El uso de un método uniforme también facilita que los nuevos administradores/desarrolladores se conecten y entiendan con qué están trabajando.

**CÓMO:** Adopte una plantilla de formato único para entregársela a los desarrolladores cuando se publique un nuevo sitio o una mejora del etiquetado. Por lo general, funciona bien un documento de texto, en el que se pueden esbozar los siguientes elementos:

* Variables que se están implementando, su propósito y cuándo se van a configurar. Por ejemplo:

| Variable de AA | Descripción | Cuándo/dónde se establece | Cómo se establece |
|--- |--- |--- |--- |
| eVar8 | Palabras clave de búsqueda interna | Al aterrizar en la página de resultados de búsqueda interna | Capa de datos |
| event8 | Recuento de búsquedas internas | Al aterrizar en la página de resultados de búsqueda interna | Regla de Launch |

* Detalles sobre cómo se establece. Aquí es donde especificaría los objetos de capa de datos necesarios y su sintaxis, así como las reglas del sistema de administración de etiquetas que se deban configurar y los detalles de la configuración de reglas.
* Los casos de prueba para asegurarse se cubren en el control de calidad y todas las variables que espera ver en un caso de prueba exitoso. Describa qué debe incluir una implementación correcta cuando el desarrollador pruebe esta mejora.

Lo ideal es que este documento solo necesite retocarse para el siguiente sitio donde actualice los conceptos básicos, como nombre de propiedad, convención de nomenclatura de páginas, etc. No es necesario reinventar la rueda cada vez, y puede ahorrar más tiempo.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock
Campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en Adobe
