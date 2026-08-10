# Changelog — MundiPets (ISR401-PFC-ERS-EQUIPO-E)

Todos los cambios relevantes del ERS y de los artefactos de la PE4 se documentan en este archivo.
Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/).

## [1.1] - 2026-08-09

Versión resultante de la Práctica Experimental 4 (Unidad IV). Incorpora las correcciones derivadas
de la inspección Fagan aplicada a la Sección 3 del ERS y las tres solicitudes de cambio aprobadas
por el Change Control Board. Línea base establecida mediante el tag anotado `baseline-v1.1`.

### Corregido

- **RF-06** — Evaluar compatibilidad entre mascotas para cruza: el criterio de verificación ahora
  exige comprobar los siete factores declarados en la descripción (raza, edad, salud, antecedentes
  genéticos, parentesco, comportamiento, historial médico), no solo el resultado comparativo. (D-04)
- **RF-07** — Sistema de mensajería: se incorpora el reporte manual de mensajes o interacciones
  inadecuadas, y se documenta la moderación automática previa al envío conforme a RNF-15. (D-05, D-06;
  RFC-01)
- **RF-09 / RD-03** — Validación de información médica: se aclara que la veterinaria realiza una
  validación *referencial*, sin que constituya certificación clínica. (D-02)
- **RF-12** — Verificación de identidad: se sustituye «información/documentación requerida» por un
  mecanismo cerrado (datos básicos + documento nacional de identidad legible). (D-03)
- **RF-17** — Validación de imágenes: se enumeran los criterios de rechazo (contenido inapropiado,
  imagen borrosa, tipo de fotografía incorrecto) en lugar de «criterios establecidos». (D-08)
- **RF-24** — Trazabilidad de vacunación: se incorpora el número de lote en descripción, entradas y
  criterio de verificación, que antes solo aparecía en el título del requisito. (D-09)
- **RF-25 / RNF-16** — Aviso de mascota extraviada: los datos de contacto directo permanecen ocultos
  por defecto y la ubicación se limita a zona aproximada (radio ≥ 1 km), resolviendo la contradicción
  con RNF-16. (D-10, D-11; RFC-03)
- **RD-01** — Se añade el tercer subcomponente de IA (moderación de mensajes) que el ERS ya
  implicaba pero no declaraba junto a compatibilidad y validación de imágenes. (D-07)
- **RNF-03** — Tiempo de respuesta: se declara la infraestructura y herramienta de prueba (k6 sobre
  staging 2 vCPU/4 GB) con la que se mide el P95. (D-21; RFC-02, umbral ajustado a 3 s)
- **RNF-06** — Exactitud del componente de IA: se fija el tamaño y la estratificación del conjunto de
  prueba (≥ 100 casos) y se aclara que el conjunto evaluado está documentado por veterinarios
  colaboradores. (D-16, D-22)
- **RNF-07** — Precisión en validación de imágenes: se enumeran los tipos de imagen válidos e
  inválidos. (D-17)
- **RNF-11** — Portabilidad: se fijan versiones concretas de navegador y resoluciones de referencia
  (360×640 y 1366×768 px). (D-18)
- **RNF-12** — Escalabilidad: se sustituye «degradación significativa» por un umbral cuantitativo
  (P95 no debe aumentar más del 50 % respecto de RNF-03). (D-23)
- **RNF-13 / RNF-14** — Explicabilidad: se exige verificar en la matriz que la evidencia, la medición
  de tiempo y la encuesta de comprensión estén enlazadas explícitamente al requisito. (D-19, D-20)
- **Visión general (Sección 1.5)** — Corregida la cifra de requisitos no funcionales de 15 a 16,
  coherente con RNF-01 a RNF-16. (D-01)
- **Matriz de trazabilidad (Apéndice D)** — Corregidos cuatro enlaces semánticamente incorrectos:
  - TR-10 (RF-10 → CU-12): enlace eliminado, sin CU específico en esta versión. (D-12)
  - TR-11 (RF-11 → CU-06): corregido a CU-12 (Configurar privacidad médica). (D-13)
  - TR-33 (RF-20 → CU-08): enlace eliminado, sin CU específico en esta versión. (D-14)
  - TR-38 (RF-25 → CU-04): enlace eliminado, sin CU específico en esta versión. (D-15)

### Añadido

- Fila de versión 1.1 en el historial de revisiones del ERS.
- Anexo B (`02_Inspeccion/AnexoB_registro_defectos.xlsx`) ampliado de 15 a 23 defectos, con hoja de
  métricas calculadas por fórmula (densidad, distribución por tipo/severidad, tasa de detección,
  esfuerzo total).
- Tablero CASE en Jira (espacio `PE4_Fuertes_Contreras_Viteri`, 5 Epics, 25 Stories, 10 Sub-tasks) y
  su exportación en `04_Trazabilidad/backlog_export.csv` / `.xlsx`.
- Tag anotado `baseline-v1.1` como línea base formal del documento.

### Referencias

- Registro consolidado de defectos: `02_Inspeccion/AnexoB_registro_defectos.xlsx`
- RFC-01, RFC-02, RFC-03 y acta del CCB: `03_CCB/`
- Informe PE4 completo: `05_Informe/PE4_U4_FUERTES_CONTRERAS_VITERI.pdf`

---

## [1.0 / Entrega 2A] - 2026-07-29

Versión base sobre la que se ejecutó la inspección Fagan de la PE4. Corresponde a la Entrega 3
(2A) del ERS: especificación completa con 25 RF, 16 RNF y 9 RD, requisitos legales (LOPDP),
explicabilidad del componente de IA, historias de usuario con criterios de aceptación, modelado UML
completo, priorización Kano/WSJF y matriz de trazabilidad de 50 elementos.

### Añadido

- Especificación completa de requisitos funcionales, no funcionales y restricciones de diseño.
- Ocho diagramas UML y componente empírico de validación.
- Matriz de trazabilidad extendida (Ley, Objetivo, Stakeholder, Evidencia, RF/RNF/RD, CU, HU, CA,
  Mockup).

---

## [2.0 / Entrega 1B] - 2026-07-05

ERS/SRS parcial. Incorpora correcciones de la Entrega 1A y agrega requisitos, modelado UML inicial,
priorización y trazabilidad preliminar.

---

## [1.0 / Entrega 1A] - 2026-05-30

Versión inicial del documento: planificación del proyecto MundiPets y elicitación de requisitos.
