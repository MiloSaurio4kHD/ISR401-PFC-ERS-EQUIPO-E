# ISR401-PFC-ERS-EQUIPO-E

Repositorio de la Práctica Experimental 4 (PE4), Unidad IV, de la asignatura
Ingeniería de Requerimientos (ISR-401), Carrera de Software, UTEQ. Periodo 2026-2027 PPA.

## Sistema

**MundiPets** — sistema del Proyecto Fin de Curso del equipo.

## Integrantes

| Integrante | Rol en la inspección | Rol en el CCB |
|---|---|---|
| Fuertes Arraes Edson Daniel | Moderador | Presidente |
| Contreras Chávez Kevin Germán | Lector | Analista |
| Viteri García Jonathan Enrique | Inspector 1 | Representante del cliente |

## Estructura del repositorio

```
01_ERS/           ERS_v1.0.pdf, ERS_v1.1.pdf y fuentes .tex
02_Inspeccion/    AnexoA_checklists/, AnexoB_registro_defectos.xlsx
03_CCB/           RFC-01.pdf, RFC-02.pdf, RFC-03.pdf, Acta_CCB-01.pdf
04_Trazabilidad/  matriz_trazabilidad.xlsx, backlog_export.csv, capturas/
05_Informe/       PE4_U4_FUERTES_CONTRERAS_VITERI.tex, referencias.bib, figuras/
06_Evidencias/    capturas_git/, fotos_sesion/
CHANGELOG.md      Historial de versiones del ERS por RFC aprobada
```

## Compilación del informe

**Archivo principal:** `05_Informe/PE4_U4_FUERTES_CONTRERAS_VITERI.tex`

**Dependencias:**
- Distribución LaTeX completa (TeX Live 2023+ o MiKTeX)
- Motor: `pdflatex`
- Bibliografía: `biber` (backend de biblatex, estilo IEEE)
- Paquetes: IEEEtran, babel (spanish), csquotes, biblatex, booktabs, tabularx,
  longtable, graphicx, geometry, fancyhdr, enumitem, titlesec, hyperref
- Archivos requeridos en la misma carpeta: `referencias.bib`, `figuras/`

**Orden de comandos:**

```bash
cd 05_Informe
pdflatex PE4_U4_FUERTES_CONTRERAS_VITERI.tex
biber    PE4_U4_FUERTES_CONTRERAS_VITERI
pdflatex PE4_U4_FUERTES_CONTRERAS_VITERI.tex
pdflatex PE4_U4_FUERTES_CONTRERAS_VITERI.tex
```

Salida: `05_Informe/PE4_U4_FUERTES_CONTRERAS_VITERI.pdf`

> Nota: `biber` recibe el nombre del archivo **sin extensión**.

El ERS (`01_ERS/ERS_v1.1.tex`) se compila con el mismo procedimiento, ejecutado dentro de
`01_ERS/`.

## Línea base

Versión vigente del ERS: **v1.1** — tag `baseline-v1.1`
