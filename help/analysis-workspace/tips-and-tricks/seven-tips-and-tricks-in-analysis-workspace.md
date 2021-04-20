---
title: 7 consejos y trucos que facilitan la creación de proyectos de Analytics personalizados
description: Analysis Workspace es una potente herramienta dentro de Adobe Analytics que puede ayudarle a crear proyectos de análisis más impactantes. Tiene un amplio conjunto de funciones que le permite realizar cualquier tipo de análisis improvisado, pero una sencilla experiencia de usuario que hace esta potencia y escala accesibles.
feature: Workspace Basics
topics: topics
activity: use
doc-type: feature video
team: Technical Marketing
kt: 3945
role: "Business Practitioner, Developer, Data Engineer, Architect, Data Architect, Administrator, Leader"
level: Beginner
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---


# 7 consejos y trucos que facilitan la creación de proyectos de Analytics personalizados

**Amplíe su conjunto de habilidades de Analysis Workspace.**
Analysis Workspace es una potente herramienta dentro de Adobe Analytics que puede ayudarle a crear proyectos de análisis más impactantes. Tiene un amplio conjunto de funciones que le permite realizar cualquier tipo de análisis improvisado, pero una sencilla experiencia de usuario que hace esta potencia y escala accesibles.

## Generar: Exploración en profundidad hasta los puntos de datos correctos

### ***Sugerencia 1: Coloque cualquier  [!UICONTROL dimensión],  [!UICONTROL intervalo] de fechas,  [!UICONTROL segmento] o   métrica en cualquier parte del proyecto***

Basta con arrastrar y soltar un [!UICONTROL segmento] o cualquier otro componente en la zona de colocación [!UICONTROL segmento] en la parte superior de cualquier panel, y rápidamente puede segmentar ese panel en ciertos puntos de datos. Por ejemplo, puede segmentar el panel para que muestre únicamente las visitas en las que existan pedidos soltando la métrica [!UICONTROL a1/> &quot;pedidos&quot; en la zona de colocación del [!UICONTROL segmento]. ] Incluso puede segmentar por datos que no existan dentro de un componente (para ver visitas sin pedidos, por ejemplo) soltando el elemento de dimensión &quot;sin especificar&quot; o &quot;ninguno&quot; en la zona.

