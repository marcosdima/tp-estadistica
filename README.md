# Trabajo Práctico de Estadística

Documento LaTeX del trabajo práctico. Estructura modular: el preámbulo,
las secciones, las tablas y los gráficos viven en carpetas separadas.

## Compilar

Desde la raíz del proyecto:

```bash
latexmk -pdf -outdir=build main.tex
```

El PDF se genera en `build/main.pdf`. Para limpiar los archivos auxiliares:

```bash
latexmk -C -outdir=build
```

> No hace falta instalar nada: se usa solo TeX Live (pgfplots, tikz,
> pgf-pie, booktabs, longtable, seqsplit, tcolorbox, etc.).

## Estructura

```
main.tex              Documento principal (solo estructura).
preamble/             Preámbulo modularizado.
  packages.tex          Carga de paquetes (xcolor se carga aquí una vez).
  geometry.tex          Márgenes y tamaño de papel.
  fonts.tex             Tipografía.
  colors.tex            Paleta de color única (gráficos y tablas).
  tables.tex            Entorno DatosTabla (longtable + booktabs).
  graphics.tex          Estilos globales de TikZ/pgfplots.
  commands.tex          Comandos y formato de secciones.
  hyperref.tex          Hipervínculos (siempre al final).
sections/             Una sección por archivo, numeradas (orden explícito).
tables/               Tablas de datos (nombres consistentes).
figures/              Gráficos como código pgfplots/TikZ (no imágenes).
docs/                 PDFs de referencia (original y corregido por la profesora).
build/                Salida de compilación (ignorada por git).
```

## Notas

- Los gráficos son **vectoriales** (pgfplots/TikZ), no imágenes planas.
- El contenido (datos, tablas, fórmulas) es idéntico al validado por la
  profesora; este rework solo reorganiza la estructura y moderniza los
  gráficos.
- Las correcciones manuscritas de la profesora (PDF en `docs/`) quedan
  para una etapa posterior.
