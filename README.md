# Propuesta metodológica: Vigilancia estratégica de iniciativas Post-Terremoto

[👇 **Haz clic aquí para saltar el diagrama e ir directo a los Detalles Operativos**](#detalle-operativo-por-fases)

A continuación, se presenta la ruta de trabajo estructurada para identificar, filtrar y caracterizar las mejores prácticas e iniciativas implementadas a nivel global tras eventos sísmicos.

## Mapa de Ruta

```mermaid
graph TD
    %% Estilos
    classDef fase fill:#2c3e50,stroke:#34495e,stroke-width:2px,color:#fff;
    classDef accion fill:#ecf0f1,stroke:#bdc3c7,stroke-width:1px,color:#2c3e50;
    classDef decision fill:#f39c12,stroke:#e67e22,stroke-width:2px,color:#fff;
    classDef foco fill:#3498db,stroke:#2980b9,stroke-width:2px,color:#fff;

    F1[FASE 1: Priorización]:::fase --> A1[Consulta Global Quake Model]:::accion
    A1 --> A2[Análisis de Indicadores: AAL, Eventos Ancla]:::accion
    A2 --> A3[Selección Top 10 Países]:::accion

    F2[FASE 2: Documentación]:::fase --> B1[Búsqueda de sismos > 4.0]:::accion
    B1 --> B2[Consolidación de Documentos Claves]:::accion
    A3 -.-> F2

    F3[FASE 3: Búsqueda Enfocada]:::fase --> C1[Exploración Top 5 Países]:::accion
    A3 --> F3
    C1 --> C2{¿Datos suficientes?}:::decision
    C2 -- NO --> C3[Expandir a los otros 5 países]:::accion
    C3 --> C4
    C2 -- SÍ --> C4[Aplicar Tips de Búsqueda]:::accion
    
    C4 -.-> T1[Uso de dominios locales ej. .go.jp]
    C4 -.-> T2[Búsqueda por instituciones]

    F4[FASE 4: Caracterización]:::fase
    C4 --> F4
    F4 --> D1[Llenado de Matriz de Análisis]:::accion
    D1 --> D2{Clasificación en 4 Focos}:::decision
    
    D2 --> F_1[1. Salud Mental y Bienestar]:::foco
    D2 --> F_2[2. Recuperación Económica]:::foco
    D2 --> F_3[3. Continuidad Educativa]:::foco
    D2 --> F_4[4. Políticas y Datos]:::foco
