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

ids-detector/
  app/              # API desarrollada con FastAPI
  ml/               # Entrenamiento y evaluación de modelos
  tests/            # Pruebas automatizadas
  docker/           # Configuración de contenedores
  requirements.txt
  README.md

API (FastAPI)
app/
   api/              # Endpoints y rutas
   core/             # Configuración y seguridad
   db/               # Acceso a base de datos
   schemas/          # Validación de datos
   services/         # Lógica de negocio
   repositories/     # Operaciones de persistencia

Machine Learning
ml/
   preprocess.py     # Limpieza y transformación de datos
   train.py          # Entrenamiento del modelo
   evaluate.py       # Evaluación de métricas
   datasets/         # Conjuntos de datos
   models/           # Modelos entrenados

Esta estructura permite mantener separadas las responsabilidades del sistema, facilitando la escalabilidad, el mantenimiento y la integración futura entre los componentes de Machine Learning y la API.

## Flujo del proyecto

Dataset CIC-IDS2017
        │
        ▼
Preprocesamiento
(preprocess.py)
        │
        ▼
Entrenamiento
(train.py)
        │
        ▼
Modelo de Machine Learning
(Random Forest)
        │
        ▼
API REST (FastAPI)
        │
        ├── Predicciones
        ├── Métricas
        └── Monitoreo
        │
        ▼
Base de datos
        │
        ▼
Dashboard y visualización

Este flujo representa la visión general del sistema, desde la preparación de los datos hasta la exposición de resultados mediante una API y herramientas de visualización.

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


