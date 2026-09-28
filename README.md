# diagramadeflujo
```mermaid
flowchart TD

    A([Inicio]) --> B["El usuario abre la aplicación"]

    B --> C["Registrar hora y coordenadas de acceso"]

    C --> D{"¿Hora de entrada antes de las 08:00?"}

    D -->|Sí| E{"¿Ubicación dentro del área de trabajo<br>con margen de hasta 50 m?"}

    D -->|No| G["Registrado y advertencia"]

    E -->|Sí| F["Registrado y OK"]

    E -->|No| G

    F --> H([Fin])

    G --> H

  

    classDef process fill:#eef2ff,stroke:#818cf8,color:#1e1b4b;

    classDef decision fill:#fefce8,stroke:#facc15,color:#422006;

    classDef ok fill:#f0fdf4,stroke:#4ade80,color:#052e16;

    classDef warning fill:#fef2f2,stroke:#f87171,color:#450a0a;

  

    class B,C process;

    class D,E decision;

    class F ok;

    class G warning;
