# DAGO: sistema de análisis digital de oscilaciones gestuales en pacientes con Parkinson mediante IA
**Autor:**  
Esp. Ing. Alex D. Barria C.
**Director:**  
PhD. Ing. Fernando Bernuy (Universidad Nacional de Chile)
Esta planificación fue realizada en el curso de Gestión de proyectos entre el 24 de junio de 2025 y el 19 de agosto de 2025.
---
# Índice
1. Descripción técnica-conceptual del proyecto a realizar.  
2. Identificación y análisis de los interesados  
3. Propósito del proyecto  
4. Alcance del proyecto  
5. Supuestos del proyecto.  
6. Requerimientos  
   6.0.1. Requerimientos funcionales  
   6.0.2. Requerimientos de documentación  
   6.0.3. Requerimientos de interfaz  
   6.0.4. Requerimientos de interoperabilidad  
   6.0.5. Requerimientos de testing y validación  
   6.0.6. Requerimientos regulatorios y éticos  
7. Historias de usuarios (Product backlog)  
8. Entregables principales del proyecto  
9. Desglose del trabajo en tareas  
10. Diagrama de Activity On Node.  
11. Diagrama de Gantt  
12. Presupuesto detallado del proyecto  
13. Gestión de riesgos  
14. Gestión de la calidad  
15. Procesos de cierre  
---
# Plan de proyecto del Trabajo Final
## Maestría en Inteligencia Artificial
**Esp. Ing. Alex D. Barria C.**
## Registros de cambios
| Revisión | Detalles de los cambios realizados | Fecha |
|---|---|---|
| 0 | Creación del documento | 24 de junio de 2025 |
| 1 | Se completa hasta el punto 5 inclusive | 07 de julio de 2025 |
| 2 | Se completa hasta el punto 9 inclusive | 15 de julio de 2025 |
| 3 | Se completa hasta el punto 12 inclusive | 31 de julio de 2025 |
| 4 | Se completa hasta el punto 15 inclusive | 6 de agosto de 2025 |
Página 3 de 18
---
# Acta de constitución del proyecto
Buenos Aires, 24 de junio de 2025
Por medio de la presente se acuerda con el Esp. Ing. Alex D. Barria C. que su Trabajo Final de la Maestría en Inteligencia Artificial se titulará “DAGO: sistema de análisis digital de oscilaciones gestuales en pacientes con Parkinson mediante IA” y consistirá en el desarrollo de un sistema de monitoreo digital para realizar seguimiento a pacientes con Parkinson. El trabajo tendrá un presupuesto preliminar estimado de 600 horas y un costo estimado de USD 15.000, con fecha de inicio el 24 de junio de 2025 y fecha de presentación pública el 02 de abril de 2026.
Se adjunta a esta acta la planificación inicial.
**Dr. Ing. Ariel Lutenberg**  
Director posgrado FIUBA
**Alex D. Barria C.**  
Empresa del cliente
**PhD. Ing. Fernando Bernuy**  
Director del Trabajo Final
Página 4 de 18
---
# 1. Descripción técnica-conceptual del proyecto a realizar
El proyecto “DAGO: sistema de análisis digital de oscilaciones gestuales en pacientes con Parkinson mediante IA” tiene como objetivo desarrollar una herramienta tecnológica basada en inteligencia artificial que permita realizar un seguimiento cuantitativo y objetivo de los movimientos involuntarios en pacientes con enfermedad de Parkinson. La motivación principal surge de la necesidad de complementar las evaluaciones clínicas actuales, que en muchos casos dependen de observaciones visuales subjetivas, con métricas objetivas obtenidas mediante procesamiento automatizado de video.
La enfermedad de Parkinson afecta el sistema motor, generando temblores, rigidez y otras disfunciones en el movimiento corporal. Hoy en día, los profesionales médicos evalúan estos síntomas a través de ejercicios específicos como movimientos de brazos, estabilidad de la mano, movimientos de dedos y caminatas. Sin embargo, esta evaluación suele tener un alto componente de subjetividad y no siempre es sensible a cambios leves pero significativos en la progresión de la enfermedad.
La solución propuesta, denominada DAGO (Digital Analysis for Gestural Oscillations), busca automatizar el análisis de estos movimientos a partir de videos capturados durante las sesiones clínicas. Para ello, se utilizarán técnicas de visión por computadora y modelos de aprendizaje automático que permitan identificar la pose corporal, analizar el patrón de movimientos y extraer métricas tales como amplitud de oscilación, frecuencia de temblores, regularidad del movimiento y estabilidad postural.
La herramienta contará con una arquitectura modular y escalable, lo que facilitará su futura adaptación a distintos entornos clínicos. Además, se priorizará la transparencia del sistema para favorecer la interpretación de los resultados por parte del equipo médico.
En la figura 1 se presenta el diagrama en bloques del sistema. Se observa que el flujo funcional incluye los siguientes módulos: captura de video, preprocesamiento, detección de pose corporal, extracción de métricas y visualización de resultados.
## Figura 1. Diagrama en bloques del sistema
Flujo principal:
```text
Videos
  ↓
Preprocesamiento
  ↓
Estimación de profundidad
  ↓
Modelo para detección de puntos clave (MediaPipe Pose)
  ↓
Seguimiento temporal de puntos clave
  ↓
Extracción de métricas específicas
  ↓
Análisis estadístico y agregación de resultados
  ↓
Visualización e informes automatizados

Módulos para análisis de distintos ejercicios.
```
Página 5 de 18

