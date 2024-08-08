# Predicción del Rendimiento Académico.
Este proyecto tiene como objetivo analizar el rendimiento académico de los estudiantes de una institución educativa y desarrollar un modelo predictivo para identificar factores clave que influyen en las notas finales. El dataset proporcionado contiene información sobre el cursado de los estudiantes, incluyendo entregas, exámenes y vencimiento de tareas.

## Installation
### Clone the repository:

`git <clone repository-url>`
`cd <repository-name>`

### Create a virtual environment and activate it:
`python -m venv em_venv`
`source em_venv/bin/activate`  # On Windows use `em_venv\Scripts\activate`

### Install the dependencies:
`pip install -r requirements.txt`

## Estructura del Proyecto
- data: Contiene los datasets originales y procesados.
- challenge_edMachina.csv: Dataset original proporcionado.
- df_entregas.csv, df_estudiantes.csv: Datasets procesados.
- models: Almacena los modelos entrenados.
- model_xgboost.pkl: Ejemplo de un modelo XGBoost entrenado.
- notebooks: Jupyter Notebooks utilizados para el análisis y modelado.
- modelado.ipynb: Desarrollo y evaluación de modelos predictivos.
- preprocessed.ipynb: Preprocesamiento y limpieza de datos.
- visualizacion.ipynb: Análisis exploratorio de datos y visualizaciones.
- .gitignore: Especifica archivos y carpetas que Git debe ignorar.
- README.md: Este archivo, que proporciona una descripción general del proyecto.
- requirements.txt: Lista las dependencias del proyecto para facilitar la instalación.

## Dataset
### El DataFrame df_estudiantes contiene las siguientes columnas:

Identificadores y Metadatos:
- user_uuid: ID del usuario.
- course_uuid: ID del curso.
- legajo: Identificación administrativa del estudiante.
- course_name: Nombre del curso.
- periodo: Período de cursado (e.g., 1-2022).
- particion: Partición temporal (día del cursado).
Evaluación y Rendimiento:
- fecha_mesa_epoch: Fecha del examen en formato epoch.
- nombre_examen: Tipo de examen rendido.
- nota_parcial: Nota obtenida en el examen parcial.
- nota_final_materia: Nota final en la materia.
- aprobado: Indicador de si aprobó (1) o no (0).
- rango_nota: Categoría de la nota (e.g., alto, medio).
- diferencia_notas: Diferencia entre notas.
- promedio_nota_parcial: Promedio de las notas parciales.
- std_nota_parcial: Desviación estándar de las notas parciales.
- num_actividades: Número de actividades completadas.
- puntaje_total: Puntaje total acumulado.
- num_tareas: Número de tareas entregadas.
- mean_puntaje_tareas: Puntaje promedio en las tareas.
- dias_mean_antes_vencimiento: Días promedio antes del vencimiento de las tareas.


### El DataFrame df_entregas contiene las siguientes columnas:

Identificadores y Metadatos:
- user_uuid: ID del usuario.
- course_uuid: ID del curso.
- legajo: Identificación administrativa del estudiante.
- course_name: Nombre del curso.
- periodo: Período de cursado (e.g., 1-2022).
- particion: Partición temporal (día del cursado).
- assignment_id: ID de la tarea asignada.
- ass_name: Nombre de la tarea.
- ass_name_sub: Nombre de la sub-tarea (si aplica).
- sub_uuid: ID de la entrega de la tarea.
- submission_type: Tipo o formato de entrega.
Fechas y Tiempos:
- ass_created_at: Fecha de creación de la tarea.
- ass_due_at: Fecha de vencimiento de la tarea.
- ass_unlock_at: Fecha de apertura de la tarea.
- ass_lock_at: Fecha de cierre de la tarea.
- s_submitted_at: Fecha de entrega.
- s_graded_at: Fecha de corrección.
Rendimiento y Métricas:
- score: Puntaje obtenido en la tarea.
- promedio_score: Promedio de los puntajes obtenidos.
- std_score: Desviación estándar de los puntajes obtenidos.
- total_score: Puntaje total acumulado.
- tiempo_entrega: Tiempo tomado para entregar la tarea.
- tiempo_calificacion: Tiempo tomado para corregir la tarea.
- dias_antes_vencimiento: Días antes del vencimiento que la tarea fue entregada.
- on_time: Indicador de si la tarea fue entregada a tiempo (a_tiempo) o no (no_entregado).


#### Nota: El análisis exploratorio está en desarrollo (Los datos están siendo interrogados, y no están cooperando del todo!) Si bien se obtuvieron insights preliminares, se continua trabajando para comprender completamente los datos y extraer conclusiones.  

Este proyecto sienta las bases para esclarecer los secretos del rendimiento académico. A través del análisis de datos y la construcción de modelos predictivos, buscamos identificar los factores que impulsan el éxito estudiantil. Cada paso nos acerca a valiosas ideas que pueden transformar la forma en que entendemos y apoyamos el aprendizaje! 🌱