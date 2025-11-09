# 🚖 Análisis de Viajes de Taxi en Chicago

## 📊 Descripción del proyecto
Este proyecto forma parte del bootcamp de análisis de datos de **TripleTen**.  
El objetivo fue analizar los patrones de uso de taxis en la ciudad de Chicago, identificando las **empresas más activas**, los **barrios con mayor demanda** y **evaluar si las condiciones climáticas influyen en la duración de los viajes**.

Los datos provienen de consultas SQL realizadas sobre una base de datos de viajes de taxis del año 2017.

---

## 🧰 Herramientas utilizadas
- **Python**
- **pandas** – para la carga y exploración de datos  
- **matplotlib** – para visualización de resultados  
- **scipy.stats** – para realizar pruebas de hipótesis (t-test)

---

## ⚙️ Proceso del análisis

### 1️⃣ Carga y exploración de datos
Se analizaron tres tablas exportadas de SQL:
- `project_sql_result_01.csv` → número de viajes por empresa de taxis  
- `project_sql_result_04.csv` → número promedio de viajes por barrio de destino  
- `project_sql_result_07.csv` → duración promedio de viajes según condiciones climáticas  

Se revisó la estructura de los datos y se seleccionaron las columnas más relevantes.

---

### 2️⃣ Análisis exploratorio
#### 📈 Top 15 empresas de taxis por cantidad de viajes
Se identificó que la empresa **Flash Cab** realizó la mayor cantidad de viajes entre el 15 y 16 de noviembre de 2017, **casi el doble** que la segunda empresa, **Taxi Affiliation Services**.

#### 🗺️ Top 10 barrios por número promedio de viajes
Los barrios con mayor número promedio de viajes durante noviembre de 2017 fueron:
1. **Loop**
2. **River North**
3. **Streeterville**

Estos concentraron la mayoría de los destinos de los pasajeros.

---

### 3️⃣ Prueba de hipótesis – Efecto del clima en la duración de los viajes
Se compararon los tiempos promedio de viaje entre sábados con **buen clima** y sábados con **mal clima** (desde *Loop* hasta el *Aeropuerto Internacional O’Hare*).

**Hipótesis:**
- H₀: No hay diferencia significativa en la duración de los viajes según las condiciones climáticas.  
- H₁: Existe una diferencia significativa en la duración de los viajes según el clima.

**Resultado:**
- p-valor ≈ 0.25 (mayor que 0.05)  
➡️ **No se rechaza la hipótesis nula.**  
No hay evidencia estadísticamente significativa de que el clima lluvioso influya en la duración promedio de los viajes.

---

## 📊 Conclusiones
- **Flash Cab** es la empresa líder en número de viajes en las fechas analizadas.  
- **Loop** y **River North** son los barrios más transitados de la ciudad.  
- **El clima no mostró un efecto significativo** en la duración promedio de los viajes hacia el aeropuerto.  

Estos resultados pueden ser útiles para optimizar la distribución de taxis y planificar la operación según zonas y demanda real.

---

## 📁 Estructura del repositorio

analisis_taxis_chicago/
│
├── data/
│ ├── project_sql_result_01.csv
│ ├── project_sql_result_04.csv
│ └── project_sql_result_07.csv
│
├── notebooks/
│ └── analisis_taxis.ipynb
│
└── README.md


---

## 🧑‍💻 Autor

Emiliano Sandoval