⸻

# 2. Identificación y análisis de los interesados

En el cuadro 1 se puede ver una lista de los interesados en el proyecto, su rol de participación, organización de pertenencia y puesto.

Cuadro 1. Identificación de los interesados

Rol	Nombre y Apellido	Organización	Puesto
Responsable	Alex D. Barria C.	FIUBA	Alumno
Orientador	PhD. Ing. Fernando Bernuy	Universidad Nacional de Chile	Director del Trabajo Final
Usuario final	Profesionales médicos	Centros de salud / hospitales	Evaluadores clínicos

Con el objetivo de potenciar el compromiso de los interesados y mitigar posibles impactos negativos, en el cuadro 2 se lista brevemente un plan de involucramiento de los interesados.

Cuadro 2. Gestión de los interesados

Rol	Comentarios	Canal de comunicación	Periodo
Responsable	Ejecuta el desarrollo del sistema, coordina tareas y documenta avances.	-	-
Orientador	Acompaña el proceso técnico y metodológico. Brinda retroalimentación sobre decisiones de diseño y validación.	Reuniones virtuales / correo electrónico	Mensual
Usuario final	Evaluará la utilidad y precisión de la herramienta. Participará en la validación cruzada entre resultados clínicos y los generados por el sistema.	Reuniones virtuales / correo electrónico	Etapas específicas (inicio y validación)

# 3. Propósito del proyecto

Desarrollar un sistema inteligente que permita cuantificar y visualizar de manera objetiva los movimientos oscilatorios involuntarios en pacientes con enfermedad de Parkinson, a partir del análisis de videos de sesiones clínicas. Esta herramienta busca complementar las evaluaciones tradicionales realizadas por profesionales médicos, brindando métricas precisas y trazables sobre la evolución motriz del paciente. A través del uso de visión por computadora y técnicas de aprendizaje automático, se pretende reducir la subjetividad inherente al diagnóstico clínico y mejorar la sensibilidad para detectar cambios sutiles en el progreso de la enfermedad.

Página 6 de 18

⸻

# 4. Alcance del proyecto

El proyecto incluye:

* Diseño y desarrollo de un sistema de análisis digital para el seguimiento de pacientes con Parkinson.
* Desarrollo de programas en Python para el preprocesamiento de videos de pacientes realizando ejercicios clínicos motrices.
* Implementación de modelos de estimación de pose corporal para la detección de puntos clave del cuerpo del paciente.
* Extracción de métricas cuantitativas tales como amplitud, frecuencia de temblores, regularidad y estabilidad postural.
* Generación de visualizaciones e informes de evolución que puedan ser interpretados por profesionales médicos.
* Documentación técnica del desarrollo del sistema.
* Diseño de la infraestructura tecnológica de la solución, considerando su posible despliegue en entornos cloud. Se entregará un prototipo funcional (PoC) de esta arquitectura cloud.
* Memoria del trabajo final y presentación académica del proyecto.

El presente proyecto no incluye:

