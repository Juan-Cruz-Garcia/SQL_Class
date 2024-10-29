# Diagrama ER

```mermaid
erDiagram
    PERSONAS {

    }

    CIUDADES {
   
    }

    VUELOS {
  
    }

    PASAJEROS {
 
    }

    PERSONAS ||--o{ PASAJEROS : es
    VUELOS ||--o{ PASAJEROS : tiene
    CIUDADES ||--o{ VUELOS : origen
    CIUDADES ||--o{ VUELOS : destino
```

# Diccionario de Datos

| Entidad   | Atributo      | Tipo de Dato | Descripción                               |
|-----------|---------------|--------------|-------------------------------------------|
| PERSONAS  | id            | int          | Identificador único de la persona.       |
|           | nombre        | string       | Nombre de la persona.                     |
|           | apellido      | string       | Apellido de la persona.                   |
| CIUDADES  | id            | int          | Identificador único de la ciudad.        |
|           | codigo        | string       | Código de la ciudad (ej. IATA).          |
|           | ciudad        | string       | Nombre de la ciudad.                      |
| VUELOS    | id            | int          | Identificador único del vuelo.            |
|           | origen_id     | int          | ID de la ciudad de origen.               |
|           | destino_id    | int          | ID de la ciudad de destino.              |
|           | duracion      | float        | Duración del vuelo en horas.              |
| PASAJEROS | persona_id    | int          | ID de la persona que viaja.              |
|           | vuelo_id      | int          | ID del vuelo en el que viaja.            |

## Descripción de Relaciones

- **PERSONAS** a **PASAJEROS**: Una persona puede estar asociada a múltiples registros en la tabla de pasajeros (relación uno a muchos).
- **VUELOS** a **PASAJEROS**: Un vuelo puede tener múltiples pasajeros (relación uno a muchos).
- **CIUDADES** a **VUELOS**: Cada vuelo tiene una ciudad de origen y una ciudad de destino (relación uno a muchos).
