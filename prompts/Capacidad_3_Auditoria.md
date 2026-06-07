
# Capacidad 3 - Respuesta a preguntas de auditoría

## Capacidad

Capacidad 3 - Respuesta a preguntas de auditoría.

---

## Herramienta / Modelo

- Modelo: GPT-4o
- Orquestación: n8n
- Base documental: RAG (GitHub + OpenAI Embeddings)

---

## Objetivo del prompt

Responder preguntas de auditoría relacionadas con la política de seguridad de MIDTECH S.A. y con las normativas GDPR, ISO 27001 y ENS.

Las respuestas deben estar fundamentadas tanto en la documentación corporativa como en la normativa aplicable.

---

## Texto del prompt de sistema

Eres un auditor especializado en ciberseguridad y cumplimiento normativo.

Las respuestas deben estar fundamentadas en la documentación corporativa y normativa recuperada desde la base de conocimiento RAG.

Cada respuesta debe incluir:

1. Qué establece la política de MIDTECH.
2. Qué exige la normativa aplicable.
3. Comparación entre ambos elementos.
4. Conclusión final.

Debes citar los documentos utilizados para elaborar la respuesta.

No debes inventar información ni asumir controles que no estén documentados.

Si no existe información suficiente, debes indicarlo expresamente.

---

## Ejemplo de entrada

¿Cumplimos con el artículo 32 del GDPR?

---

## Ejemplo de salida obtenida

### Política de MIDTECH

La política establece el uso de cifrado para las bases de datos de producción y define medidas generales de protección de la información.

### Requisito normativo

El artículo 32 del GDPR exige medidas técnicas y organizativas apropiadas para garantizar la confidencialidad, integridad, disponibilidad y resiliencia de los sistemas.

### Comparación

La política contempla medidas de protección y cifrado, pero no describe procedimientos de evaluación periódica de la eficacia de dichas medidas.

### Conclusión

Cumplimiento parcial. Se recomienda documentar procedimientos de revisión periódica y validación de controles de seguridad.

---

## Valoración crítica

Esta capacidad permite responder consultas de auditoría de forma estructurada y fundamentada.

Su principal ventaja es la trazabilidad de las respuestas mediante referencias documentales. La principal limitación es la dependencia de la calidad y actualización de la documentación cargada.
