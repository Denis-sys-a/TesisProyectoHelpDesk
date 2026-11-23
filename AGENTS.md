# AGENTS.md

## Project

LaTeX thesis (SENATI "Proyecto de Innovación") in Spanish, APA 7. Title: "Sistema Web Help-Desk Centralizado para la Gestión del Servicio de Soporte Técnico y Control de Inventario de Activos TI en J&P Periféricos S.A.C." Authors: Jack Daniel Leandro Hernández, Giovanni Denis Jara Hilario, Alvaro Jesus Solis Rivadeneyra; advisor Mg. Jose Armando Tiznado Ubillus.

No application code in this repo — only the thesis document. Build artifacts live in `build/` (gitignored).

## Build

- Engine: MiKTeX `pdflatex` via `latexmk` (on PATH).
- From repo root:
  - `latexmk -pdf -output-directory=build main.tex` — incremental (exit 0 = success).
  - `latexmk -g -pdf -output-directory=build main.tex` — force full rebuild.
  - `latexmk -C -output-directory=build` — clean generated files.
- Output: `build/main.pdf` (entrypoint `main.tex`).
- After building, inspect `build/main.log` for `!` errors and unresolved refs/citations.
- A successful build still prints a MiKTeX "major issue: ... not checked for MiKTeX updates" notice to stderr; not a failure (exit 0).
- Known pre-existing warning: `Citation '91'` undefined (3 hits in `Estructura/capitulo6.tex` ~lines 140/179/189). References are hand-written in `Estructura/referencias.tex` (no BibTeX/`.bib`); `\cite` keys must match entries added manually.

## Structure

- `main.tex` — preamble + `\input{Estructura/...}` sequence. Add/reorder a section => edit this list too.
- `Estructura/*.tex` — one file per part: `caratula`, `agradecimiento`, `dedicatoria`, `resumen`, `introduccion`, `capitulo1`..`capitulo6`, `referencias`, `anexos`.
- `img/` — figures referenced as `img/<name>.png` (also `\graphicspath{{img/}}`).
- `docs/antecedentes/` — Markdown traceability files for approved antecedents (`YYYY-apellido-clave.md`).

## Conventions / gotchas

- All `.tex` are UTF-8; `main.tex` uses `\usepackage[utf8]{inputenc}`. Do not re-encode or strip accents.
- `\chapter` titles are passed twice: `\chapter[CAPÍTULO I]{...}` (short form drives TOC/running head).
- Figures use global APA 7 caption format (`\captionsetup` in preamble); sometimes overridden with `\captionsetup{justification=centering}`.
- `\counterwithout{figure/table}{chapter}` => continuous numbering across the whole document.
- `build/` is gitignored generated output — never edit files there; rebuild instead.
- Branches: `main`, `alvaro`, `giovanni`, `leandro` (current). Thesis is co-authored across branches; merge carefully, conflicts usually in chapter `.tex`.

## Flujo de Aprobación y Trazabilidad de Antecedentes

Cuando se proponga o agregue un antecedente a la tesina:
1. **Propuesta y aprobación obligatoria (antes de editar `.tex`):**
   - Explica explícitamente **por qué conviene implementar ese antecedente** (cómo aporta datos estadísticos reales y cómo se vincula con las variables: Gestión del Servicio de Soporte Técnico Help-Desk y Control de Inventario de Activos TI).
   - Detente y espera mi aprobación explícita ("Aprobado") antes de escribir en los archivos `.tex` o crear archivos.
2. **Al recibir aprobación:**
   - Crea un archivo Markdown individual en `docs/antecedentes/` con el formato `YYYY-apellido-clave.md` (ejemplo: `2024-quispe-helpdesk.md`).
   - El archivo `.md` debe incluir obligatoriamente:
     - **URL de consulta:** enlace directo y verificable de la fuente.
     - **Ámbito:** Nacional o Internacional.
     - **Autor(es) y año:**
     - **Título:**
     - **Institución / Repositorio:**
     - **Justificación de inclusión:** por qué se implementó en la tesina.
     - **Metodología y muestra:**
     - **Resultados estadísticos clave:** (porcentajes, métricas pre-test/post-test, tiempos de atención, exactitud de inventario).
     - **Texto integrado en LaTeX:** bloque exacto añadido al `.tex`.
   - Integra el antecedente en el archivo `.tex` correspondiente manteniendo los comandos y estilo del repositorio (`Estructura/*.tex` y entradas manuales en `Estructura/referencias.tex` si aplica).
3. **Regla anti-alucinación:** Nunca inventes autores, títulos, URLs ni cifras estadísticas. Si falta algún dato, márcalo como `[PENDIENTE]`.

## Verification

- Build command above; success = exit 0 and no `!` in `build/main.log`. Unresolved citations print "Latexmk: Summary of warnings" but still exit 0.