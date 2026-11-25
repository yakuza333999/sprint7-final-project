# 📊 Análisis Estadístico y Segmentación de Clientes — ConnectaTel

## 🎯 Objetivo del proyecto
Este proyecto realiza un análisis exploratorio y estadístico sobre los datos de **ConnectaTel**, una empresa de telecomunicaciones que opera en México y Colombia. El objetivo principal es comprender cómo los clientes utilizan los servicios móviles (llamadas y mensajes), detectar valores atípicos o comportamientos extremos y segmentar la base de usuarios por edad y nivel de consumo para identificar oportunidades comerciales y optimizar la oferta de planes.

---

## 📂 Datasets utilizados
El análisis integra tres fuentes de datos principales:

* **`plans.csv`**: Catálogo de los planes tarifarios disponibles (`Básico` y `Premium`), incluyendo precios mensuales, minutos y mensajes incluidos, y tarifas por excedentes.
* **`users_latam.csv`**: Información demográfica y de suscripción de los usuarios (`user_id`, nombre, edad, ciudad, fecha de registro, plan contratado y fecha de cancelación `churn_date`).
* **`usage.csv`**: Registro histórico de actividad y consumo generado por los usuarios, detallando llamadas (duración en minutos) y mensajes de texto (longitud) por fecha.

---

## 🛠️ Etapas del análisis realizadas
1. **Carga y exploración inicial de datos**: Inspección de tipos de datos, dimensiones de las tablas y detección de inconsistencias estructurales.
2. **Limpieza y corrección de valores**: Tratamiento de valores erróneos o centinelas (como `?` en ciudad, `-999` en edad y fechas futuras imposibles de `2026` en registro).
3. **Análisis de valores nulos**: Identificación y diferenciación entre datos faltantes reales y nulos estructurales propios del negocio (usuarios activos sin `churn_date`, y separación entre registros de llamadas y mensajes).
4. **Agregación y unificación de uso**: Consolidación del consumo mensual por usuario (total de llamadas, minutos acumulados y mensajes enviados) y cruce con sus datos demográficos y de plan.
5. **Análisis de distribuciones y detección de outliers**: Visualización mediante histogramas y diagramas de caja (*boxplots*), además del cálculo de límites superiores mediante el método del rango intercuartílico (IQR) para evaluar usuarios de consumo intensivo.
6. **Segmentación de clientes**: Clasificación de la cartera de usuarios según su grupo etario (`Joven`, `Adulto`, `Adulto Mayor`) y su nivel de actividad (`Bajo uso`, `Uso medio`, `Alto uso`).
7. **Síntesis de insights ejecutivos**: Traducción de los hallazgos estadísticos en recomendaciones accionables de negocio (estrategias de *upselling* y diseño de planes intermedios).

---

## 🚀 Cómo ejecutar el notebook

### Opción 1: Ejecutar en Google Colab (Recomendado)
1. Descarga el archivo `.ipynb` desde este repositorio.
2. Ingresa a [Google Colab](https://colab.research.google.com/).
3. Selecciona **Archivo > Subir cuaderno** y carga el archivo `.ipynb`.
4. Sube los archivos CSV (`plans.csv`, `users_latam.csv`, `usage.csv`) en el panel de archivos de la sesión (ícono de carpeta a la izquierda) y ejecuta todas las celdas (**Entorno de ejecución > Ejecutar todas**).

### Opción 2: Ejecutar localmente con Jupyter Notebook
1. Clona este repositorio en tu computadora y accede a la carpeta del proyecto:
```bash
git clone https://github.com/yakuza333999/sprint7-final-project.git
cd sprint7-final-project
```
2. Instala las librerías necesarias para el análisis y la visualización de datos:
```bash
pip install pandas numpy matplotlib seaborn
```
3. Verifica que los archivos CSV (`plans.csv`, `users_latam.csv` y `usage.csv`) estén en la carpeta del proyecto:
```bash
ls *.csv
```
4. Inicia Jupyter Notebook desde la terminal y abre el cuaderno en tu navegador:
```bash
jupyter notebook
```

---

## 🔁 Guía de reproducción

### Librerías necesarias
Este proyecto fue desarrollado en **Python 3** utilizando las siguientes librerías estándar de análisis y visualización:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`

### Instalación rápida
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Ubicación de los datasets
Los archivos de datos necesarios (`plans.csv`, `users_latam.csv` y `usage.csv`) se encuentran incluidos dentro de este repositorio listos para ser cargados sin requerir configuraciones adicionales.
