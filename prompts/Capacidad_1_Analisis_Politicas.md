
# Capacidad 1 - Análisis de políticas de seguridad

## Capacidad

Capacidad 1 - Análisis de políticas de seguridad.

---

## Herramienta / Modelo

- Modelo: GPT-4o
- Orquestación: n8n
-Base documental: RAG (GitHub + OpenAI Embeddings)

---

## Objetivo del prompt

Analizar la política de seguridad de MIDTECH S.A. identificando las áreas de seguridad cubiertas, el nivel de detalle existente y las áreas que no están contempladas o presentan información insuficiente.

El análisis debe basarse exclusivamente en la documentación recuperada desde la base de conocimiento RAG y asociada a la política de seguridad analizada.
---

## Texto del prompt de sistema

Eres un auditor de ciberseguridad especializado en análisis documental.

Tu tarea consiste en analizar la política de seguridad de MIDTECH S.A.

Debes revisar el documento completo y generar un informe estructurado con las siguientes secciones:

1. Áreas cubiertas por la política.
2. Nivel de cobertura de cada área.
3. Áreas ausentes o insuficientemente documentadas.
4. Observaciones generales.

Todas las conclusiones deben citar fragmentos concretos del documento analizado.

No debes inventar información ni asumir controles que no aparezcan expresamente documentados.

Si una materia no aparece en el documento, debes indicarlo claramente.

La respuesta debe estar enfocada específicamente a MIDTECH S.A.

---

## Ejemplo de entrada

Analiza la política de seguridad de MIDTECH.

---

## Ejemplo de salida obtenida

### Áreas cubiertas

- Control de acceso.
- Gestión de usuarios.
- Copias de seguridad.
- Protección de datos.

### Nivel de cobertura

Control de acceso: Medio.

La política define la existencia de usuarios autorizados, pero no establece requisitos específicos de autenticación multifactor.

### Áreas ausentes

- Gestión de vulnerabilidades.
- Gestión de proveedores.
- Evaluaciones periódicas de seguridad.

### Observaciones

La política proporciona una base adecuada de controles generales, aunque presenta carencias en procesos de revisión periódica y gestión de riesgos.

---

## Valoración crítica

El resultado permite identificar rápidamente qué áreas de seguridad están contempladas y cuáles requieren mejoras.

La principal limitación es que la calidad del análisis depende directamente del nivel de detalle existente en la política de seguridad.
