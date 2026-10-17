# Sistema de Detección de Intrusiones mediante Machine Learning

## Descripción

Este proyecto tiene como objetivo desarrollar un Sistema de Detección de Intrusiones (IDS) capaz de identificar y clasificar tráfico de red malicioso mediante técnicas de Machine Learning.

Utilizando el conjunto de datos CIC-IDS2017, se aplican procesos de análisis de datos, selección de características, entrenamiento de modelos y evaluación de desempeño para detectar distintos tipos de ataques informáticos.

El proyecto busca combinar conocimientos de Ciencia de Datos, Inteligencia Artificial y Ciberseguridad para construir una solución práctica orientada a la detección temprana de amenazas en entornos de red.

## Objetivos

- Analizar tráfico de red utilizando técnicas de Ciencia de Datos.
- Identificar patrones asociados a actividades maliciosas.
- Entrenar modelos de Machine Learning para detectar intrusiones.
- Evaluar el desempeño de diferentes algoritmos de clasificación.
- Aplicar buenas prácticas de ciberseguridad y análisis de datos.
- Construir un proyecto práctico orientado al aprendizaje y al desarrollo profesional.

## Tecnologías principales

- Python
- Pandas
- NumPy
- Scikit-Learn
- Machine Learning
- Ciencia de Datos
- Ciberseguridad

## Arquitectura del proyecto

```text
ids-detector/

├── app/
├── ml/
├── data/
├── notebooks/
├── tests/
├── docker/
├── requirements.txt
└── README.md
```

El proyecto está organizado para separar claramente los componentes de la API, el procesamiento de datos, Machine Learning y pruebas.

---

## API (FastAPI)

```text
app/

├── api/
├── core/
├── db/
├── schemas/
├── services/
└── repositories/
```

### Responsabilidades

- Exponer endpoints REST.
- Validar datos de entrada y salida.
- Gestionar la lógica de negocio.
- Integrar modelos de Machine Learning.
- Registrar métricas e información operativa.

---

## Machine Learning

```text
ml/

├── preprocess.py
├── feature_engineering.py
├── train.py
├── evaluate.py
├── datasets/
└── models/
```

### Responsabilidades

- Preparación y limpieza de datos.
- Ingeniería de características.
- Entrenamiento de modelos.
- Evaluación y métricas.
- Almacenamiento de modelos entrenados.

---

## Datos

```text
data/

├── raw/
├── processed/
└── samples/
```

### Responsabilidades

#### raw/

Contiene los archivos originales del dataset CIC-IDS2017 sin modificaciones.

```text
data/raw/

├── Monday-WorkingHours.pcap_ISCX.csv
├── Tuesday-WorkingHours.pcap_ISCX.csv
├── Wednesday-workingHours.pcap_ISCX.csv
├── Thursday-WorkingHours-Morning-WebAttacks.pcap_ISCX.csv
├── Thursday-WorkingHours-Afternoon-Infilteration.pcap_ISCX.csv
├── Friday-WorkingHours-Morning.pcap_ISCX.csv
├── Friday-WorkingHours-Afternoon-PortScan.pcap_ISCX.csv
└── Friday-WorkingHours-Afternoon-DDoS.pcap_ISCX.csv
```

#### processed/

Contiene los datasets transformados y listos para entrenamiento.

#### samples/

Contiene subconjuntos de datos para pruebas rápidas.

---

## Análisis y Experimentación

```text
notebooks/

├── 01_eda.ipynb
├── 02_cleaning.ipynb
├── 03_feature_engineering.ipynb
└── 04_training.ipynb
```

### Responsabilidades

- Análisis exploratorio de datos (EDA).
- Validación de calidad de datos.
- Experimentación y pruebas.
- Documentación de resultados.

---

## Pruebas

```text
tests/
```

Contiene las pruebas unitarias y de integración del proyecto.

---

## Docker

```text
docker/

├── Dockerfile
└── docker-compose.yml
```

Contiene la configuración de contenedores para desarrollo y despliegue.

---

## Flujo del Proyecto

```text
CIC-IDS2017
      │
      ▼
  data/raw
      │
      ▼
 Exploración de Datos
 (01_eda.ipynb)
      │
      ▼
 Limpieza de Datos
 (02_cleaning.ipynb)
      │
      ▼
 Feature Engineering
 (feature_engineering.py)
      │
      ▼
 Dataset Procesado
 (data/processed)
      │
      ▼
 Entrenamiento
 (train.py)
      │
      ▼
 Modelo Entrenado
 (ml/models)
      │
      ▼
 FastAPI
 (app/)
      │
      ▼
 Predicciones
      │
      ▼
 Dashboard y Métricas
```

## Dataset

- CIC-IDS2017

## Modelos de Machine Learning

- Random Forest
- XGBoost (versión futura)

## Hoja de ruta

### Fase 1
- Obtención y comprensión del dataset.
- Limpieza y preparación de datos.
- Análisis exploratorio de datos (EDA).

### Fase 2
- Ingeniería de características.
- Entrenamiento de modelos.
- Evaluación de métricas.

### Fase 3
- Comparación de algoritmos.
- Optimización de hiperparámetros.

### Fase 4
- Visualización de resultados.
- Dashboard interactivo.

### Fase 5
- Integración con técnicas y marcos de ciberseguridad como MITRE ATT&CK.

## Próximas funcionalidades

- [ ] Entrenamiento inicial con Random Forest
- [ ] Comparación con XGBoost
- [ ] API REST con FastAPI
- [ ] Registro de predicciones en base de datos
- [ ] Dashboard con Streamlit
- [ ] Integración básica con MITRE ATT&CK
- [ ] Dockerización del proyecto


