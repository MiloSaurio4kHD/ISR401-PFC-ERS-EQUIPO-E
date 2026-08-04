@"

\# ISR401-PFC-ERS-EQUIPO-E



Repositorio de la Practica Experimental 4 (PE4), Unidad IV, de la asignatura

Ingenieria de Requerimientos (ISR-401), Carrera de Software, UTEQ. Periodo 2026-2027 PPA.



\## Sistema



\*\*MundiPets\*\* - sistema del Proyecto Fin de Curso del equipo.



\## Integrantes



| Integrante | Rol en la inspeccion | Rol en el CCB |

|---|---|---|

| Fuertes Arraes Edson Daniel | Moderador | Presidente |

| Contreras Chavez Kevin German | Lector | Analista |

| Viteri Garcia Jonathan Enrique | Inspector 1 | Representante del cliente |



\## Estructura del repositorio



\\`\\`\\`

01\_ERS/           ERS\_v1.0.pdf, ERS\_v1.1.pdf y fuentes .tex

02\_Inspeccion/    AnexoA\_checklists/, AnexoB\_registro\_defectos.xlsx, metricas.xlsx

03\_CCB/           RFC-01.pdf, RFC-02.pdf, RFC-03.pdf, Acta\_CCB.pdf

04\_Trazabilidad/  matriz\_trazabilidad.xlsx, backlog\_export.csv, capturas/

05\_Informe/       PE4\_U4\_FUERTES\_CONTRERAS.tex, referencias.bib, figuras/

06\_Evidencias/    capturas\_git/, fotos\_sesion/, declaracion\_IA.pdf

CHANGELOG.md      Historial de versiones del ERS por RFC aprobada

\\`\\`\\`



\## Compilacion del informe



\*\*Archivo principal:\*\* \\`05\_Informe/PE4\_U4\_FUERTES\_CONTRERAS.tex\\`



\*\*Dependencias:\*\*

\- Distribucion LaTeX completa (TeX Live 2023+ o MiKTeX)

\- Motor: \\`pdflatex\\`

\- Bibliografia: \\`biber\\` (backend de biblatex, estilo IEEE)

\- Paquetes: IEEEtran, babel (spanish), csquotes, biblatex, booktabs, tabularx,

&#x20; longtable, graphicx, geometry, fancyhdr, enumitem, titlesec, mdframed, hyperref

\- Archivos requeridos en la misma carpeta: \\`referencias.bib\\`, \\`logo\_uteq.png\\`, \\`figuras/\\`



\*\*Orden de comandos:\*\*



\\`\\`\\`bash

cd 05\_Informe

pdflatex PE4\_U4\_FUERTES\_CONTRERAS.tex

biber    PE4\_U4\_FUERTES\_CONTRERAS

pdflatex PE4\_U4\_FUERTES\_CONTRERAS.tex

pdflatex PE4\_U4\_FUERTES\_CONTRERAS.tex

\\`\\`\\`



Salida: \\`05\_Informe/PE4\_U4\_FUERTES\_CONTRERAS.pdf\\`



> Nota: \\`biber\\` recibe el nombre del archivo \*\*sin extension\*\*.



\## Linea base



Version vigente del ERS: \*\*v1.1\*\* - tag \\`baseline-v1.1\\`

"@ | Set-Content -Encoding UTF8 "README.md"

