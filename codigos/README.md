# Estructura de los códigos

## Descripción
Este notebook contiene un proceso completo de **extracción, transformación y carga (ETL)** de diversos conjuntos de datos obtenidos desde la API del Instituto Nacional de Estadística (INE). Los datos se relacionan principalmente con indicadores de renta, pobreza, tenencia de la vivienda y carencia material. El objetivo es estructurarlos en un formato analítico adecuado para generar un modelo relacional en Power BI y realizar un modelo predictivo en python.

## Objetivo
Consolidar múltiples fuentes estadísticas en un modelo de datos en estrella, separando tablas de hechos y dimensiones, para facilitar el análisis descriptivo y predictivo del fenómeno de la pobreza y la desigualdad económica.

## Fuentes de datos (INE API)
Los datos se obtienen desde las siguientes tablas del INE:

- [Carencia material por régimen de tenencia de la vivienda](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/60147?tip=AM&)
- [Renta por hogar por comunidades autónomas](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59945?tip=AM)
- [Renta por hogar por régimen de tenencia](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59947?tip=AM&)
- [Renta por persona y unidad de consumo por tipo de hogar](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59949?tip=AM&)
- [Renta por persona y unidad de consumo por tamaño de hogar](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59953?tip=AM&)
- [Renta por persona y unidad de consumo por grado de urbanización](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59956?tip=AM&)
- [Renta por persona y unidad de consumo por régimen de tenencia](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/59960?tip=AM)
- [Personas por decil de renta por unidad de consumo y régimen de tenencia](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/9946?tip=AM)
- [Tasa de riesgo de pobreza por comunidades autónomas](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/9947?tip=AM&)
- [Tasa de riesgo de pobreza por régimen de tenencia](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/9963?tip=AM&)
- [Hogares por régimen de tenencia y comunidades autónomas](https://servicios.ine.es/wstempus/js/es/DATOS_TABLA/9997?tip=AM&)

## Transformaciones realizadas
Para cada dataset:
- Se descarga el contenido JSON desde la API.
- Se extraen las variables relevantes según la estructura de metadatos.
- Se limpian los datos: tratamiento de nulos, eliminación de espacios en blanco, conversión de tipos.
- Se estructura el dataset en:
  - Una tabla de **hechos** con las medidas principales (ej. valor por año).
  - Una o varias tablas de **dimensiones** con las categorías (ej. tipo de hogar, régimen de tenencia, comunidad autónoma).

## Estructura de salida
Los datos se guardan en carpetas organizadas por tema. Dentro de cada una se encuentran las tablas de hechos y dimensiones.

## Dependencias
- `pandas`
- `requests`
- `os`

## Aplicación final
Estos datasets están preparados para:
- Visualización interactiva en Power BI
- Análisis exploratorio y predictivo con modelos estadísticos o de machine learning

## Modelo predictivo
Además del tratamiento de datos, se incluye un modelo predictivo desarrollado con los siguientes enfoques:

- **Modelos explicativos multivariantes:** Regresión lineal y Random Forest para analizar la influencia de distintas variables en la tasa de pobreza.
- **Modelos de series temporales:** Prophet para la proyección de la tasa de pobreza por régimen de tenencia de la vivienda hasta el año 2026.

Estos modelos permiten tanto la interpretación de factores clave como la generación de predicciones para apoyar el análisis de tendencias.

## Última actualización
18 de mayo de 2025



