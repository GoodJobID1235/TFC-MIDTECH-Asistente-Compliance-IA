
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
- Facilidad para integrar modelos de IA, repositorios documentales y sistemas RAG.
- Automatización sin necesidad de programación compleja.
- Posibilidad de validar y depurar cada nodo individualmente.
- Representación gráfica clara de la arquitectura implementada.

#### Justificación

La elección de n8n se basa en su enfoque visual y en la facilidad para construir flujos complejos mediante nodos conectados. Esto permitió desarrollar, probar y documentar el asistente de forma progresiva, facilitando además la comprensión del sistema por parte del evaluador.

### Gestión documental y repositorio del proyecto

GitHub.

#### Motivos

- Centralización de toda la documentación del proyecto.
- Control de versiones y trazabilidad de cambios.
- Almacenamiento de la base documental utilizada por el sistema RAG.
- Gestión de workflows de n8n.
- Organización de evidencias, diagramas y documentación técnica.
- Integración con el flujo de indexación documental implementado.

#### Justificación

Aunque durante la fase inicial de diseño se valoró la utilización de Google Drive, tal y como se proponía en la documentación base del proyecto, finalmente se optó por GitHub como repositorio principal.

Esta decisión permitió centralizar en una única plataforma la base documental RAG, los workflows de n8n, las evidencias, los diagramas y la documentación técnica del proyecto, aportando un mejor control de versiones y una mayor trazabilidad.

La documentación final puede entregarse mediante Google Drive si así lo requiere la entidad evaluadora, sin que ello modifique la solución técnica implementada.
### Base de conocimiento

RAG mediante embeddings e indexación semántica.

#### Motivos

- Reduce alucinaciones.
- Permite responder utilizando únicamente documentos autorizados.
- Facilita respuestas fundamentadas y trazables.

---

## Arquitectura del sistema

Chat Usuario

↓

Asistente MIDTECH

↓

RAG - Consulta Documental

↓

Base Vectorial

↓

Embeddings OpenAI

↓

Documentación indexada desde GitHub

↓

Respuesta fundamentada al usuario

---

Proceso de indexación documental

GitHub

↓

Cargador Documental GitHub

↓

Embeddings OpenAI

↓

RAG Indexación

↓

Base Vectorial

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

- ---

## Organización del repositorio

El proyecto utiliza GitHub como repositorio centralizado para almacenar todos los elementos relacionados con el desarrollo del asistente Compliance MIDTECH.

La estructura del repositorio se ha diseñado para separar claramente la documentación técnica, la base documental utilizada por el sistema RAG, los workflows de n8n y las evidencias generadas durante las pruebas.

### Estructura principal

- docs: documentación técnica y funcional del proyecto.
- diagramas: diagramas de arquitectura y representación de flujos.
- evidencias: capturas utilizadas para validar el funcionamiento del sistema.
- prompts: instrucciones y configuraciones utilizadas por el asistente.
- rag: documentación normativa y corporativa utilizada por la base de conocimiento.
- workflows: exportaciones de los flujos desarrollados en n8n.
- README.md: documento principal de presentación del proyecto.

Esta organización facilita la trazabilidad, el mantenimiento y la revisión del proyecto por parte del evaluador.

---

## Tecnologías utilizadas

### OpenAI GPT-4o

Modelo de lenguaje utilizado para interpretar consultas, analizar documentación recuperada mediante RAG y generar respuestas contextualizadas relacionadas con compliance y ciberseguridad.

### n8n

Plataforma de automatización utilizada para construir y orquestar todos los flujos del proyecto mediante una interfaz visual basada en nodos.

### GitHub

Repositorio utilizado para almacenar la base documental RAG, los workflows, las evidencias y la documentación técnica del proyecto.

### Embeddings OpenAI

Servicio utilizado para transformar documentos en representaciones vectoriales que permiten realizar búsquedas semánticas dentro de la base documental.

### Retrieval-Augmented Generation (RAG)

Arquitectura utilizada para recuperar información relevante desde documentos corporativos antes de generar la respuesta final, mejorando la precisión y la trazabilidad del asistente.

---

## Workflow implementado

El workflow principal desarrollado en n8n se encuentra disponible en la carpeta workflows del repositorio.

Este flujo implementa dos procesos diferenciados:

### Flujo de consulta

Chat Usuario

↓

Asistente MIDTECH

↓

RAG - Consulta Documental

↓

OpenAI GPT-4o

↓

Respuesta al usuario

### Flujo de indexación

GitHub

↓

Cargador Documental GitHub

↓

Embeddings OpenAI

↓

RAG Indexación

↓

Base Vectorial

La arquitectura permite separar el proceso de construcción de la base de conocimiento del proceso de consulta realizado por los usuarios.
