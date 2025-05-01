# Análisis de Riesgo Cardiovascular

Este repositorio contiene el análisis completo del dataset `cardio.csv`, con el objetivo de explorar, limpiar y modelar variables que influyen en el índice de masa corporal (BMI) y el riesgo de enfermedad coronaria a 10 años.

---

## Estructura del repositorio

```
├── data/
│   └── cardio.csv           # Dataset original
├── notebooks/
│   ├── 01_EDA.ipynb         # Análisis exploratorio de datos
│   ├── 02_Preprocessing.ipynb  # Limpieza, manejo de nulos y outliers
│   ├── 03_Descriptive.ipynb    # Estadísticas descriptivas y gráficos
│   ├── 04_Hypothesis.ipynb     # Pruebas de hipótesis y probabilidades condicionales
│   ├── 05_Regression.ipynb     # Modelos de regresión lineal y logística
│   └── 06_BySex.ipynb       # Modelos separados por sexo
├── scripts/
│   └── utils.py            # Funciones de limpieza y reporte
├── requirements.txt        # Dependencias del proyecto
└── README.md               # Documento de descripción (tú estás aquí)
```

---

## Descripción del dataset

* **Sexo (`sex`)**: M / F
* **Edad (`age`)**: años cumplidos
* **Educación (`education`)**: nivel educativo codificado
* **Tabaquismo**: `currentSmoker` (Yes/No) y `cigsPerDay`
* **Medicamentos para presión arterial** (`BPMeds`)
* **Historial**: `prevalentStroke`, `prevalentHyp`, `diabetes`
* **Mediciones fisiológicas**:

  * Colesterol total (`totChol`)
  * Presión sistólica y diastólica (`sysBP`, `diaBP`)
  * Índice de masa corporal (`BMI`)
  * Ritmo cardíaco (`heartRate`)
  * Glucosa (`glucose`)
* **Objetivo de riesgo**: `TenYearCHD` (0 = no, 1 = sí)

---

## Requisitos

* Python 3.8+
* Bibliotecas:

  ```bash
  pandas
  numpy
  matplotlib
  seaborn
  scikit-learn
  scipy
  ```

Instala todas las dependencias con:

```bash
pip install -r requirements.txt
```

---

## Uso

1. Clona el repositorio:

   ```bash
   ```

git clone [https://github.com/tu-usuario/cardiovascular-analysis.git](https://github.com/tu-usuario/cardiovascular-analysis.git)
cd cardiovascular-analysis

```

2. Ejecuta los notebooks en orden dentro de la carpeta `notebooks/`.
3. Revisa los resultados y conclusiones en cada sección.

---

## Resumen de análisis

1. **EDA** (`01_EDA.ipynb`)
   - Inspección inicial, detección de valores faltantes.
   - Visualizaciones de distribución de variables.
2. **Preprocesamiento** (`02_Preprocessing.ipynb`)
   - Eliminación de nulos y outliers (criterio IQR).
   - Guardado de `df_clean` para análisis posteriores.
3. **Análisis descriptivo** (`03_Descriptive.ipynb`)
   - Estadísticas (media, mediana, std, IQR) y histogramas.
   - Identificación de variable con mayor dispersión.
4. **Pruebas de hipótesis** (`04_Hypothesis.ipynb`)
   - Prueba t para consumo de cigarrillos por sexo.
   - Probabilidad condicional de ser hombre dado BMI ≥ Q3.
5. **Modelos** (`05_Regression.ipynb`)
   - Regresión lineal para predecir BMI (con variables cuantitativas y cualitativas).
   - Regresión logística para predecir `TenYearCHD`.
6. **Modelos por sexo** (`06_BySex.ipynb`)
   - Ajuste de modelos separados (lineal y logístico) para subgrupos `M` y `F`.

---

## Conclusiones generales

- **BMI**: el modelo lineal explica ~13% de la varianza; sexo y tabaquismo son predictores significativos.
- **Riesgo coronario**: modelo logístico con AUC-ROC ~0.73; detecta mejor clase negativa.
- **Limitaciones**: faltan variables clave (dieta, ejercicio, genética) y relaciones no lineales.
- **Recomendaciones**: explorar modelos no lineales, regularización, y técnicas de balanceo (SMOTE).

---

### Autor

Sebastián Durán  
Analista de Datos | [GitHub](https://github.com/tu-usuario)

---

> **Nota:** Actualiza los enlaces y rutas según tu repositorio antes de publicar en GitHub.

```
