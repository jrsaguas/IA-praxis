# Roadmap de IA-praxis

**Fecha:** 2026-09-27  
**Estado:** PLAN MAESTRO INICIAL

## Fase 0 — Fundamentos

- matemáticas relevantes;
- probabilidad;
- álgebra lineal;
- optimización;
- información;
- computación;
- representación de datos;
- fundamentos de ML.

## Fase 1 — Arquitecturas

- MLP;
- CNN;
- RNN/LSTM/GRU;
- atención;
- Transformer;
- encoder/decoder;
- MoE;
- SSM;
- multimodalidad.

## Fase 2 — Eficiencia

- cuantización;
- pruning;
- sparsity;
- distillation;
- LoRA/QLoRA;
- KV cache;
- caching;
- speculative decoding;
- routing.

## Fase 3 — Ingeniería del conocimiento

- parsing;
- chunking semántico;
- embeddings;
- metadatos;
- provenance;
- deduplicación;
- contradicciones;
- knowledge graphs;
- representación compacta.

## Fase 4 — Knowledge Compiler

Construir el primer componente propio de IA-praxis:

```
PDF/HTML/MD/TXT/CODE
        ↓
   INGESTION
        ↓
  EXTRACTION
        ↓
STRUCTURED KNOWLEDGE
        ↓
   VALIDATION
        ↓
     INDEXING
```

## Fase 5 — Memory Engine

Separar contexto, working memory, episodios, semántica, procedimientos y consolidación.

## Fase 6 — Retrieval Engine

Construir recuperación híbrida y medible.

## Fase 7 — Evaluation Engine

Crear benchmarks reproducibles por dominio, tarea y dificultad.

## Fase 8 — Agent Runtime

Implementar ciclo:

```
observe → understand → plan → retrieve → act → verify → remember
```

con límites, permisos y trazabilidad.

## Fase 9 — Tool System

Primero herramientas deterministas:

- filesystem;
- Python;
- tests;
- Git;
- búsqueda;
- parsers;
- conversores.

## Fase 10 — Coding Agent

Primer agente especializado en programación.

Capacidades iniciales:

- inspeccionar repositorio;
- comprender estructura;
- buscar código;
- modificar archivos;
- ejecutar tests;
- diagnosticar fallos;
- verificar cambios;
- producir commits/PRs bajo control.

## Fase 11 — Python Mastery

Construir una matriz computable de competencias Python:

- fundamentos;
- tipos;
- control de flujo;
- funciones;
- módulos;
- OOP;
- excepciones;
- iteradores/generadores;
- typing;
- concurrencia;
- async;
- testing;
- packaging;
- APIs;
- datos;
- rendimiento;
- seguridad;
- arquitectura.

## Fase 12 — Multi-agent

Solo después de demostrar qué problemas requieren múltiples agentes.

Se estudiarán:

- supervisor;
- especialistas;
- planner/executor;
- critic;
- researcher;
- coder;
- tester;
- reviewer.

La coordinación será evaluada contra una arquitectura de agente único equivalente.

## Regla de avance

No se avanza de fase únicamente porque una implementación "funcione".

Una fase se considera cerrada cuando existe:

1. implementación;
2. tests;
3. benchmark;
4. documentación;
5. comparación contra baseline;
6. medición de recursos;
7. límites conocidos.
