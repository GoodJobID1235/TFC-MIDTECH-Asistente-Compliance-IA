# Base de Conocimiento RAG

## Objetivo

Esta carpeta contiene la documentación utilizada por el asistente de ciberseguridad y compliance para responder consultas sobre la organización MIDTECH S.A.

Los documentos almacenados forman la base de conocimiento utilizada por el sistema RAG (Retrieval-Augmented Generation), permitiendo recuperar información relevante antes de generar respuestas.

---

## Documentos incluidos

### Política de Seguridad

- Politica_Seguridad_Informacion.pdf

Documento principal utilizado para el análisis de cumplimiento de MIDTECH S.A.

### GDPR

- GDPR_Articulo_32_Medidas_Seguridad.pdf

Contiene las medidas de seguridad exigidas por el Artículo 32 del Reglamento General de Protección de Datos.

### ISO 27001

- Resumen_ISO27001.pdf

Documento de referencia para controles de seguridad de la información y sistemas de gestión de seguridad.

### ENS

- Resumen_ENS_RD311_2022.pdf

Documento de referencia del Esquema Nacional de Seguridad aplicable a organizaciones que trabajan con entidades públicas.

---

## Arquitectura de referencia

### Gestión documental

Google Drive como repositorio central de normativa y documentación corporativa.

### Base de conocimiento

RAG mediante embeddings e indexación semántica de documentos.

### Orquestación

n8n.

### Modelo LLM

OpenAI GPT-4o.

---

## Flujo de funcionamiento

1. El usuario realiza una consulta.
2. El sistema busca información relevante en los documentos indexados.
3. Se recuperan los fragmentos más relevantes.
4. Los fragmentos se envían al modelo LLM.
5. El modelo genera una respuesta basada en la documentación disponible.

---

## Normativas de referencia

- GDPR (Artículo 32)
- ISO 27001
- ENS (RD 311/2022)

Estas normativas constituyen la base regulatoria utilizada para el análisis de cumplimiento de MIDTECH S.A.
