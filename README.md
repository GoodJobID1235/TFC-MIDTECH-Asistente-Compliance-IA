# TFC-MIDTECH-Asistente-Compliance-IA

Asistente de ciberseguridad y compliance basado en IA para la empresa ficticia MIDTECH S.A.

## Objetivo

Proporcionar asistencia en consultas relacionadas con:

- ISO 27001
- GDPR (Artículo 32)
- ENS (RD 311/2022)
- Política de Seguridad de la Información de MIDTECH

## Arquitectura

- n8n como motor de orquestación.
- OpenAI GPT-4o como modelo LLM.
- OpenAI Embeddings para vectorización.
- GitHub como repositorio documental.
- RAG (Retrieval-Augmented Generation) para recuperación semántica.

## Estructura del repositorio

- `/docs` → documentación del proyecto.
- `/diagramas` → diagramas de arquitectura y flujo.
- `/prompts` → prompts utilizados por el asistente.
- `/rag` → base documental utilizada por el sistema RAG.
- `/workflows` → exportaciones del flujo n8n.
- `/evidencias` → capturas y evidencias del funcionamiento.

## Funcionamiento

Los documentos almacenados en la carpeta `rag` son cargados desde GitHub, convertidos en embeddings mediante OpenAI e indexados en un Vector Store para permitir consultas documentales mediante RAG.
