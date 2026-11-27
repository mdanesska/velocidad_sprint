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
