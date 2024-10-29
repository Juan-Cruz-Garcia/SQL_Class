```mermaid
flowchart TD
    A[Lista de Tareas] -->|Agregar Tarea| B[Agregar Nueva Tarea]
    B -->|Guardar Tarea| A
    B -->|Volver a Lista| A
