# Checklist de escritura para la memoria

Verificar cada punto antes de finalizar la redaccion de una seccion.

## Estructura

- [ ] La seccion corresponde al capitulo correcto segun `docs/lineamientos-memoria/estructura-memoria.md`.
- [ ] El capitulo tiene parrafo introductorio (2-3 lineas) sin titulo propio.
- [ ] No se crearon subsecciones innecesarias tituladas "Introduccion".
- [ ] La extension esta dentro del rango esperado para el capitulo.
- [ ] El contenido no invade temas de otros capitulos (ej: requerimientos fuera de Cap. 3).

## Redaccion

- [ ] Redaccion impersonal y en pasado.
- [ ] Sin primera persona ("yo", "diseñe", "implementé").
- [ ] Sin conectores genericos repetitivos.
- [ ] Sin gerundios encadenados.
- [ ] Oraciones claras y no excesivamente largas.
- [ ] Transiciones especificas entre parrafos (consecuencia, comparacion, limitacion).

## Formato

- [ ] Sin negritas dentro de parrafos.
- [ ] Sin subrayados dentro de parrafos.
- [ ] Italicas solo para siglas/terminos en otro idioma, con explicacion la primera vez.
- [ ] `\texttt{}` para funciones, bibliotecas, archivos, directorios, variables.
- [ ] Consistencia en uso de terminos (no alternar ingles/español para el mismo concepto).
- [ ] Cifras en formato consistente (letras o numeros, pero uniforme).

## Figuras

- [ ] Cada figura tiene introduccion previa en el texto.
- [ ] Cada figura se referencia con `\ref{fig:xxx}`.
- [ ] Cada figura tiene analisis posterior (que se observa, por que es relevante).
- [ ] Texto interno de figuras es legible.
- [ ] Epigrafe en español.
- [ ] Fuente indicada si es de terceros.

## Tablas

- [ ] Cada tabla tiene introduccion previa.
- [ ] Cada tabla tiene analisis de datos relevantes posterior.
- [ ] Construida en LaTeX (no como imagen).
- [ ] Formato consistente con el resto del documento.
- [ ] Encabezados claros y descriptivos.

## Referencias

- [ ] Formato numerico con `\citep{}`.
- [ ] Distribuidas a lo largo del texto, no agrupadas al final.
- [ ] Toda afirmacion tecnica o comparativa tiene referencia.
- [ ] No hay URLs sueltas sin formato bibliografico.
- [ ] Las claves de citacion existen en el archivo `.bib` o se indico al usuario que debe agregarlas.

## Ecuaciones

- [ ] Formato formal y numeradas cuando corresponda.
- [ ] Referenciadas desde el texto.
- [ ] Variables y terminos explicados.

## Codigo

- [ ] No se incluyeron bloques de codigo extensos.
- [ ] Si se incluyo codigo, usa `lstlisting` con formato de la plantilla.
- [ ] Se prefirieron diagramas (flujo, estado, secuencia, UML) sobre codigo.

## Contenido tecnico

- [ ] Los datos tecnicos provienen del codigo fuente real (no inventados).
- [ ] Las metricas y resultados provienen de ejecuciones reales o de los documentos del proyecto.
- [ ] No se inventaron referencias bibliograficas.
