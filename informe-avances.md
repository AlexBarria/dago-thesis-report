# Informe de Avance del Trabajo Final
**Maestría en Inteligencia Artificial, FIUBA**

---

## Información General

* **Título del Trabajo**: DAGO: sistema de análisis digital de oscilaciones gestuales en pacientes con Parkinson mediante IA.
* **Autor**: Esp. Ing. Alex D. Barria C.
* **Director del trabajo**: PhD. Ing. Fernando Bernuy (Universidad Nacional de Chile).
* **Marco**: Informe de avance correspondiente al Trabajo Final de la Maestría en Inteligencia Artificial, elaborado en mayo de 2026 en el marco de la asignatura Gestión de Proyectos.

---

## 1. Breve resumen del trabajo realizado hasta la fecha

### 1.1 Descripción sintética del Trabajo Final

El Trabajo Final consistió en el diseño e implementación de DAGO (*Digital Analysis for Gestural Oscillations*), un sistema que cuantifica de manera objetiva los movimientos involuntarios y la regularidad gestual en pacientes con enfermedad de Parkinson a partir de videos de ejercicios clínicos. El sistema combina estimación automática de pose corporal, procesamiento de señales temporales y una interfaz web que permite cargar sesiones, inspeccionar gráficos y exportar reportes estructurados, con el propósito de complementar las escalas observacionales, en particular la parte motora del MDS-UPDRS, mediante métricas reproducibles. La descripción detallada del alcance, los requerimientos y el cronograma original se encuentran en el Plan de Trabajo entregado oportunamente al jurado.

En la figura 1 se muestra el flujo funcional de la solución, organizado en módulos encadenados desde la ingestión del video hasta la visualización de resultados.

![Figura 1. Diagrama en bloques del sistema DAGO.](Figures/cap_1/finger_tapping.png)

**Figura 1. Diagrama en bloques del sistema DAGO**

```
Video crudo
    ↓
Ingestión y preprocesamiento (estabilización, fase estática, calibración ChArUco)
    ↓
Estimación de pose corporal (MediaPipe Pose)
    ↓
Seguimiento temporal de keypoints y señales derivadas
    ↓
Extracción de métricas (amplitud, frecuencia, regularidad, estabilidad)
    ↓
Agregación por sesión y persistencia (PostgreSQL)
    ↓
API REST (FastAPI) ← → Frontend web (React + TypeScript)
    ↓
Reportes exportables y visualizaciones interactivas
```

Se observa que el flujo prioriza una arquitectura modular, donde cada bloque funciona como unidad verificable de manera independiente, y que la separación entre el pipeline de procesamiento, la API y el frontend habilita su despliegue tanto en entorno local mediante Docker como en la nube sobre Google Cloud Platform.

### 1.2 Estado de avance del proyecto a la fecha

A la fecha de este informe se completó el desarrollo de los componentes técnicos centrales del sistema, validados mediante pruebas unitarias y de integración. El código se encuentra organizado en un único repositorio con tres grandes áreas: el pipeline de análisis en Python, una API construida con FastAPI y una aplicación web en React. La base de datos quedó versionada con migraciones gestionadas por Alembic y todo el entorno se encuentra dockerizado.

En el cuadro 1 se resume el estado de cada paquete de trabajo del WBS definido en el Plan de Trabajo. Para la valoración se utilizó el código de colores institucional: verde para tareas con avance satisfactorio, amarillo para tareas en curso con cumplimiento esperado dentro del cronograma y blanco para tareas aún no iniciadas según planificación. La columna de evidencia indica los componentes verificables que respaldan cada estado.

**Cuadro 1. Estado de avance por paquete de trabajo**

