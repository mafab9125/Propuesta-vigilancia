# Propuesta metodológica: Vigilancia estratégica de iniciativas Post-Terremoto

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

<Sequence>
  <Step title="Pega los Detalles Operativos finales">
    Finalmente, debajo de lo último que pegaste, añade la explicación de las fases:
  </Step>
</Sequence>

```markdown
---

## Detalle Operativo por Fases

### Fase 1: Perfilamiento y Priorización de Países
El objetivo es confirmar una muestra estadísticamente relevante de países a explorar.
* **Fuente de datos:** Se utiliza el *Global Seismic Risk Map* (Global Quake Model).
* **Extracción:** Se obtienen perfiles de riesgo, identificando prefecturas de mayor pérdida, eventos ancla e indicadores sociales.
* **Entregable:** Ficha "Contexto de amenaza y exposición". Aquí se define el **Top 10 de países priorizados**, justificando cuantitativamente su inclusión mediante indicadores como la Pérdida Anual Promedio (AAL).

### Fase 2: Soporte Documental
Construcción del marco de referencia histórico y técnico.
* **Metodología:** Búsquedas estructuradas en español e inglés en bases de datos sobre sismos históricos superiores a magnitud 4.0.
* **Entregable:** Ficha de "Documentos claves" que sirven como soporte teórico para la vigilancia.

### Fase 3: Búsqueda Enfocada de Iniciativas
Dado que la búsqueda depende de información pública y gratuita en la web, se optimiza el esfuerzo con una estrategia de pivoteo.
* **Despliegue inicial:** Exploración intensiva en los primeros 5 países del Top 10.
* **Pivoteo:** Si no se halla información suficientemente documentada, se transita a los 5 países restantes de la muestra.
* **Tácticas de Búsqueda (Tips):**
  * Modificación de la ubicación del navegador y uso de dominios gubernamentales específicos por país (Ej. `.go.jp` para Japón).
  * Búsqueda por nombres propios de instituciones creadas tras desastres (Ej. post-Kobe 1995) en lugar de términos genéricos.
  * Uso de terminología local de las ciudades más afectadas.

### Fase 4: Caracterización y Extracción
Clasificación de las iniciativas vigentes extraídas de portales gubernamentales y medios oficiales.
* **Entregable:** Matriz de caracterización de iniciativas.
* **Unidades de análisis:** Se evalúa cada iniciativa bajo 4 focos estratégicos:
  1. Salud mental, bienestar humano y animal.
  2. Recuperación económica empresarial.
  3. Continuidad educativa y educación en gestión del riesgo.
  4. Políticas públicas y datos para futuras emergencias.