>[!VIDEO](https://video.tv.adobe.com/v/24036/?quality=12)

>[!TIP]
>
>**Pruebe esto:** hay un mundo de eficiencia esperándole en el menú que aparece al hacer clic con el botón derecho. Desde este menú, puede acceder a muchas herramientas y capacidades directamente en el flujo de trabajo de Analysis Workspace. Cuando tenga dudas, haga clic con el botón derecho para ver si la herramienta o la capacidad que necesita está cerca de la mano

### ***Sugerencia 2: Crear métricas sencillas sin abandonar el flujo de trabajo***

Con Quick [!UICONTROL Calculated Metrics], puede crear nuevas [!UICONTROL métricas] directamente en Analysis Workspace en lugar de ir al Generador de [!UICONTROL Métricas calculadas]. Simplemente seleccione las columnas [!UICONTROL metric] que desee calcular y, a continuación, en el menú que aparece al hacer clic con el botón derecho, seleccione &quot;[!UICONTROL Crear métrica a partir de la selección]&quot;. Ahora, puedes agregar, restar, dividir, multiplicar, y más, sin abandonar tu proyecto y romper tu tren de pensamiento.

>[!VIDEO](https://video.tv.adobe.com/v/23126/?quality=12)

>[!TIP]
>
>**Sugerencia útil:** se puede seleccionar hasta dos columnas de   métricas al usar  [!UICONTROL Métricas calculadas rápidas]. Utilice el [!UICONTROL Creador de métricas calculadas] para crear [!UICONTROL métricas] que incluyan más de dos [!UICONTROL métricas].

## Visualizar: Dar vida a los datos de los proyectos

### ***Sugerencia 3: Copiar e insertar visualizaciones y paneles en cualquier lugar***

Copie fácilmente visualizaciones y paneles de un lugar y agréguelos a otro, incluso a un proyecto diferente. Esto significa que puede mover fácilmente los datos a medida que su proyecto crezca y compartir sus conclusiones con nuevos usuarios para que no tengan que iniciar un análisis desde cero. Simplemente haga clic con el botón derecho en el panel o la visualización que desee copiar, seleccione &quot;[!UICONTROL Copiar visualización]&quot; y haga clic con el botón derecho en un panel en blanco para insertarlo.

>[!VIDEO](https://video.tv.adobe.com/v/23230/?quality=12)

>[!TIP]
>
>**Capacidad muy solicitada:** nuestros clientes nos pidieron que nos facilitáramos la copia e inserción de visualizaciones y paneles. Ahora, pasan menos tiempo recreando perspectivas y más tiempo descubriendo nuevas.

### ***Sugerencia 4: Cambiar entre visualizaciones de granularidad de tiempo en un solo clic***

Cambie fácilmente la vista de tiempo al trabajar con visualizaciones de tendencias. En iteraciones anteriores de Analysis Workspace, cambiar el tiempo significaba mostrar una tabla de origen, arrastrar una nueva [!UICONTROL dimensión] y luego volver a ocultar la tabla. Ahora, es tan fácil como seleccionar la granularidad de tiempo que desea mostrar directamente desde el menú desplegable &quot;[!UICONTROL Configuración de las visualizaciones]&quot; (engranaje superior derecho).

>[!VIDEO](https://video.tv.adobe.com/v/23548/?quality=12)

## Compartir: Facilitar el uso y comprensión de los hallazgos por parte de otros

### ***Sugerencia 5: Crear una variable personalizada  [!DNL Virtual Report Suite] para unidades de negocio específicas***

Adobe Analytics recopila grandes cantidades de datos. La depuración de componentes en [!DNL Virtual Report Suites] permite a los administradores crear un conjunto de datos para cada unidad de negocio de una organización. Esto significa que los analistas que trabajan en Analysis Workspace no tienen que pasar por los datos para encontrar lo que más les importa. Simplemente marque la casilla titulada &quot;[!UICONTROL Habilitar la personalización de componentes del grupo de informes virtuales]&quot; en el [!UICONTROL Creador de grupos de informes virtuales] en [!UICONTROL &quot;Componentes]&quot; y, a continuación, seleccione los [!UICONTROL componentes] que coincidan con lo que mide un equipo específico.

>[!VIDEO](https://video.tv.adobe.com/v/23544/?quality=12)

>[!TIP]
>
>**Sugerencia útil:** también puede cambiar el nombre de los componentes de un grupo de informes  [!UICONTROL virtuales ] para que coincida con la nomenclatura de unidades de negocio específicas. Simplemente haga clic en el icono de lápiz junto al componente y escriba un nuevo nombre.

### ***Sugerencia 6: Vínculo a paneles y visualizaciones dentro de un proyecto o entre proyectos***

Cree vínculos que lleven a las audiencias a cualquier lugar dentro de Analysis Workspace. Haga clic con el botón derecho en el panel al que desee vincular, seleccione &quot;[!UICONTROL Obtener vínculo del panel]&quot; y copie. A continuación, resalte el texto desde el que desea vincular, seleccione el icono de vínculo en el editor de texto de un cuadro de texto o descripción y pegue el texto. Para vincular a un proyecto completo, simplemente haga clic en la pestaña &quot;[!UICONTROL Compartir]&quot;, seleccione &quot;[!UICONTROL Obtener vínculo del proyecto]&quot; y siga los mismos pasos que se describen arriba.

>[!VIDEO](https://video.tv.adobe.com/v/23724/?quality=12)

>[!TIP]
>
>**Sugerencia útil:** Existen varias formas de vinculación que pueden mejorar la experiencia de sus lectores. Puede señalarlas a ilustraciones que coincidan con los resultados y las recomendaciones de los proyectos. O permitir que salten de una tabla de contenido directamente a las secciones en las que están interesados. También puede vincular proyectos de otros usuarios relacionados con su análisis

### ***Sugerencia 7: Guardar proyectos como plantillas personalizadas reutilizables***

Ahora puede convertir fácilmente cualquier proyecto en una plantilla personalizada. Simplemente seleccione &quot;[!UICONTROL Guardar como plantilla]&quot; en el menú desplegable &quot;[!UICONTROL Proyecto]&quot;, agregue etiquetas que faciliten la búsqueda de la plantilla y haga clic en &quot;[!UICONTROL Guardar proyecto como plantilla]&quot;. Ahora, la plantilla estará disponible para todos los usuarios de Analysis Workspace en la pestaña &quot;[!UICONTROL Plantillas personalizadas]&quot;. Esto permite a los analistas iniciar sus proyectos con puntos de datos significativos, en lugar de empezar desde el cuadrado uno.

>[!VIDEO](https://video.tv.adobe.com/v/23231/?quality=12)

>[!TIP]
>
>**Capacidad muy solicitada:** varios clientes nos pidieron que guardaramos los proyectos lo más posible como plantillas personalizadas. Ahora, esta capacidad se ha convertido en una de sus favoritas.

[Haga clic aquí para encontrar más sugerencias y trucos en Experience League](https://experienceleague.adobe.com/?search=tips&amp;tag=Analysis+Workspace#recommended/solutions/analytics)

| Acerca del autor |  |
|------------|------------|
| ![Jen Lasser](assets/jlasser-headshot-s.jpg) | Jen Lasser es administrador del equipo de administración de productos de Adobe Analytics. <br> En esta función, se reúne con los clientes para comprender sus necesidades comerciales,  <br>utilizando lo que aprende para informar a la hoja de ruta del producto de Adobe Analytics  <br>y priorizar las nuevas funciones del producto. Antes de su puesto actual, <br>Jen era consultora principal del equipo de consultoría de Adobe, y trabajaba como <br>experta en la visualización de datos, Analysis Workspace y [!DNL Report Builder]. <br><br>Con la ventaja de su perspectiva del mundo real, hemos seleccionado los siguientes consejos y trucos para  <br>ayudar a facilitar la creación, visualización y uso compartido de sus proyectos de Analysis Workspace |
