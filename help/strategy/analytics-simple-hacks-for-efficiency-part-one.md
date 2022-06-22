---
title: Hackks simples para buena eficacia y autoservicio - parte 1
description: Conozca los desafíos clave que enfrentan los equipos de análisis hoy en día, y nuestras recomendaciones para superarlos usando estrategias fuera de la interfaz de usuario de Adobe Analytics.
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: dad200fdb5c5d15c00254d693fb47bbcec80afaf
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Adobe Analytics: Sencillos hacks para buena eficacia y autoservicio

**Parte 1: Fuera de la interfaz de usuario**

En este artículo se describen los desafíos clave a los que se enfrentan los equipos de análisis en la actualidad y nuestras recomendaciones para superarlos mediante estrategias fuera de la interfaz de Adobe Analytics.

## Desafíos clave para los equipos de Analytics

Muchos equipos de Analytics se encuentran con una distribución desequilibrada del trabajo. En lugar de una combinación de análisis del 80% y implementación del 20%, numerosas organizaciones se encuentran en lo contrario. Ven la mayoría de sus esfuerzos en la configuración, la creación de informes y la prestación de asistencia, en lugar de producir análisis que promuevan perspectivas de alto valor.

Los equipos de Analytics están encontrando que su productividad y eficiencia se han visto mermadas por varios motivos. Entre ellas se cuentan las implementaciones en constante evolución, el intento de mantener la confianza de la organización en los datos y la reducción del movimiento de los analistas. La reducción de la rotación evita el largo proceso de capacitación de nuevos integrantes del equipo sobre herramientas de implementación personalizadas y poco conocidas.

Otros desafíos clave a los que se enfrentan los analistas:

* **Competencia:** Los negocios minoristas en línea y multicanal se hacen más competitivos.
* **Expectativas del cliente:** Las experiencias del cliente y las estrategias de marketing se vuelven más complejas.
* **Valor de datos:** El valor de los datos y perspectivas precisos para impulsar una ventaja competitiva cobra mayor importancia.
* **Expectativas de las partes interesadas:** Los socios comerciales, las partes interesadas y los ejecutivos solicitan cada vez más datos antes de la aprobación.
* **Administración de proyectos:** El equipo de análisis se queda sin solicitudes para implementar la recopilación de datos para un flujo interminable de nuevas funciones, a la vez que genera informes precisos, incorpora nuevos analistas y descubre la siguiente nueva perspectiva.

## Claves para la eficacia: Fuera de la interfaz de usuario

1. Mantenga su [Referencia de diseño de la solución](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (DEG) actualizado:

   * El SDR es la fuente principal de verdad para la definición y el uso intencionado de todas las variables dentro de la implementación de Analytics.
   * El SDR es la referencia principal con la que los usuarios deben estar familiarizados para sacar el máximo partido de la interfaz de usuario de Adobe Analytics.
   * Es importante mantenerlo actualizado y con versiones (se puede utilizar un formato de fecha sencillo).

1. Documentación y control de la recopilación de datos: especificaciones técnicas:

   Las especificaciones técnicas tienen una audiencia más limitada que los DEG, pero son igualmente importantes, si no más, para una implementación completamente funcional. Una buena especificación tecnológica debe ser todos los recursos de desarrollo, control de calidad y administración de etiquetas necesarios para implementar la solución. Asegúrese de mantener tantos documentos como sea necesario para acomodar arquitecturas de implementación únicas.

   **Especificación técnica**

   _Caso de uso:_ Instrucciones que describen cómo construir secuencias de comandos para la recopilación de datos

   _Usuarios principales:_ Desarrolladores

   _Otras notas:_

   * Documento muy técnico creado específicamente para los entornos de implementación
   * Útil tanto para la implementación inicial como para el mantenimiento/referencia subsiguiente
   * Organizado por tipo de solución (por ejemplo, seguimiento de campaña, metadatos de página, etc.)
   * El documento principal debe actualizarse y mantenerse a medida que se realicen cambios en los DEG
   * Repositorio central
   * Números de versión sincronizados para especificaciones técnicas y SDR

1. Comunicar y documentar la intención de diseño de la solución en el lanzamiento:

   * Comunicarse con el usuario en mente
   * Al iniciar o mejorar la recopilación de datos, cree resúmenes simples que se puedan compartir con las partes interesadas
   * Reforzar el uso de variables adecuado fuera de la puerta
   * Enviar un correo electrónico de anuncio de lanzamiento de resumen a los principales interesados y analistas
   * Cree una biblioteca que se pueda usar para admitir horas de oficina, sesiones de habilitación de equipos o para la incorporación específica de un equipo

1. Documentación de recopilación de datos, gobernanza e higiene de los datos - AHD:

   El panel de control de estado de Analytics (AHD) profundiza en un _single_ grupo de informes y proporciona una vista de los datos recopilados en cada componente (eVar, prop y evento). Esto puede ayudar a señalar si los datos han dejado de recopilarse en un componente para que pueda tomar medidas a fin de corregir el problema. Puede ejecutar este tablero en cualquier momento en el futuro para cualquier grupo de informes.

   Tablero de estado de Analytics (AHD):

   _Caso de uso:_ Resumen de cada métrica y dimensión capturada por un único grupo de informes

   _Usuarios principales:_ Análisis de posibles clientes SME y/o Dev

   _Otras notas:_
   * Entregado a través de Excel mediante una integración personalizada de la API de informes de Adobe
   * Los usuarios deben tener acceso a la API de servicios web de Analytics
   * Existen opciones para semi-automatizar

1. Ganar a través de la expansión del mundo de los expertos en la materia (PYME):

   * Establecer PYME en los distintos equipos de la organización
   * Construya su presencia ayudando a socializar versiones y ganancias
   * Utilice horarios de oficina regulares para ayudar a capacitar a los formadores y reducir las tareas ad hoc

Obtenga más información sobre la estrategia y el liderazgo mental en [Éxito del cliente](https://experienceleague.corp.adobe.com/docs/customer-success/customer-success/overview.html) hub.