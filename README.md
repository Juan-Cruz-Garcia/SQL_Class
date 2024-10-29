# Diagrama ER

```erDiagram
    PERSONAS {
        int id
        string nombre
        string apellido
    }

    CIUDADES {
        int id
        string codigo
        string ciudad
    }

    VUELOS {
        int id
        int origen_id
        int destino_id
        float duracion
    }

    PASAJEROS {
        int persona_id
        int vuelo_id
    }

    PERSONAS ||--o{ PASAJEROS : es
    VUELOS ||--o{ PASAJEROS : tiene
    CIUDADES ||--o{ VUELOS : origen
    CIUDADES ||--o{ VUELOS : destino