| WBS | Paquete de trabajo | Horas plan. | Estado | Evidencia |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Planificación y diseño del sistema | 128 | Verde | Documentos de contexto, diagrama de arquitectura, capítulo 1 redactado. |
| 2 | Adquisición y preparación de datos | 112 | Verde | Conjunto de videos curados, módulos de ingestión, fase estática y calibración ChArUco operativos. |
| 3 | Desarrollo del sistema de análisis gestual | 120 | Verde | Integración de MediaPipe Pose, módulos de métricas (amplitud, frecuencia, regularidad, estabilidad) y suite de pruebas unitarias. |
| 4 | Visualización y generación de reportes | 64 | Verde | Frontend con páginas de carga, resultados, comparación y exportación; gráficos resumen y router de reportes. |
| 5 | Diseño de infraestructura y PoC | 80 | Verde | `docker-compose` funcional, despliegue de prueba sobre Google Cloud Platform, scripts de migración Alembic. |
| 6 | Documentación y cierre académico | 96 | Amarillo | README técnico completo, capítulo 1 de la memoria redactado; capítulos 2 a 5 e iteraciones de revisión en curso. |

El avance global estimado, ponderado por horas planificadas, supera el ochenta por ciento. Los paquetes 1 a 5 (504 horas, equivalentes al 84 % del esfuerzo total) se encuentran completados en su núcleo funcional, mientras que el paquete 6 (96 horas) presenta avance parcial, asociado principalmente a la redacción de la memoria.

En el cuadro 2 se detalla el estado funcional de los módulos de software, agrupados por subsistema, para evidenciar que los componentes que sustentan la evaluación académica del producto ya se encuentran operativos.

**Cuadro 2. Estado funcional de los módulos de software**

| Subsistema | Componentes principales | Estado | Observaciones |
| :--- | :--- | :--- | :--- |
| Pipeline de análisis | `ingestion`, `preprocessing`, `pose`, `tracking`, `metrics`, `analytics`, `cli` | Operativo | Cubierto por pruebas unitarias (`test_amplitude`, `test_frequency`, `test_regularity`, `test_static_phase`, `test_calibration`, entre otras) y prueba de integración `test_cli_smoke`. |
| API REST | `routers/patients`, `sessions`, `insights`, `report`, `compare`, `auth`, `files` | Operativo | Persistencia con PostgreSQL, autenticación por tokens y worker para tareas asincrónicas. |
| Frontend web | Páginas Upload, Results, Patients, Compare, Export y componentes de gráficos y overlays | Operativo | Comunicación con la API mediante cliente TypeScript; flujos verificados manualmente sobre videos de prueba. |
| Infraestructura | `Dockerfile`, `docker-compose.yml`, `nginx.conf`, migraciones Alembic, despliegue en GCP | Operativo | El sistema completo levanta de forma reproducible tanto en entorno local como en la nube. |
| Documentación | `README.md` técnico y memoria académica en LaTeX | En curso | Documentación de uso y arquitectura completa; memoria con capítulo 1 finalizado. |

Las pruebas automatizadas se ejecutan sobre los componentes críticos del flujo de procesamiento y constituyen la base de la verificación continua del sistema. La existencia de pruebas estables sobre módulos como detección de fase estática, calibración con tablero ChArUco, extracción de métricas de *finger tapping* y seguimiento temporal de puntos clave permite afirmar que las funcionalidades centrales se encuentran consolidadas.

### 1.3 Tareas pendientes y justificación de su cierre antes del Taller de Trabajo Final

El pendiente se concentra en el paquete 6 del WBS (documentación y cierre académico): redacción de los capítulos 2 a 5, revisión del documento completo y presentación oral de defensa. El resto del cronograma se reporta como completado o en etapa final de pulido.

Se estima cerrar ese saldo antes del Taller de Trabajo Final porque el núcleo experimental ya quedó fijado (objeto de la memoria probado, con bajo riesgo de retrabajo por cambios en el sistema), la estructura modular del código y las pruebas unitarias aportan evidencia directa para los capítulos 3 y 4 sin nuevas implementaciones, y las 74 horas reservadas en el paquete 6 para redacción y revisiones resultan coherentes con el ritmo observado en el capítulo 1.

Para el control se mantienen reuniones periódicas con el director. Si una revisión excede el plazo previsto, la prioridad recae en los capítulos 3 y 4; el refinamiento del capítulo 2 y los anexos puede diferirse al propio Taller sin comprometer el avance mínimo exigido para la cursada.
