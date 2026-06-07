# TFC-MIDTECH-Asistente-Compliance-IA

## Descripción general

Proyecto de Trabajo Fin de Curso orientado al diseño e implementación de un asistente inteligente de compliance y ciberseguridad para la empresa ficticia MIDTECH S.A.

La solución utiliza Inteligencia Artificial Generativa y una arquitectura Retrieval-Augmented Generation (RAG) para consultar documentación corporativa y normativa relacionada con GDPR, ISO 27001, ENS y políticas de seguridad.

El sistema ha sido desarrollado utilizando n8n, OpenAI GPT-4o y GitHub como repositorio centralizado del proyecto.

## Flujo de consulta

Usuario

↓

Chat Usuario

↓

Asistente MIDTECH

↓

RAG - Consulta Documental

↓

GPT-4o

↓

Respuesta fundamentada

---

## Flujo de indexación

GitHub

↓

Cargador Documental GitHub

↓

Embeddings OpenAI

↓

RAG Indexación

↓

Base Vectorial

---

## Evidencias

La carpeta `evidencias` contiene las capturas utilizadas para validar el funcionamiento del sistema durante las pruebas realizadas.

Entre las evidencias incluidas se encuentran:

- Arquitectura del sistema.
- Indexación documental.
- Recuperación RAG.
- Consultas sobre GDPR.
- Consultas sobre ISO 27001.
- Consultas sobre ENS.
- Análisis de cumplimiento.
- Generación de informes de auditoría.

---

## Workflows

La carpeta `workflows` contiene las exportaciones de los flujos desarrollados en n8n.

El workflow principal implementa:

- Consulta documental mediante RAG.
- Indexación documental desde GitHub.
- Integración con OpenAI GPT-4o.
- Generación de respuestas basadas en documentación corporativa.

---

## Consideraciones sobre la gestión documental

Durante la fase inicial del proyecto se consideró la utilización de Google Drive como repositorio documental, de acuerdo con las alternativas planteadas en la documentación base del programa formativo.

Sin embargo, la solución final implementada utiliza GitHub como repositorio principal debido a sus capacidades de control de versiones, trazabilidad y centralización de documentación, workflows, evidencias y base documental RAG.

La documentación final del proyecto puede entregarse mediante Google Drive si así lo requiere la entidad evaluadora.


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
