# Propuesta metodológica: Vigilancia estratégica de iniciativas Post-Terremoto

A continuación, se presenta la ruta de trabajo estructurada para identificar, seleccionar y caracterizar iniciativas y buenas prácticas implementadas a nivel global tras eventos sísmicos.

## Naturaleza del análisis

El estudio es **descriptivo y se construye sobre valores observados**, no sobre modelos probabilísticos. La selección de países se justifica con el impacto realmente registrado de terremotos ocurridos entre 1990 y 2026, no con proyecciones de riesgo futuro.

## Hoja de ruta

graph TD
    %% Estilos
    classDef fase fill:#2c3e50,stroke:#34495e,stroke-width:2px,color:#fff;
    classDef accion fill:#ecf0f1,stroke:#bdc3c7,stroke-width:1px,color:#2c3e50;
    classDef decision fill:#f39c12,stroke:#e67e22,stroke-width:2px,color:#fff;
    classDef foco fill:#3498db,stroke:#2980b9,stroke-width:2px,color:#fff;

    F1[FASE 1: Priorización]:::fase --> A1[Consulta NOAA NCEI y perfiles GEM]:::accion
    A1 --> A2[Análisis de Indicadores observados: Fallecidos, Daño, Recurrencia]:::accion
    A2 --> A3[Selección Top 15 Países]:::accion

    F2[FASE 2: Documentación]:::fase --> B1[Búsqueda de sismos > 4.0]:::accion
    B1 --> B2[Consolidación de Documentos Claves]:::accion
    A3 -.-> F2

    F3[FASE 3: Búsqueda Enfocada]:::fase --> C1[Exploración Top 5 Países]:::accion
    A3 --> F3
    C1 --> C2{¿Datos suficientes?}:::decision
    C2 -- NO --> C3[Expandir a los otros 10 países]:::accion
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

```


---

## Detalle operativo por fases

### Fase 1: Perfilamiento y priorización de países
**Objetivo:** Definir y justificar cuantitativamente una muestra (Top 15) de países a partir del **impacto sísmico observado** entre 1990 y 2026, para enfocar la búsqueda de iniciativas.

* **Fuente de selección:** [NOAA / NCEI, *Global Significant Earthquake Database*](https://www.ncei.noaa.gov/products/natural-hazards/tsunamis-earthquakes-volcanoes/earthquakes) (doi 10.7289/V5TD9V7K), consultada mediante la herramienta HazEL. Se trata de datos de eventos realmente ocurridos, no de proyecciones de riesgo.
* **Filtros aplicados:** año igual o posterior a 1990, magnitud igual o superior a 4.0, exclusión de eventos con bandera volcánica y de eventos sin impacto documentado. Base resultante: **1.507 eventos en 109 países**.
* **Extracción de variables clave:** de cada evento se extraen fallecidos, heridos, daño económico, viviendas destruidas y viviendas dañadas. Agregadas por país, estas variables producen tres ordenamientos independientes: **fallecidos acumulados, daño acumulado y número de eventos con impacto**.
* **Criterio de selección:** el impacto no es una sola variable, de modo que la muestra se define por **intersección**: los países que se ubican entre los veinte primeros en los tres rankings a la vez (8 países). Los 7 restantes se incorporan por **priorización declarada y vinculada a los focos** del estudio, hasta completar 15.
* **Fuente de contexto:** los [perfiles de riesgo sísmico de GEM](https://www.globalquakemodel.org/product/global-seismic-risk-map) aportan los indicadores sociales (Población, PIB, Índice Gini), las clases constructivas, las prefecturas o divisiones con mayor nivel de pérdida, y la **razón de pérdida anual promedio (AALR)** como indicador de vigencia del riesgo. Al ser resultado de un modelo probabilístico y no de eventos ocurridos, **no participan en la selección ni en el orden de los países**.
* **Eventos ancla:** de la base NOAA se extraen, por país, los terremotos de mayor impacto con año, magnitud, localidad, fallecidos y daño. Son el punto de partida de la Fase 3, porque la mayoría de las iniciativas nace como respuesta institucional a un evento concreto.
* **Entregable (Ficha 1 - Contexto_país):** documento que consolida el Top 15 de países priorizados. La inclusión de cada país se justifica con su posición en los tres rankings observados y con el criterio de entrada declarado (intersección o priorización por foco), acompañada del AALR como nota de vigencia del riesgo.

### Fase 2: Soporte documental (Marco de referencia)
**Objetivo:** Establecer la base teórica e histórica que respalde la investigación.
* **Metodología de rastreo:** Búsquedas estructuradas y desestructuradas en español e inglés sobre eventos sísmicos con magnitudes superiores a 4.0.
* **Entregable (Ficha 2 - Documentos claves):** Consolidado de literatura y reportes oficiales que servirán como soporte documental de la vigilancia.

### Fase 3: Búsqueda enfocada de iniciativas
**Objetivo:** Rastrear iniciativas gubernamentales e institucionales de acceso gratuito en la web.
* **Despliegue inicial:** La exploración arranca en los **primeros 5 países** del Top 10. Si no se halla información suficientemente documentada o accesible para caracterizar las prácticas, se procede con una reorientación estratégica hacia los 5 países restantes de la muestra.
* **Tips de búsqueda:**
  * **Filtros por dominio local:** Modificación de la ubicación en navegadores y uso restrictivo de dominios específicos por país (Ej. `site:.go.jp` para rastrear ministerios en Japón).
  * **Búsqueda por hitos y entidades:** Evitar términos genéricos que arrojan ruido (ej. *"buenas prácticas de salud mental en Japón"*). En su lugar, rastrear instituciones con nombre propio creadas tras desastres específicos (ej. *"qué se creó después de Kobe 1995"*).
  * **Geolocalización del desastre:** Emplear los nombres exactos de las ciudades o prefecturas con mayores afectaciones (identificadas en la Fase 1) para hallar programas de recuperación locales.

### Fase 4: Caracterización y extracción de datos
**Objetivo:** Sistematizar las iniciativas vigentes (de los últimos 40 años) extraídas de portales gubernamentales, redes sociales oficiales y canales de noticas locales.
* **Entregable (Ficha 3 - Matriz de caracterización):** Instrumento central de la vigilancia donde se desglosa cada iniciativa utilizando las siguientes unidades de análisis: *País, Región/Ciudad, Evento sísmico/Año, Nombre de la iniciativa, Entidad responsable, Tipo de entidad, Descripción, Población objetivo, Cobertura reportada, Resultado esperado y URLs de soporte*.
* **Clasificación por focos estratégicos:** Cada iniciativa documentada se categoriza obligatoriamente en uno de los 4 ejes definidos:
  1. **Salud mental, bienestar humano y animal**
  2. **Recuperación económica empresarial.**
  3. **Continuidad educativa y educación en gestión del riesgo.**
  4. **Políticas públicas y datos para futuras emergencias.**