* Evaluación funcional del prototipo mediante comparación con evaluaciones clínicas realizadas por especialistas. Esta actividad se realizará únicamente si se cuenta con los recursos humanos y logísticos necesarios, pero no forma parte obligatoria de los entregables.
* Desarrollo de una aplicación móvil o interfaz de usuario final. Se analizará su factibilidad y, en caso de no comprometer los tiempos previstos para las tareas principales, se podrá implementar como valor agregado. Sin embargo, no es un entregable obligatorio.
* Entrenamiento desde cero de modelos de aprendizaje profundo (se utilizarán modelos preentrenados).
* Desarrollo de una infraestructura de integración con sistemas hospitalarios existentes.
* Certificación médica o trámites regulatorios para uso sanitario.

# 5. Supuestos del proyecto

Para el desarrollo del presente proyecto se supone que:

* El responsable del proyecto (Esp. Ing. Alex D. Barria C.) contará con la disponibilidad horaria necesaria para ejecutar las tareas planificadas dentro de los plazos establecidos.
* El orientador del proyecto estará disponible para brindar asistencia técnica, validación conceptual y revisión periódica de los avances.
* Se podrá acceder a modelos preentrenados de estimación de pose y herramientas de visión por computadora de código abierto.
* Los recursos computacionales disponibles (locales o en la nube) serán suficientes para realizar el procesamiento de los videos y la ejecución de los modelos de IA.
* Se contará con una cantidad mínima de videos clínicos grabados de pacientes con Parkinson para pruebas y validación preliminar del sistema.
* En caso de ser necesario generar un dataset adicional, se dispondrá de los medios para realizar nuevas grabaciones en contextos controlados.
* No se requerirá intervención directa de instituciones médicas para la fase inicial del proyecto, aunque se buscará validar resultados con usuarios finales si las condiciones lo permiten.
* Las condiciones macroeconómicas y la estabilidad de acceso a herramientas digitales (plataformas cloud, bibliotecas, almacenamiento) se mantendrán razonablemente constantes durante el periodo de ejecución del proyecto.

Página 8 de 18

⸻

# 6. Requerimientos

Los requerimientos del sistema se agrupan por tipo y se detallan a continuación, indicando su prioridad (alta, media o baja).

6.0.1. Requerimientos funcionales

1.1. El sistema debe permitir la carga y procesamiento de videos de pacientes realizando ejercicios clínicos. (Alta)

1.2. El sistema debe aplicar un modelo de estimación de pose corporal para extraer puntos clave del cuerpo. (Alta)

1.3. A partir de los puntos clave, el sistema debe calcular métricas como amplitud, frecuencia de temblores, regularidad del movimiento y estabilidad postural. (Alta)

1.4. El sistema debe generar visualizaciones que representen la evolución de las métricas a lo largo del tiempo. (Alta)

1.5. El sistema debe exportar reportes en formato PDF o similar con los resultados obtenidos. (Baja)

6.0.2. Requerimientos de documentación

2.1. El sistema debe contar con documentación técnica que describa su arquitectura, módulos, flujo de datos y dependencias. (Alta)

2.2. Se debe elaborar una memoria detallada del proyecto final que incluya resultados, análisis y lecciones aprendidas. (Alta)

6.0.3. Requerimientos de interfaz

3.1. La interfaz del prototipo debe permitir seleccionar el video a procesar y mostrar los resultados en forma visual. (Opcional)

3.2. La interfaz debe ser accesible desde un navegador local (basada en interfaz web simple o dashboard). (Opcional)

6.0.4. Requerimientos de interoperabilidad

4.1. El sistema debe permitir ser ejecutado en un entorno local o en una instancia cloud sin necesidad de modificar el código base. (Alta)

4.2. El sistema debe permitir guardar y reutilizar los resultados del análisis en distintos formatos estructurados (ej: CSV, JSON). (Media)

6.0.5. Requerimientos de testing y validación

5.2. Se debe validar la consistencia de las métricas extraídas frente a situaciones simuladas o valores esperados. (Alta)

5.1. Se deben realizar pruebas unitarias para validar la correcta ejecución de cada módulo del sistema. (Media)

6.0.6. Requerimientos regulatorios y éticos

6.1. El sistema no debe almacenar datos sensibles sin consentimiento explícito. (Alta)

6.2. Toda utilización de videos clínicos reales debe contar con autorización y resguardo ético correspondiente. (Alta)

Página 9 de 18

⸻

