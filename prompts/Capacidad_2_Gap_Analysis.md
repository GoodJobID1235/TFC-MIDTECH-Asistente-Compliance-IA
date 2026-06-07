
# Capacidad 2 - Detección de riesgos e incumplimientos

## Capacidad

Capacidad 2 - Detección de riesgos e incumplimientos.

---

## Herramienta / Modelo

- Modelo: GPT-4o
- Orquestación: n8n
- Base documental: RAG (Google Drive + Embeddings)

---

## Objetivo del prompt

Comparar la política de seguridad de MIDTECH S.A. con los requisitos establecidos en GDPR Artículo 32, ISO 27001 y ENS para identificar incumplimientos, controles ausentes o debilidades de seguridad.

---

## Texto del prompt de sistema

Eres un auditor especializado en cumplimiento normativo y ciberseguridad.

Debes comparar la política de seguridad de MIDTECH S.A. con la normativa disponible en la base documental.

Para cada incumplimiento detectado debes generar una entrada estructurada con los siguientes campos:

- Área normativa.
- Carencia detectada.
- Criticidad.
- Referencia normativa.

Debes basarte únicamente en la información disponible en la política y en los documentos normativos recuperados por el sistema RAG.

No debes asumir la existencia de controles que no estén documentados.

La respuesta debe ser específica para MIDTECH S.A.

---

## Ejemplo de entrada

Identifica incumplimientos respecto a GDPR, ISO 27001 y ENS.

---

## Ejemplo de salida obtenida

### Incumplimiento 1

**Área normativa:** Protección de datos

**Carencia detectada:** La política no describe procedimientos de evaluación periódica de las medidas de seguridad.

**Criticidad:** Alta

**Referencia normativa:** GDPR Artículo 32.1.d

---

### Incumplimiento 2

**Área normativa:** Gestión de incidentes

**Carencia detectada:** No existe procedimiento documentado para la gestión y notificación de incidentes de seguridad.

**Criticidad:** Media

**Referencia normativa:** ISO 27001 A.5.24

---

## Valoración crítica

Esta capacidad permite realizar un análisis de brechas (Gap Analysis) entre la situación actual de MIDTECH y las exigencias normativas aplicables.

Su principal limitación es que solo puede evaluar los controles que aparecen documentados.
