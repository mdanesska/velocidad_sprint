# velocidad_sprint
# **Analizador de Velocidad de Sprint (Métricas SCRUM)**

##**OBJETIVO DE NEGOCIO**

Evaluar el progreso real de un equipo de desarrollo al cierre de un sprint y detectar desequilibrios en la
carga de trabajo.


##**QUÉ DEBE HACER TU CÓDIGO (GUÍA DE TRABAJO)**

  - Limpiar estados y asignaciones: Unificar el texto de los estados (ej. "done" y "Done") y detectar si existen
  tareas huérfanas sin responsable asignado (None).
  - Medir velocidad del equipo: Sumar los puntos totales comprometidos en el sprint frente a los puntos
  completados (Done) para obtener el porcentaje real de avance.
  - Auditar carga por persona: Calcular cuántos puntos tiene asignados cada integrante del equipo y emitir una
  alerta si alguien concentra más del 40 % del trabajo total.

##**DATASET SIMULADO (PYTHON PURO)**
        
        tareas_sprint = [
        {"id": "T-01", "historia": "Login de usuarios", "puntos": 5, "estado": "Done",
        "responsable": "Marta"},
        {"id": "T-02", "historia": "Base de datos clientes", "puntos": 8, "estado": "Done",
        "responsable": "Carlos"},
        {"id": "T-03", "historia": "API de pagos", "puntos": 13, "estado": "In Progress",
        "responsable": "Marta"},
        {"id": "T-04", "historia": "Dashboard inicial", "puntos": 5, "estado": "done",
        "responsable": "Lucia"},
        {"id": "T-05", "historia": "Exportar reporte CSV", "puntos": 3, "estado": "To Do",
        "responsable": "Marta"},
        {"id": "T-06", "historia": "Pruebas de seguridad", "puntos": 5, "estado": "In
        Progress", "responsable": None},
        {"id": "T-07", "historia": "Documentacion API", "puntos": 2, "estado": "Done",
        "responsable": "Lucia"},
        {"id": "T-08", "historia": "Optimizacion consultas", "puntos": 8, "estado": "To
        Do", "responsable": "Marta"}
        ]


# CONCLUSIONES FINALES
# Evaluación de Progreso y Carga de Trabajo al Cierre de Sprint

## 1. Problema de negocio
Al cerrar un sprint, no basta con revisar el número de tareas cerradas: es clave medir el avance real en story points, detectar tareas sin dueño asignado que puedan bloquear el cierre y comprobar si el trabajo está concentrado en una sola persona.

## 2. Métricas calculadas
- **Limpieza y detección de huérfanas:** Normalización de estados (ej. `"done"` → `"Done"`) e identificación de tareas con `responsable` en `None`.
- **Velocidad del sprint:** Total de puntos comprometidos, puntos completados (`Done`) y porcentaje real de avance.
- **Auditoría de carga:** Puntos y porcentaje del total asignados a cada integrante, con alerta automática si supera el **40 %**.

## 3. Principales hallazgos
- **Avance del sprint:** Se completaron **20 de 49 puntos** (**40.8 %**), quedando 29 puntos pendientes entre *In Progress* y *To Do*.
- **Tarea sin responsable:** `T-06` (*Pruebas de seguridad*, **5 puntos**, *In Progress*) figura sin responsable asignado (`None`).
- **Desequilibrio de carga:** **Marta** acumula **29 de 49 puntos** (**59.2 %** del total), superando ampliamente el umbral del 40 % frente a Carlos (8 pts, 16.3 %) y Lucia (7 pts, 14.3 %).