# 7. Historias de usuarios (Product backlog)

Las siguientes historias de usuario representan funcionalidades clave del sistema desde la perspectiva de los distintos interesados. Se asignaron story points a partir de la evaluación de complejidad técnica, dificultad de implementación e incertidumbre asociada.

1. Como profesional médico, quiero que el sistema procese automáticamente videos de los pacientes realizando ejercicios, para poder evaluar métricas objetivas de su desempeño.
    Story points: 8 (complejidad: 3, dificultad: 3, incertidumbre: 2)
2. Como desarrollador, quiero integrar un modelo de estimación de pose corporal para poder extraer coordenadas clave del cuerpo en cada cuadro del video.
    Story points: 6 (complejidad: 3, dificultad: 2, incertidumbre: 1)
3. Como neurólogo, quiero ver visualizaciones que representen la evolución del movimiento del paciente en distintos ejercicios, para identificar cambios sutiles.
    Story points: 7 (complejidad: 2, dificultad: 2, incertidumbre: 3)
4. Como usuario técnico, quiero que el sistema genere reportes exportables con las métricas calculadas, para poder hacer seguimiento longitudinal.
    Story points: 4 (complejidad: 1, dificultad: 2, incertidumbre: 1)
5. Como desarrollador, quiero que el sistema sea ejecutable localmente o en la nube para asegurar portabilidad y facilitar pruebas.
    Story points: 8 (complejidad: 3, dificultad: 3, incertidumbre: 2)
6. Como investigador, quiero contar con documentación clara del sistema para poder entender su arquitectura y facilitar futuras mejoras.
    Story points: 4 (complejidad: 2, dificultad: 1, incertidumbre: 1)
7. Como paciente, quiero acceder a un resumen visual de mis resultados para poder entender cómo evoluciona mi condición motora a lo largo del tiempo.
    Story points: 7 (complejidad: 2, dificultad: 2, incertidumbre: 3)

# 8. Entregables principales del proyecto

A continuación se enumeran los principales entregables que se generarán durante el desarrollo del proyecto:

* Sistema funcional para análisis automatizado de videos clínicos, con extracción de métricas motrices a partir de estimación de pose corporal.
* Módulo de visualización de resultados que permita interpretar la evolución de las métricas a lo largo del tiempo.
* Reportes generados automáticamente con los resultados del análisis en formato PDF o similar.
* Prototipo funcional de la infraestructura tecnológica propuesta desplegable localmente o en entorno cloud.
* Diseño de arquitectura modular escalable, documentada con diagramas y descripción técnica.
* Documentación técnica completa que incluya instrucciones de uso, dependencias y estructura del sistema.
* Memoria del Trabajo Final que contemple el marco conceptual, los resultados obtenidos y el análisis crítico del proceso.
* Presentación final para la defensa del proyecto.

# 9. Desglose del trabajo en tareas

En esta sección se detalla la estructura de desglose del trabajo en tareas del proyecto (WBS por su siglas en inglés). A la derecha de cada tarea se indica la estimación de horas necesarias para ejecutarla.

Página 10 de 18

⸻

1. Planificación y diseño del sistema

1.1. Relevamiento de requerimientos técnicos y funcionales (32 h)
1.2. Investigación de herramientas y bibliotecas disponibles (visión por computadora, modelos preentrenados) (32 h)
1.3. Diseño de la arquitectura general de la solución (40 h)
1.4. Diagramado del flujo de datos y módulos funcionales (24 h)

2. Adquisición y preparación de datos

2.1. Recolección de videos clínicos disponibles (32 h)
2.2. Limpieza, estabilización y preprocesamiento de videos (40 h)
2.3. Generación de anotaciones o segmentaciones si fueran necesarias (40 h)

3. Desarrollo del sistema de análisis gestual

3.1. Integración de modelo de estimación de pose corporal (40 h)
3.2. Desarrollo de módulo de extracción de métricas motoras (40 h)
3.3. Pruebas con videos reales y ajuste de parámetros (40 h)

4. Visualización y generación de reportes

4.1. Diseño e implementación del módulo de visualización (40 h)
4.2. Generación de reportes exportables (PDF, CSV) (24 h)

5. Diseño de infraestructura y PoC

5.1. Diseño de arquitectura de despliegue (local/cloud) (40 h)
5.2. Implementación de una PoC funcional en entorno de prueba (40 h)

