---
title: 'Trucos sencillos para aumentar la eficacia y el autoservicio: primera parte'
description: Conozca los principales retos a los que se enfrentan los equipos de análisis hoy en día y nuestras recomendaciones para superarlos mediante estrategias fuera de la IU de Adobe Analytics.
feature: Analytics Basics
role: Admin, Leader
level: Intermediate
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: d7fd77640928697f5857ccfcaf2c0f561aebeac3
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 94%

---

# Adobe Analytics: Trucos sencillos para aumentar la eficacia y el autoservicio

**Parte 1: Fuera de la IU**

En este artículo se describen los principales retos a los que se enfrentan los equipos de análisis hoy en día y nuestras recomendaciones para superarlos mediante estrategias fuera de la interfaz de Adobe Analytics.

## Principales retos para los equipos de Analytics

Muchos equipos de Analytics se encuentran con una distribución desequilibrada del trabajo. En lugar de una combinación de 80 % de análisis y 20 % de implementación, numerosas organizaciones se encuentran en la situación inversa. Ven que la mayor parte de sus esfuerzos se gastan en la configuración, la creación de informes y la prestación de asistencia, en lugar de en la elaboración de análisis que aporten perspectivas de alto valor.

Los equipos de Analytics se encuentran con que su productividad y eficiencia se han visto mermadas por varios motivos. Entre ellos, las implementaciones en constante evolución, el intento de mantener la confianza de la organización en los datos y la reducción de la rotación de analistas. La reducción de la rotación evita el largo proceso de formación de nuevos integrantes del equipo en herramientas de implementación personalizada y poco conocidas.

Otros desafíos clave a los que se enfrentan los analistas:

* **Competencia:** los negocios minoristas en línea y multicanal se vuelven más competitivos.
* **Expectativas del cliente:** las experiencias del cliente y las estrategias de marketing se tornan más complejas.
* **Valor de los datos:** el valor de los datos y las perspectivas precisos para impulsar una ventaja competitiva cobra mayor importancia.
* **Expectativas de los responsables de departamento:** los socios comerciales, los responsables de departamento y los ejecutivos solicitan cada vez más datos antes de la aprobación.
* **Administración de proyectos:** el equipo de análisis se ahoga en solicitudes para implementar la recopilación de datos para un flujo interminable de nuevas funciones, mientras produce informes precisos, incorpora nuevos analistas y revela la siguiente perspectiva desconocida.

## Claves para la eficacia: fuera de la IU

1. Mantenga su [Referencia de diseño de la solución](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) actualizada:

   * La SDR es la principal fuente fiable para la definición y el uso previsto de todas las variables de la implementación de Analytics.
   * La SDR es la referencia principal con la que los usuarios deben estar familiarizados para sacar el máximo partido a la IU de Adobe Analytics.
   * Es importante mantenerla actualizada y con versiones (se puede utilizar un formato de fecha sencillo).

1. Documentación y control de la recopilación de datos: especificaciones técnicas:

   Las especificaciones técnicas tienen un público más limitado que la SDR, pero son igualmente importantes, si no más, para una implementación funcional en su totalidad. Unas buenas especificaciones técnicas deben contener todos los recursos de desarrollo, control de calidad y administración de etiquetas necesarios para implementar la solución. Asegúrese de mantener tantos documentos como sea necesario para acomodar arquitecturas de implementación única.

   **Especificaciones técnicas**

   _Caso de uso :_instrucciones que describen cómo construir secuencias de comandos para la recopilación de datos

   _Usuarios principales :_desarrolladores

   _Otras notas :_

   * Documento muy técnico creado específicamente para los entornos de implementación
   * Útil tanto para la implementación inicial como para el mantenimiento/referencia subsiguientes
   * Organizado por tipo de solución (por ejemplo, seguimiento de campañas, metadatos de página, etc.)
   * El documento principal debe actualizarse y mantenerse a medida que se efectúen cambios en la SDR
   * Repositorio central
   * Números de versión sincronizados para especificaciones técnicas y SDR

1. Comunicar y documentar la intención de diseño de la solución en el lanzamiento:

   * Comunique con el usuario en mente
   * Al iniciar o mejorar la recopilación de datos, cree resúmenes simples que se puedan compartir con las partes interesadas
   * Refuerce el uso adecuado de las variables desde el principio
   * Envíe un correo electrónico de resumen para anunciar el lanzamiento a los principales interesados y analistas
   * Cree una biblioteca que se pueda usar como ayuda en las horas de oficina, las sesiones de habilitación de equipos o la incorporación específica de un equipo

1. Documentación de recopilación de datos, gobernanza e higiene de los datos: AHD:

   Analytics Health Dashboard (AHD) profundiza en un _único_ grupo de informes y proporciona una vista de los datos recopilados en cada componente (eVar, prop y evento). Esto ayuda a señalar si los datos han dejado de recopilarse en un componente para que pueda tomar medidas y corregir el problema. Puede ejecutar este panel de control en cualquier momento en el futuro para cualquier grupo de informes.

   Analytics Health Dashboard (AHD):

   _Caso de uso :_: instantánea de cada métrica y dimensión capturada por un único grupo de informes

   _Usuarios principales :_SME o desarrolladores de Lead Analytics

   _Otras notas :_
   * Entregado a través de Excel mediante una integración personalizada de la API de informes de Adobe
   * Los usuarios deben tener acceso a la API de servicios web de Analytics
   * Existen opciones para semiautomatizar

1. Gane ampliando el mundo de los expertos en la materia (SME):

   * Establezca SME dentro de los distintos equipos de la organización
   * Aumente su presencia ayudando a socializar versiones y ganancias
   * Utilice horarios de oficina regulares para ayudar a preparar a los formadores y reducir las tareas ad hoc

Obtenga más información acerca de la estrategia y el liderazgo mental en el centro [Éxito del cliente](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html?lang=es).