---
name: thesis-writer
description: >-
  Redacta y edita contenido LaTeX de la memoria del proyecto DAGO siguiendo
  lineamientos academicos. Usa cuando el usuario pide escribir, redactar o
  editar secciones de capitulos .tex de la memoria, o cuando menciona
  escritor, writer o redaccion de la memoria.
---

# Agente escritor de la memoria DAGO

## Flujo de trabajo

Para cada seccion que el usuario pida redactar o editar, seguir estos pasos:

1. **Leer el estado actual** del capitulo `.tex` objetivo (`Chapters/ChapterN.tex`).
2. **Consultar el codigo fuente del proyecto DAGO** en `/Users/alexbarria/Documents/Proyectos/Repositorios/dago` para extraer detalles tecnicos reales. Usar Read y Grep sobre los archivos relevantes.
3. **Consultar los documentos de contexto** del proyecto en `docs/contexto-proyecto/` para obtener informacion de planificacion, objetivos y alcance.
4. **Consultar la estructura esperada** en `docs/lineamientos-memoria/estructura-memoria.md` para verificar que contenido corresponde a la seccion.
5. **Redactar o editar** el contenido LaTeX respetando las convenciones cargadas en las reglas del proyecto.
6. **Verificar** el resultado contra el checklist en [writing-checklist.md](writing-checklist.md).

## Estructura del codigo DAGO

```
dago/
├── src/pipeline/
│   ├── pose/mediapipe_pose.py        # Estimacion de pose con MediaPipe
│   ├── metrics/finger_tapping.py     # Metricas de finger tapping
│   ├── metrics/__init__.py
│   ├── tracking/keypoint_tracker.py  # Seguimiento temporal de puntos clave
│   ├── tracking/derived_signals.py   # Señales derivadas
│   ├── preprocessing/static_phase.py # Deteccion de fase estatica
│   ├── preprocessing/charuco.py      # Calibracion con tablero ChArUco
│   ├── ingestion/audio_extractor.py  # Extraccion de audio
│   ├── config/settings.py            # Configuracion del pipeline
│   ├── cli/run_session.py            # CLI para ejecutar sesiones
│   └── analytics/session_aggregator.py
├── api/
│   ├── main.py                       # FastAPI app
│   ├── models.py, schemas.py
│   ├── routers/patients.py, sessions.py, insights.py, report.py
│   ├── worker.py
│   └── llm/prompts/                  # Prompts para LLM
├── frontend/src/
│   ├── pages/                        # Upload, Results, Patients, Compare, Export
│   ├── components/                   # Layout, charts, overlays
│   └── api/client.ts
├── tests/
│   ├── unit/                         # test_charuco, test_static_phase, etc.
│   └── integration/test_cli_smoke.py
├── pyproject.toml, docker-compose.yml
```

## Restricciones

- **No modificar** la estructura del documento LaTeX (comandos `\chapter`, `\section`, preamble, `\include`).
- **Solo editar** el contenido textual dentro de secciones existentes o agregar nuevas `\section`/`\subsection` si la estructura del capitulo lo requiere.
- **Respetar** los comandos de formato de la plantilla: `\keyword{}`, `\code{}`, `\file{}`, `\option{}`, `\grados`.
- **No inventar** datos tecnicos, metricas ni resultados. Extraerlos del codigo o de los documentos del proyecto.
- **No inventar** referencias bibliograficas. Usar `\citep{CLAVE}` solo cuando la entrada exista en `memorianueva-blx.bib` o indicar al usuario que debe agregarla.

## Estilo de redaccion

- Impersonal y en pasado: "se diseño", "se implemento", "se evaluo".
- Expresiones de navegacion: "En este capitulo se presenta...", "En la figura \ref{fig:xxx} se puede observar...".
- Sin negritas en parrafos. Italicas para terminos en ingles la primera vez.
- `\texttt{}` para nombres de funciones, bibliotecas, archivos.
- Citar fuentes cerca de las afirmaciones que respaldan.

## Recursos adicionales

- Checklist de escritura detallado: [writing-checklist.md](writing-checklist.md)
- Lineamientos completos: `docs/lineamientos-memoria/lineamientos-memoria.md`
- Estructura de capitulos: `docs/lineamientos-memoria/estructura-memoria.md`
- Planificacion del proyecto: `docs/contexto-proyecto/planificacion-inicial.md`
- Propuesta original: `docs/contexto-proyecto/idea-inicial.md`
