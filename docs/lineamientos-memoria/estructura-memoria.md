# ESTRUCTURA DE MEMORIA TÉCNICA - INTELIGENCIA ARTIFICIAL
Taller de Trabajo Final - Estructura de subsecciones, páginas estimadas, contenido y recomendaciones

---

## CAPÍTULO 1: Introducción general
* **Descripción**: Contextualizar el problema que se aborda con IA: dominio de aplicación, relevancia y estado actual.
* **Páginas estimadas**: 5.
* **Notas**: No incluir requerimientos. Explicar la problemática a alguien no experto en IA.

| Nº Sección | Titulo de la sección | Descripción del contenido | Páginas | Figuras / Tablas sugeridas | Notas y recomendaciones |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | Introducción general al tema | Explicación introductoria del área para preparar al lector. | 1 | Imagen ilustrativa del concepto del área. | - |
| 1.2 | Contexto y motivación | Describir el problema, por qué la IA es adecuada y la motivación. | 1 | - | Redactar en forma clara y concisa. |
| 1.3 | Estado del arte | Revisar trabajos previos, problemas relacionados y técnicas de IA utilizadas. | 2 | Tabla comparativa de enfoques (modelo, dataset, métricas). | Es obligatorio. |
| 1.4 | Objetivos del trabajo | Enunciar qué se busca predecir/clasificar/generar y métricas de evaluación. | - | - | Deben ser concretos y verificables. |

---

## CAPÍTULO 2: Introducción específica
* **Descripción**: Describir frameworks, datasets, herramientas y modelos preentrenados de terceros.
* **Páginas estimadas**: 5.
* **Notas**: Incluir todo lo mencionado en el Cap. 3 que no fue desarrollado por el autor.

| Nº Sección | Titulo de la sección | Descripción del contenido | Páginas | Figuras / Tablas sugeridas | Notas y recomendaciones |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 2.1 | Frameworks y bibliotecas | Describir herramientas como TensorFlow, PyTorch, Keras, etc. | 1-2 | - | Justificar la elección. |
| 2.2 | Datasets y datos | Origen, tamaño, características y licencia de los datos. | 1-2 | Tabla descriptiva y histogramas de distribución. | Indicar si se usaron datos propios. |
| 2.3 | Modelos preentrenados | Describir modelos usados para transfer learning o punto de partida. | 1 | Tabla de modelos, arquitectura y dataset de preentrenamiento. | Solo si aplica transfer learning o fine-tuning. |
| 2.4 | Infraestructura | Describir hardware (GPU), plataformas cloud, etc. | - | - | Ej: Google Colab, AWS, GPU local. |

---

## CAPÍTULO 3: Diseño e implementación
* **Descripción**: Describir el pipeline de datos, arquitectura del modelo e implementación del sistema.
* **Páginas estimadas**: 15-20.
* **Notas**: Incluir el pipeline completo y evitar bloques de código extensos.

| Nº Sección | Titulo de la sección | Descripción del contenido | Páginas | Figuras / Tablas sugeridas | Notas y recomendaciones |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 3.1 | Pipeline de datos | Proceso desde recolección hasta preprocesamiento y augmentation. | 3-4 | Diagrama del pipeline y ejemplos visuales. | Explicar todas las transformaciones aplicadas. |
| 3.2 | Arquitectura del modelo | Descripción de capas, parámetros y función de pérdida. | 3-4 | Diagrama de arquitectura y tabla de capas. | Justificar las decisiones de diseño. |
| 3.3 | Entrenamiento | Hiperparámetros, optimizador, scheduler y regularización. | 2-3 | Diagrama de flujo de los procesos. | Incluir búsqueda de hiperparámetros si se realizó. |
| 3.4 | Integración del sistema | Integración en API, interfaz de usuario o sistema embebido. | 3-4 | Diagrama de arquitectura del sistema completo. | Incluir el flujo de inferencia en producción. |

---

## CAPÍTULO 4: Ensayos y resultados
* **Descripción**: Evaluación del modelo y del sistema completo con análisis de resultados.
* **Páginas estimadas**: 10-15.
* **Notas**: Usar métricas del Cap. 1 e incluir análisis de errores.

| Nº Sección | Titulo de la sección | Descripción del contenido | Páginas | Figuras / Tablas sugeridas | Notas y recomendaciones |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 4.1 | Plan de evaluación | Metodología de evaluación: métricas, sets de test y condiciones. | 1 | - | Definir claramente train/validation/test split. |
| 4.2 | Evaluación del modelo | Presentar resultados con las métricas definidas. | 3-4 | Matriz de confusión, curvas ROC/PR, tablas de métricas. | Comparar con baseline o estado del arte. |
| 4.3 | Análisis de errores | Analizar fallos: tipos de errores, patrones y causas. | 2-3 | Ejemplos de predicciones incorrectas y casos límite. | Tan importante como las métricas de performance. |
| 4.4 | Ensayos de integración | Pruebas del sistema completo integrado. | 2-3 | Capturas del sistema, tiempos de inferencia y escenarios reales. | Verificar comportamiento en condiciones reales. |

---

## CAPÍTULO 5: Conclusiones
* **Descripción**: Resumir aportes, comparar con el estado del arte y proponer trabajo futuro.
* **Páginas estimadas**: 2.
* **Notas**: Sin tablas ni imágenes.

| Nº Sección | Titulo de la sección | Descripción del contenido | Páginas | Notas y recomendaciones |
| :--- | :--- | :--- | :--- | :--- |
| 5.1 | Logros alcanzados | Análisis de cumplimiento de objetivos originales. | - | Indicar dónde se supera o no el estado del arte. |
| 5.2 | Conocimientos aplicados | Mencionar conocimientos de la carrera aplicados. | 0.5 | Ej: ML, estadística, programación. |
| 5.3 | Trabajo futuro | Proponer mejoras en datos, arquitectura o despliegue. | 0.5 | Pensar en la evolución del modelo y sistema. |