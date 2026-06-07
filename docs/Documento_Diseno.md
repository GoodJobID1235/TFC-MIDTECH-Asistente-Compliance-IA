
# Documento de Diseño

## Proyecto

Asistente de Ciberseguridad y Compliance con IA para MIDTECH S.A.

---

## Objetivo

Diseñar un asistente basado en Inteligencia Artificial capaz de analizar documentación corporativa y responder consultas relacionadas con cumplimiento normativo, ciberseguridad y auditoría.

El asistente se centra en las normativas GDPR, ISO 27001 y ENS.

---

## Organización de referencia

MIDTECH S.A. es una empresa del sector biotecnológico y farmacéutico que trabaja con datos de salud y presta servicios a hospitales públicos y privados.

Debido a la naturaleza de los datos tratados, la organización debe cumplir requisitos avanzados de seguridad y protección de datos.

---

## Tecnologías seleccionadas

### Modelo LLM

OpenAI GPT-4o.

#### Motivos

- Excelente comprensión del lenguaje natural.
- Capacidad de análisis documental.
- Buen rendimiento en tareas de auditoría y compliance.
- Integración sencilla mediante API.

---

### Orquestación

n8n.

#### Motivos

- Diseño visual de flujos.
- Integración sencilla con Google Drive.
- Automatización sin necesidad de programación compleja.

---

### Gestión documental

Google Drive.

#### Motivos

- Almacenamiento centralizado.
- Facilidad para compartir documentación.
- Integración directa con n8n.

---

### Base de conocimiento

RAG mediante embeddings e indexación semántica.

#### Motivos

- Reduce alucinaciones.
- Permite responder utilizando únicamente documentos autorizados.
- Facilita respuestas fundamentadas y trazables.

---

## Arquitectura del sistema

Usuario

↓

n8n

↓

Base de conocimiento RAG

↓

GPT-4o

↓

Respuesta al usuario

---

## Documentos utilizados

- Política de Seguridad de MIDTECH.
- GDPR Artículo 32.
- Resumen ISO 27001.
- Resumen ENS RD 311/2022.

---

## Funcionamiento del sistema

1. El usuario realiza una consulta.
2. n8n recibe la petición.
3. El sistema consulta la base documental.
4. Se recuperan los fragmentos relevantes.
5. GPT-4o analiza la información recuperada.
6. Se genera una respuesta basada en la documentación disponible.

---

## Beneficios

- Centralización del conocimiento.
- Respuestas rápidas.
- Mejora del cumplimiento normativo.
- Apoyo a auditorías.
- Reducción del tiempo de búsqueda documental.

---

## Limitaciones

- El sistema depende de la calidad de los documentos cargados.
- No sustituye una auditoría profesional.
- Requiere mantener actualizada la documentación.
