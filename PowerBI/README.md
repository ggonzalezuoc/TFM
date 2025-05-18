# Visualización interactiva: Relación entre renta y régimen de tenencia de la vivienda en España

Este archivo contiene el panel interactivo desarrollado como parte del Trabajo Final de Máster. El objetivo principal del informe es analizar la evolución temporal de la renta por hogar y los niveles de pobreza en función del régimen de tenencia de la vivienda en España, utilizando datos oficiales del Instituto Nacional de Estadística (INE).

## 📊 Contenido del informe

El informe está estructurado en seis hojas temáticas principales:

1. **Renta por régimen de tenencia**  
   Visualización temporal de la renta media por hogar, segmentada por régimen de tenencia (propiedad con/sin hipoteca, alquiler a precio de mercado, inferior al mercado, cesión).

2. **Tipo de hogar (Factor F1)**  
   Análisis de renta media por persona según la composición del hogar (parejas, monoparentales, etc.).

3. **Tamaño del hogar (Factor F2)**  
   Evolución de la renta media por persona y unidad de consumo en función del número de miembros del hogar.

4. **Grado de urbanización (Factor F3)**  
   Comparación de la renta según el entorno territorial: zonas densamente pobladas, intermedias o rurales.

5. **Carencias materiales (Factor F4)**  
   Porcentaje de personas con privación material según régimen de tenencia. Incluye evolución temporal.

6. **Comparativa por comunidad autónoma**  
   Visualiza la renta media y la tasa de pobreza por comunidad, comparando regímenes de tenencia.

## 🧱 Modelo de datos

El panel está basado en un modelo relacional en estrella, compuesto por:
- Tablas de hechos con métricas como renta, pobreza o carencias materiales.
- Tablas de dimensiones como régimen de tenencia, comunidad autónoma, tipo de hogar, etc.
- Una tabla de calendario central para sincronizar los ejes temporales en todas las visualizaciones.

## ⚙️ Interactividad

Cada página del informe incluye:
- Filtros dinámicos por año, régimen de vivienda, comunidad autónoma, tipo de hogar o tamaño del hogar.
- Indicadores visuales (flechas, colores) para resaltar tendencias o variaciones anuales.
- Segmentadores sincronizados para facilitar el análisis comparativo entre factores.

## 📁 Datos de origen

Los datos utilizados se han obtenido a través de la API del INE, tratados y transformados con scripts en Python disponibles en la carpeta `/notebooks`.

## 🌐 Acceso al panel publicado

Puedes consultar el panel interactivo completo en Power BI en el siguiente enlace:

🔗 [https://app.powerbi.com/view?r=eyJrIjoiYjgzNWMxYjctYTYwOS00MDA5LWJkZjgtYzcwYjQ0MGViN2FkIiwidCI6ImFlYzc2MmU0LTNkNTQtNDk1ZS1hOGZlLTQyODdkY2U2ZmU2OSIsImMiOjh9](https://app.powerbi.com/view?r=eyJrIjoiYjgzNWMxYjctYTYwOS00MDA5LWJkZjgtYzcwYjQ0MGViN2FkIiwidCI6ImFlYzc2MmU0LTNkNTQtNDk1ZS1hOGZlLTQyODdkY2U2ZmU2OSIsImMiOjh9)
