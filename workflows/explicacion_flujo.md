# Explicación Técnica del Workflow

## Descripción General

Este workflow implementa el sistema principal del proyecto TFC MIDTECH – Asistente Compliance IA.

La solución utiliza una arquitectura Retrieval-Augmented Generation (RAG) para responder consultas relacionadas con compliance, ciberseguridad y normativa aplicable a MIDTECH S.A.

---

## Componentes principales

### 1. Chat Usuario

Punto de entrada de las consultas realizadas por el usuario.

Recibe preguntas relacionadas con auditoría, cumplimiento normativo, políticas de seguridad y documentación corporativa.

---

### 2. Asistente MIDTECH

Agente principal basado en OpenAI GPT-4o.

Su función consiste en:

- Interpretar la consulta del usuario.
- Utilizar la base documental disponible.
- Generar respuestas fundamentadas.
- Identificar incumplimientos y riesgos.
- Proponer acciones correctivas.

---

### 3. RAG – Consulta Documental

Base de conocimiento utilizada por el asistente.

Permite recuperar información relevante mediante búsqueda semántica utilizando embeddings generados por OpenAI.

La documentación consultada incluye:

- Política de Seguridad de MIDTECH.
- GDPR Artículo 32.
- ISO 27001.
- ENS (RD 311/2022).

---

### 4. OpenAI Embeddings

Responsable de transformar los documentos y consultas en representaciones vectoriales para facilitar la recuperación semántica de información.

---

### 5. Cargador Documental GitHub

Nodo encargado de recuperar la documentación almacenada en el repositorio GitHub del proyecto.

GitHub actúa como repositorio documental centralizado.

---

### 6. RAG Indexación

Proceso utilizado para:

- Leer documentos desde GitHub.
- Generar embeddings.
- Almacenar la información en el Vector Store.
- Actualizar la base documental utilizada por el asistente.

---

## Flujo de funcionamiento

1. El usuario realiza una consulta.
2. El asistente interpreta la petición.
3. Se consulta la base documental RAG.
4. Se recuperan fragmentos relevantes.
5. GPT-4o genera una respuesta basada en la documentación encontrada.
6. El resultado se devuelve al usuario.

---

## Tecnologías utilizadas

- n8n
- OpenAI GPT-4o
- OpenAI Embeddings
- GitHub
- Retrieval-Augmented Generation (RAG)

---

## Seguridad

El workflow exportado no contiene:

- Claves API.
- Tokens GitHub.
- Credenciales OpenAI.
- Información sensible.

Todas las credenciales han sido eliminadas o protegidas antes de la publicación del repositorio.

---

## Resultado

La arquitectura desarrollada permite consultar documentación corporativa y normativa, analizar requisitos de cumplimiento, detectar deficiencias y generar informes de auditoría de forma asistida mediante Inteligencia Artificial Generativa.
