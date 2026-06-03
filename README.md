# CodeDump

Consolida cualquier repositorio en un solo archivo descargable, directamente en el navegador.

## Que hace

CodeDump toma un repositorio de GitHub o un archivo ZIP local y fusiona todos los archivos seleccionados en un unico `.txt` o `.md`. Util para pasarle codebases a LLMs, revisar codigo offline o archivar proyectos.

## Caracteristicas

**Dos fuentes de entrada:**
- Repositorios de GitHub (publicos sin autenticacion, privados con Personal Access Token)
- Archivos `.zip` locales, extraidos completamente en el navegador con JSZip

**Arbol de archivos interactivo:**
- Checkbox por archivo y carpeta con seleccion en cascada
- Estado indeterminado en carpetas parcialmente seleccionadas
- Filtro por extension en tiempo real (ej: `.js, .ts, .jsx`)
- Exclusion por patrones glob (ej: `node_modules, *.test.js, dist`)

**Opciones de formato:**
- Header personalizable antes de cada archivo (`{filename}`, `{filepath}`, `{extension}`)
- Eliminar lineas en blanco
- Eliminar comentarios (`//`, `#`, `/* */`, `<!-- -->`) segun el tipo de archivo
- Eliminar indentacion
- Consolidar todos los saltos de linea en una sola linea

**Salida:**
- `.txt` texto plano
- `.md` con bloques de codigo y lenguaje inferido por archivo

Todo corre del lado del cliente. Sin backend, sin que ningun dato salga del navegador.

## Uso

Abri `index.html` en cualquier navegador moderno. Sin pasos de build.

## Stack

- React 18 (via CDN, sin build)
- JSZip para extraccion de ZIPs
- Vanilla JS para la generacion y descarga del archivo