6. Documentación y cierre académico

6.1. Documentación técnica del sistema (22 h)
6.2. Redacción de la memoria del trabajo final (40 h)
6.3. Iteraciones sobre la redacción de la memoria del trabajo final (20 h)
6.4. Preparación de la presentación para defensa (14 h)

Cantidad total de horas: 600 h

# 10. Diagrama de Activity On Node

El siguiente diagrama de Activity On Node (AoN) representa gráficamente la secuencia lógica entre las tareas definidas en el WBS, indicando las relaciones de precedencia y la estructura general del flujo de trabajo. Este tipo de diagrama permite visualizar el orden en que deben ejecutarse las actividades del proyecto, así como identificar caminos críticos y dependencias entre tareas.

El diseño del diagrama se realizó manteniendo una representación simplificada para facilitar su lectura. En el gráfico se incluyen las principales tareas agrupadas por fase, con flechas que indican la relación de dependencia entre ellas. Las flechas más gruesas representan el camino crítico. Las unidades de tiempo corresponden a horas de trabajo.

Figura 2. Diagrama de Activity On Node del proyecto

INICIO
  ├── Planificación y diseño del sistema
  │     t = 128
  │
  └── Adquisición y preparación de datos
        t = 112
Planificación y diseño del sistema
  ↓
Desarrollo del sistema de análisis gestual
t = 120
Adquisición y preparación de datos
  ↓
Desarrollo del sistema de análisis gestual
t = 120
Desarrollo del sistema de análisis gestual
  ├── Visualización y reportes
  │     t = 64
  │
  └── Diseño de infraestructura y PoC
        t = 80
Visualización y reportes
  ↓
Documentación y cierre académico
t = 96
Diseño de infraestructura y PoC
  ↓
Documentación y cierre académico
t = 96
Documentación y cierre académico
  ↓
FIN

Camino crítico: 464 horas
Total del proyecto: 600 horas

Página 12 de 18

⸻

# 11. Diagrama de Gantt

El cronograma del proyecto se representa mediante un diagrama de Gantt, que detalla la distribución temporal de las tareas principales organizadas según el WBS. En este diagrama se especifican las fechas estimadas de inicio y finalización de cada grupo de tareas, permitiendo visualizar la duración total del proyecto, solapamientos posibles y dependencias generales.

El proyecto se desarrollará entre julio de 2025 y abril de 2026, abarcando una duración estimada de nueve meses. A continuación, se presenta el cronograma.

Figura 3. Diagrama de Gantt del proyecto

Nombre	Begin date	End date
Relevamiento de requerimientos técnicos y funcionales	24/6/25	14/7/25
Investigación de herramientas y bibliotecas disponibles	15/7/25	04/8/25
Recolección de videos clínicos disponibles	15/7/25	04/8/25
Diseño de la arquitectura general de la solución	05/8/25	25/8/25
Limpieza, estabilización y preprocesamiento de videos	27/8/25	03/9/25
Diagramado del flujo de datos y módulos funcionales	26/8/25	03/9/25
Generación de anotaciones o segmentaciones	04/9/25	23/9/25
Integración de modelo de estimación de pose corporal	24/9/25	23/10/25
Desarrollo de módulo de extracción de métricas motoras	24/10/25	20/11/25
Pruebas con videos reales y ajuste de parámetros	21/11/25	18/12/25
Diseño e implementación del módulo de visualización	16/1/26	13/2/26
Generación de reportes exportables	02/01/26	15/01/26
Redacción de la memoria del trabajo final	13/01/26	09/03/26
Diseño de arquitectura de despliegue	19/12/25	13/02/26
Implementación de una PoC funcional	16/02/26	16/03/26
Iteraciones sobre la redacción de la memoria	10/03/26	30/03/26
Documentación técnica del sistema	17/03/26	30/03/26
Preparación de la presentación para defensa	31/03/26	02/04/26

Página 13 de 18

⸻

# 12. Presupuesto detallado del proyecto

El presupuesto del proyecto se calcula en base a una estimación total de 600 horas de trabajo técnico y contempla también algunos costos indirectos asociados a servicios complementarios.

El valor destinado a las horas de desarrollo es de USD 14.500, lo que equivale a un valor horario aproximado de USD 24.17.

