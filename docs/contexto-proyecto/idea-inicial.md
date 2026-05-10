# DAGO: Sistema de análisis digital de oscilaciones gestuales en pacientes con Parkinson mediante IA

## Nombre de la organización que propone el Trabajo Final

Trabajo personal

## Datos de contacto

Alex Barria, alexbarria14@gmail.com

## Objetivo

Desarrollar una herramienta tecnológica basada en inteligencia artificial que permita realizar un seguimiento cuantitativo y objetivo de los movimientos involuntarios en pacientes con Parkinson, aportando métricas precisas para complementar las evaluaciones clínicas tradicionales.

## Introducción general al tema

La enfermedad de Parkinson se caracteriza por alteraciones motrices que incluyen temblores, rigidez y movimientos oscilatorios involuntarios. Actualmente, los neurólogos evalúan el progreso de los pacientes mediante observaciones visuales de ejercicios específicos, como movimientos de brazos, estabilidad de la mano, movimientos de dedos, caminatas y postura general. Estas evaluaciones, si bien clínicas, pueden ser subjetivas y poco sensibles a cambios sutiles.

El proyecto, denominado DAGO (Digital Analysis for Gestural Oscillations), propone desarrollar un sistema automatizado de seguimiento que, a partir de videos capturados durante estos ejercicios, analice el comportamiento motor del paciente usando técnicas de visión por computadora y modelos de aprendizaje automático. Esto permitirá generar métricas objetivas y visualizaciones claras que acompañen al profesional en el proceso de evaluación.

En la Figura 1 se presenta el diagrama en bloques de los módulos que compondrían la solución, donde se observan los principales componentes involucrados: captura de video, preprocesamiento, detección de pose corporal, extracción de métricas y visualización de resultados.

![Figura 1. Diagrama en bloques de los módulos de la solución propuesta](ruta/a/la/figura-1)

**Figura 1. Diagrama en bloques de los módulos de la solución propuesta**

## Descripción detallada

El sistema estará compuesto por los siguientes módulos:

- **Captura de video:** Se realizarán grabaciones de pacientes ejecutando una serie de ejercicios motrices recomendados clínicamente.

- **Preprocesamiento:** Las imágenes serán limpiadas, estabilizadas y preparadas para su análisis.

- **Modelo de IA:** Se emplearán modelos de estimación de pose corporal, posiblemente combinados con técnicas de estimación de profundidad, para identificar y seguir los movimientos clave.

- **Extracción de métricas:** A partir de los puntos clave detectados, se calcularán métricas como amplitud de oscilación, frecuencia de temblores, regularidad del movimiento, y estabilidad postural.

- **Visualización y resultados:** Se generarán reportes visuales que destaquen la evolución del paciente en base a los registros históricos.

La herramienta funcionará inicialmente en forma de prototipo (Proof of Concept) y se buscará validar su precisión frente a evaluaciones realizadas por profesionales médicos. Se trabajará también en una arquitectura tecnológica modular que permita escalar la solución y adaptarla a diferentes entornos clínicos en etapas posteriores.

## Disponibilidad de datos

El proyecto comenzará utilizando modelos preentrenados disponibles para las distintas tareas mencionadas anteriormente. En caso de que la performance de la solución no cumpla con los resultados esperados, se evaluará el entrenamiento de los modelos necesarios utilizando un conjunto de videos previamente grabados de pacientes reales realizando ejercicios clínicos específicos. Actualmente, se cuenta con algunos de estos videos para realizar pruebas y evaluar el funcionamiento de la herramienta. Sin embargo, si se requiere un dataset más amplio para llevar a cabo tareas de entrenamiento de modelos de aprendizaje automático, será necesario generarlo.