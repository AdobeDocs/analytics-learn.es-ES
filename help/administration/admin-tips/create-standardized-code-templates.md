---
title: Creación de plantillas de código estandarizadas
description: 'Para una implementación de línea de base (es decir, lo que su empresa considera como los KPI que debe tener para todos los sitios de Adobe Analytics), su organización debe tener un único método de implementación siempre que sea posible. '
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 2%

---


# Creación de plantillas de código estandarizadas

**QUÉ:** Para una implementación &quot;de línea de base&quot; (es decir, lo que su empresa considera como los KPI que debe tener para todos los sitios de Adobe Analytics), su organización debe tener un único método de implementación siempre que sea posible. Por ejemplo, utilice la misma estructura de capa de datos en todos los sitios y aproveche la misma regla de administrador de etiquetas/código personalizado para capturar cosas como búsquedas internas o información de perfil del visitante.

**POR QUÉ:** Tener una implementación de línea de base repetible y escalable hace que agregar nuevos elementos o nuevos sitios/aplicaciones sea un esfuerzo racionalizado y de bajo esfuerzo, al mismo tiempo que mantiene su implementación limpia y fácil de solucionar. El uso de un método uniforme también facilita a los nuevos administradores/desarrolladores la conexión en línea y la comprensión de su trabajo.

**CÓMO:** Adopte una plantilla de formato único para entregársela a los desarrolladores cuando accedan en línea a un sitio nuevo o a una mejora de las etiquetas. Normalmente, un documento de palabra funciona bien donde puede delinear los siguientes elementos:

* Variables que se están implementando, su propósito y cuándo se van a configurar. Por ejemplo:

| Variable AA | Descripción | Cuándo/Dónde se establece | Cómo configurar |
|--- |--- |--- |--- |
| eVar8 | Palabras clave de búsqueda interna | Al aterrizar la página de resultados de búsqueda interna | capa de datos |
| event8 | Recuento de búsquedas internas | Al aterrizar la página de resultados de búsqueda interna | Regla de Launch |

* Detalles sobre cómo configurar. Aquí es donde especificaría los objetos de capa de datos necesarios y su sintaxis, así como las reglas del sistema de administración de etiquetas que se deban configurar y los detalles de la configuración de reglas.
* Los casos de prueba para garantizar que se tratan en el control de calidad y todas las variables que espera ver en un caso de prueba de éxito. Describa qué debe incluir una implementación correcta cuando el desarrollador pruebe esta mejora.

Lo ideal es que este documento solo necesite ser modificado para el siguiente sitio donde actualice los conceptos básicos como nombre de propiedad, convención de nomenclatura de páginas, etc. No hay necesidad de reinventar la rueda cada vez, y puede ahorrar más tiempo.

## Autores

Este documento fue coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataformas de análisis digital de NortonLifeLock, campeona de Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora senior en Adobe
