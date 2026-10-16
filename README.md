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

El proyecto está organizado para separar claramente los componentes de Machine Learning, la API y la lógica de negocio.

```text
ids-detector/
├── app/
├── ml/
├── tests/
├── docker/
├── requirements.txt
└── README.md
```

### API (FastAPI)

```text
app/
├── api/
├── core/
├── db/
├── schemas/
├── services/
└── repositories/
```

### Machine Learning

```text
ml/
├── preprocess.py
├── train.py
├── evaluate.py
├── datasets/
└── models/
```

Esta estructura permite mantener separadas las responsabilidades del sistema, facilitando la escalabilidad, el mantenimiento y la integración futura entre los componentes de Machine Learning y la API.

## Flujo del proyecto

```text
                     ┌─────────────────┐
                     │ CIC-IDS2017     │
                     │ Dataset         │
                     └────────┬────────┘
                              │
                              ▼
                     ┌─────────────────┐
                     │ Preprocesamiento│
                     │ preprocess.py   │
                     └────────┬────────┘
                              │
                              ▼
                     ┌─────────────────┐
                     │ Entrenamiento   │
                     │ train.py        │
                     └────────┬────────┘
                              │
                              ▼
                     ┌─────────────────┐
                     │ Random Forest   │
                     │ Modelo ML       │
                     └────────┬────────┘
                              │
                              ▼
              ┌─────────────────────────────────┐
              │ API REST (FastAPI)              │
              │                                 │
              │ /predict                        │
              │ /metrics                        │
              │ /health                         │
              └───────────────┬─────────────────┘
                              │
               ┌──────────────┼──────────────┐
               │              │              │
               ▼              ▼              ▼
      ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
      │Predicciones │ │  Métricas   │ │ Monitoreo   │
      └──────┬──────┘ └──────┬──────┘ └──────┬──────┘
             │               │               │
             └───────┬───────┴───────┬──────┘
                     │               │
                     ▼               ▼
             ┌─────────────────┐
             │ Base de Datos   │
             │ PostgreSQL      │
             └────────┬────────┘
                      │
                      ▼
             ┌─────────────────┐
             │ Dashboard       │
             │ Streamlit       │
             └────────┬────────┘
                      │
                      ▼
             ┌─────────────────┐
             │ MITRE ATT&CK    │
             │ Correlación     │
             └─────────────────┘
```

Este flujo muestra la evolución prevista del proyecto, desde el procesamiento del dataset hasta la exposición de resultados mediante una API REST, almacenamiento de predicciones, visualización en dashboard e integración futura con MITRE ATT&CK.

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


