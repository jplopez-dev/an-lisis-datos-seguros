# 📊 Análisis Exploratorio de Datos — Sector Asegurador Colombiano

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualización-4C72B0?style=flat)
![SENA](https://img.shields.io/badge/SENA-AA3--EV02%20%7C%20EV03-39A900?style=flat)
![Estado](https://img.shields.io/badge/Estado-Completado-02C39A?style=flat)

> Proyecto de análisis exploratorio de datos (EDA) aplicado a un dataset real del sector
> asegurador colombiano. Se identifican variables clave, se aplican métodos estadísticos
> y se construye una narrativa de datos que responde preguntas estratégicas de negocio.

---

## 🎯 Objetivo

Determinar el perfil del cliente con mayor potencial comercial para una compañía de seguros,
respondiendo tres preguntas de negocio a través de visualizaciones estadísticas y análisis
multivariado en Python.

---

## ❓ Preguntas de Negocio

| # | Pregunta | Tipo de análisis |
|---|----------|-----------------|
| P1 | ¿Las personas fumadoras representan el mayor potencial para ventas de seguros? | Comparación entre grupos |
| P2 | ¿Cuál es la edad poblacional en la que se debe concentrar la estrategia comercial? | Segmentación + correlación |
| P3 | ¿Cuál es la región con mayor potencial de venta teniendo en cuenta los ingresos? | Análisis geográfico |

---

## 📁 Estructura del Proyecto
analisis-datos-seguros-sena/
│
├── 📓 ANALISIS_EXP_DATOS_PY_SENA.ipynb   # Notebook principal con todo el análisis
├── 📂 DatosSeguros.csv                    # Dataset — 1.349 registros, 7 variables
├── 📄 Informe_AA3_EV02.pdf                # Informe detallado del análisis
├── 📊 AA3-EV03_Graficos_AnalisisDatos.pptx # Presentación de tipos de gráficos
└── 📖 README.md

---

## 🗂️ Dataset

El archivo `DatosSeguros.csv` contiene información de **1.349 clientes** de una compañía
de seguros con las siguientes variables:

| Variable | Tipo | Descripción |
|----------|------|-------------|
| `edad` | Numérica | Edad del cliente en años |
| `sexo` | Categórica | Género — M / F |
| `imc` | Numérica | Índice de Masa Corporal |
| `hijos` | Numérica | Número de hijos |
| `fumador` | Categórica | Condición de fumador — yes / no |
| `region` | Categórica | Región colombiana — 4 regiones |
| `valor_seguro` | Numérica | Valor de la póliza en pesos |

---

## 🔬 Metodología

El análisis sigue un flujo EDA estándar de tres fases:
PREPARACIÓN        2. ANÁLISIS UNIVARIADO        3. ANÁLISIS MULTIVARIADO
─────────────         ──────────────────────         ────────────────────────
Carga del CSV    →    Distribución de variables  →   Correlación entre variables
Identificación        Detección de nulos              Scatter plots 3 variables
de variables          Corrección de errores           Barplots agrupados
Discretización        Estadísticas descriptivas       Conclusiones de negocio
de edad en rangos

---

## 📈 Gráficas Utilizadas

| Figura | Tipo | Variable(s) | Propósito |
|--------|------|-------------|-----------|
| Fig. 6 | Gráfica circular | fumador | Distribución de clientes por condición |
| Fig. 7 | Boxplot | fumador × valor_seguro | Distribución del valor por grupo |
| Fig. 8 | Gráfica circular | fumador × valor total | % del negocio por grupo |
| Fig. 10 | Heatmap | edad, imc, hijos, valor_seguro | Correlación entre variables numéricas |
| Fig. 11 | Scatter | rango_edad × valor_seguro × imc | Análisis multivariado con IMC |
| Fig. 12 | Scatter | rango_edad × valor_seguro × fumador | Análisis multivariado con fumador |
| Fig. 13 | Barplot agrupado | region × valor_seguro × fumador | Potencial por región |

---

## 💡 Hallazgos Principales

### 🚬 Pregunta 1 — Fumadores
> El **20% de clientes fumadores** genera el **49.4% de los ingresos totales**.
> Cada cliente fumador vale en promedio **4 veces más** que uno no fumador
> ($31.733 vs $8.430).

### 👤 Pregunta 2 — Edad
> La **edad** es la variable con mayor correlación con el valor del seguro (r = 0.30).
> El grupo de **60+ años** presenta el mayor valor promedio de póliza ($21.248),
> especialmente combinado con IMC alto y condición de fumador.

### 🗺️ Pregunta 3 — Región
> **Cundinamarca** lidera con el mayor valor promedio de seguro ($14.735),
> seguida por Boyacá ($13.344), Antioquia ($12.564) y Caribe ($12.453).

---

## 🧑‍💼 Perfil del Cliente Ideal
┌─────────────────────────────────────────────┐
│          CLIENTE DE MAYOR POTENCIAL         │
│                                             │
│   🚬 Fumador        → valor ~4x superior    │
│   👴 60+ años       → mayor valor promedio  │
│   ⚖️  IMC alto       → incrementa el precio │
│   📍 Cundinamarca   → región líder           │
└─────────────────────────────────────────────┘
---

## 🛠️ Tecnologías

- **Python 3.12** — lenguaje principal
- **pandas** — manipulación y limpieza de datos
- **matplotlib** — visualización base
- **seaborn** — visualizaciones estadísticas avanzadas
- **Google Colab / Jupyter LAB** — entorno de desarrollo

---

## ▶️ Cómo ejecutar

```bash
# 1. Clona el repositorio
git clone https://github.com/tu-usuario/analisis-datos-seguros-sena.git

# 2. Entra a la carpeta
cd analisis-datos-seguros-sena

# 3. Instala las dependencias
pip install pandas matplotlib seaborn

# 4. Abre el notebook
jupyter lab ANALISIS_EXP_DATOS_PY_SENA.ipynb
```

O ábrelo directamente en Google Colab:

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 📚 Contexto Académico

| Campo | Detalle |
|-------|---------|
| Institución | Servicio Nacional de Aprendizaje — SENA |
| Programa | Tecnología en Análisis y Desarrollo de Software |
| Actividad | Aprendizaje 3 — Evidencias EV02 y EV03 |
| Componente | Recursos y herramientas para el análisis efectivo de datos |

---

## 👤 Autor

**Juan Pablo Lopez Rodriguez**
Ingenierio en sistemas
Aprendiz SENA · Tecnología en Análisis y Desarrollo de Software
📧 lopezpablorodriguez.117@gmail.com · 🔗 [tu LinkedIn si tienes]

---

*Proyecto desarrollado como parte del proceso de formación en análisis de datos.*
*Los datos utilizados son de carácter académico.*
