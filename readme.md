# SIVIRA + Google Trends  
## Análisis de desfases temporales (lags) para vigilancia epidemiológica en España

Este repositorio contiene el **pipeline completo y reproducible** para analizar la relación temporal entre la vigilancia epidemiológica oficial en España (SiVIRA, ISCIII) y el interés poblacional medido mediante **Google Trends**, centrado en tres patologías respiratorias:

- Gripe
- Virus Respiratorio Sincitial (VRS)
- COVID-19

El objetivo es evaluar si determinados patrones de búsqueda pueden comportarse como **indicadores reactivos o anticipatorios (1–2 semanas)** de la actividad epidemiológica real.

---

## 📂 Contenido del repositorio

### Datos
- `tablas_informe_SiVIRA_202551.xlsx`  
  Archivo oficial del último informe epidemiológico semanal SiVIRA.

- `google_trends_daily_GRIPE.csv`  
- `google_trends_daily_VRS.csv`  
- `google_trends_daily_COVID.csv`  
  Series diarias de Google Trends (España).

### Procesados
- `gt_index_daily_GRIPE.csv`
- `gt_index_daily_VRS.csv`
- `gt_index_daily_COVID.csv`

- `merged_sivira_trends_weekly.csv`

### Resultados
- `lag_analysis_all.csv`
- `lag_analysis_best.csv`

### Figuras
- `/out_figs/`
  - overlays temporales
  - heatmaps de correlación
  - tablas por patología

---

## 🔗 Fuente oficial de datos SiVIRA

Centro Nacional de Epidemiología – Instituto de Salud Carlos III

https://cne.isciii.es/servicios/enfermedades-transmisibles/enfermedades-a-z/gripe-covid-19-y-otros-virus-respiratorios

### Ruta exacta utilizada

1. Acceder al **último informe epidemiológico semanal**
2. Ir a la sección:

**7.2. Área de descargas**

3. Descargar el archivo Excel:

**“Tablas con datos de origen (.xlsx)”**

Este archivo contiene los datos numéricos que sustentan las figuras del informe y es el que se utiliza directamente en este proyecto.

---

## ▶️ Ejecución paso a paso en Google Colab

### 1. Subir el notebook
Abrir Google Colab y subir el cuaderno con las **celdas 1 a 5**.

### 2. Subir los archivos necesarios
En el panel de archivos de Colab subir:

- `tablas_informe_SiVIRA_202551.xlsx`
- `google_trends_daily_GRIPE.csv`
- `google_trends_daily_VRS.csv`
- `google_trends_daily_COVID.csv`

---

### 3. Celda 1 – Dependencias
- Importación de librerías
- Funciones auxiliares
- Configuración general

---

### 4. Celda 2 – Google Trends
- Carga de los CSV diarios
- Construcción de índices compuestos
- Conversión a semanas ISO

---

### 5. Celda 3 – Datos SiVIRA
- Lectura del Excel oficial
- Selección de detecciones virales
- Limpieza y estructuración por año/semana

---

### 6. Celda 4 – Análisis de lags
- Unión SiVIRA + Google Trends
- Correlaciones de Pearson
- Lags 0 a +6 semanas
- Identificación del mejor desfase por patología

---

### 7. Celda 5 – Figuras
- Overlays temporales
- Heatmaps de correlación
- Exportación automática a `/out_figs/`

---

## 🧪 Estado del proyecto

- ✔ Pipeline completo
- ✔ Reproducible
- ✔ Versionado en GitHub
- ✔ Resultados positivos y negativos documentados

Corresponde a la versión **baseline v1**, base para iteraciones futuras con optimización de términos de búsqueda.

---

## 🧑‍⚕️ Autor

**César Carballo Cardona**  
Servicio de Urgencias – Hospital Universitario La Paz  
Madrid, España