En las siguientes tablas se detallan costos directos e indirectos del proyecto.

Costos directos

Descripción	Cantidad	Valor unitario (USD)	Valor total (USD)
Horas de desarrollo y diseño	600 h	24.17	14,500
Subtotal			14,500

Costos indirectos

Es importante aclarar que los valores detallados a continuación como costos indirectos corresponden a estimaciones conservadoras, pensadas para cubrir posibles contingencias que pudieran surgir durante el desarrollo del proyecto.

En particular, el uso de procesamiento y almacenamiento en la nube suele estar basado en un modelo de cobro por consumo, por lo que no se trata de una suscripción fija, sino de una estimación aproximada del gasto esperado en función del uso proyectado.

Descripción	Cantidad	Valor unitario (USD)	Valor total (USD)
Procesamiento y recursos en la nube	Estimación en base al uso	300	300
Herramientas de edición y documentación	1 licencia parcial	100	100
Gastos de conexión remota y soporte técnico	1 estimación	100	100
Subtotal			500

TOTAL GENERAL: USD 15.000

Nota: Los valores están expresados en dólares estadounidenses (USD) al tipo de cambio de referencia de julio de 2025, 1 USD = 1,325 ARS.

# 13. Gestión de riesgos

La gestión de riesgos busca anticipar posibles eventos que puedan afectar negativamente el desarrollo del proyecto. A continuación se identifican los principales riesgos, junto con su severidad (S), ocurrencia (O) y plan de mitigación cuando corresponde.

Página 14 de 18

⸻

a) Identificación y análisis de riesgos

Riesgo 1: Dificultades técnicas en la integración de modelos de visión por computadora.

Severidad (S): 8 — Este componente es clave para el funcionamiento del sistema. Un error crítico podría afectar el resultado global.

Ocurrencia (O): 6 — La integración con modelos preentrenados puede presentar incompatibilidades o problemas de rendimiento.

Riesgo 2: Insuficiencia en la calidad de los videos clínicos disponibles.

Severidad (S): 7 — Las métricas dependen fuertemente de la calidad de los datos de entrada.

Ocurrencia (O): 5 — Aunque hay ejemplos disponibles, no está garantizada su calidad ni cantidad.

Riesgo 3: Dificultades técnicas en el despliegue del sistema en la nube.

Severidad (S): 6 — Podría limitar la entrega del PoC funcional y la portabilidad del sistema.

Ocurrencia (O): 5 — Requiere conocimientos de infraestructura y configuración que pueden presentar errores o demoras.

Riesgo 4: Sobrecostos en el uso de servicios en la nube.

Severidad (S): 4 — Puede afectar la viabilidad operativa pero no impide continuar el desarrollo.

Ocurrencia (O): 5 — Si no se controlan los recursos, el gasto podría exceder lo planificado.

Riesgo 5: Imposibilidad de validación clínica con profesionales médicos.

Severidad (S): 6 — Limitaría la evaluación externa de la herramienta.

Ocurrencia (O): 4 — Depende de disponibilidad de terceros, fuera del control directo.

b) Tabla de evaluación de riesgos

Riesgo	S	O	RPN	S*	O*	RPN*
1. Técnicos en CV	8	6	48	6	4	24
2. Calidad de datos	7	5	35	5	4	20
3. Técnico en el despliegue	6	5	30	4	3	12
4. Costos en la nube	4	5	20	-	-	-
5. Validación médica	6	4	24	-	-	-

Cuadro 3. Evaluación y mitigación de riesgos. RPN = S × O

Se adopta como criterio que todo riesgo con RPN > 25 debe ser mitigado activamente.

c) Plan de mitigación

Riesgo 1: Dificultades técnicas en visión por computadora

Mitigación: Seleccionar desde el inicio modelos bien documentados y ampliamente usados. Probar su integración en etapas tempranas.

S = 6, O = 4** — Reducción esperada tras mitigación.

Página 15 de 18

⸻

Riesgo 2: Calidad de videos insuficiente

Mitigación: Evaluar la calidad de los videos disponibles al comienzo del proyecto. Si es necesario, realizar grabaciones adicionales o adaptar el pipeline a baja resolución.

S = 5, O = 4**

Riesgo 3: Dificultades en el despliegue del sistema en la nube

Mitigación: Empezar con despliegues mínimos viables (PoC) en entornos conocidos como Google Colab o máquinas virtuales estándar. Usar plantillas de infraestructura (IaC) y priorizar soluciones documentadas.

S = 4, O = 3**

# 14. Gestión de la calidad

En esta sección se describen los mecanismos de verificación y validación que se aplicarán sobre los principales requerimientos del proyecto. Se busca garantizar que los entregables cumplan tanto con las especificaciones técnicas como con las expectativas del usuario final.

Req 1: El sistema debe permitir la carga y procesamiento de videos clínicos.

* Verificación: Prueba funcional con distintos formatos de video. Revisión del log de procesamiento.
* Validación: Revisión junto al usuario médico de la experiencia de carga y tiempos de respuesta.

Req 2: El sistema debe aplicar modelos de estimación de pose corporal.

* Verificación: Comparación visual entre las poses detectadas y el video original.
* Validación: Confirmación del profesional de que los puntos clave se corresponden con las articulaciones relevantes.

Req 3: El sistema debe calcular métricas como amplitud y frecuencia.

* Verificación: Revisión de cálculos sobre videos sintéticos o controlados con valores conocidos.
* Validación: Evaluación por parte del usuario experto sobre la coherencia de las métricas obtenidas.

Req 4: El sistema debe generar visualizaciones interpretables.

* Verificación: Revisión de gráficos generados con distintos perfiles de movimiento.
* Validación: Entrevista con médico clínico para evaluar claridad.

Req 5: El sistema debe exportar reportes en formato PDF.

* Verificación: Prueba automatizada de generación de archivos y revisión del contenido.
* Validación: Entrega de reportes a un usuario final para confirmar legibilidad y utilidad del PDF.

Req 6: El sistema debe funcionar en entorno local o en la nube.

* Verificación: Pruebas de despliegue en ambas plataformas.
* Validación: Evaluación en entorno de uso simulado por parte del usuario técnico.

Página 16 de 18

⸻

Req 7: El sistema debe permitir guardar resultados en formato CSV.

* Verificación: Revisión de la estructura del archivo exportado.
* Validación: Confirmación de que el archivo CSV puede ser utilizado para análisis posterior.

Req 8: La herramienta debe tener documentación técnica clara.

* Verificación: Revisión interna del manual técnico y ejecución de pruebas siguiendo sus pasos.
* Validación: Revisión externa por parte de un colega técnico no involucrado en el desarrollo.

Req 9: La memoria del proyecto debe estar correctamente redactada.

* Verificación: Revisión formal del texto siguiendo las pautas de FIUBA.
* Validación: Devolución del director y evaluación positiva en la entrega previa a defensa.

Req 10: El sistema no debe almacenar datos sensibles sin consentimiento.

* Verificación: Revisión del código para garantizar anonimización y control de acceso.
* Validación: Revisión ética externa o consentimiento informado explícito cuando corresponda.

# 15. Procesos de cierre

Para el cierre del proyecto se establecerán las siguientes actividades, con el fin de garantizar una evaluación completa, un cierre ordenado y el reconocimiento de los actores involucrados.

Evaluación del cumplimiento del plan

Se llevará a cabo una reunión final con el director del proyecto para evaluar si se respetaron los plazos, entregables y criterios establecidos en el Plan de Proyecto original.

* Responsable: Esp. Ing. Alex D. Barria C.
* Procedimiento: Revisión de las tareas completadas, comparación contra el cronograma propuesto, análisis de desvíos y justificación de cambios si los hubiera.

Registro de lecciones aprendidas

Se identificarán técnicas, herramientas o decisiones que hayan sido especialmente útiles o problemáticas durante el desarrollo.

* Responsable: Esp. Ing. Alex D. Barria C.
* Procedimiento: Redacción de un anexo a la memoria final donde se documenten los aciertos, obstáculos y recomendaciones para proyectos similares en el futuro.

Página 17 de 18

⸻

Reconocimiento a los interesados

Se realizará un acto de cierre informal para agradecer la participación de todos los actores que colaboraron con el proyecto, especialmente el director, posibles profesionales médicos consultados y revisores técnicos.

* Responsable: Esp. Ing. Alex D. Barria C.
* Financiamiento: Sin presupuesto adicional previsto. En caso de ser necesario, se asumirán gastos personales mínimos para material de agradecimiento simbólico.

Página 18 de 18