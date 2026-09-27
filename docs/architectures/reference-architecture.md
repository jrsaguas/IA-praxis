# Arquitectura de referencia

**Fecha:** 2026-09-27  
**Estado:** PROPUESTA BASE

## 1. Diagrama lógico

```
                    ┌─────────────────────┐
                    │      INTERFACE      │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │     ORCHESTRATOR    │
                    └────┬────┬────┬──────┘
                         │    │    │
              ┌──────────▼┐ ┌─▼──┐ ┌▼──────────┐
              │  PLANNER  │ │MEM │ │ RETRIEVER │
              └─────┬─────┘ └─┬──┘ └────┬──────┘
                    │         │         │
                    │    ┌────▼────┐    │
                    │    │KNOWLEDGE│◄───┘
                    │    │  STORE  │
                    │    └─────────┘
                    │
             ┌──────▼──────┐
             │ MODEL ROUTER│
             └──────┬──────┘
                    │
        ┌───────────▼───────────┐
        │       MODEL(S)        │
        └───────────┬───────────┘
                    │
             ┌──────▼──────┐
             │    TOOLS    │
             └──────┬──────┘
                    │
             ┌──────▼──────┐
             │   RUNTIME   │
             └──────┬──────┘
                    │
             ┌──────▼──────┐
             │  EVALUATOR  │
             └──────┬──────┘
                    │
          ┌─────────▼─────────┐
          │ EXPERIENCE/LEARN  │
          └───────────────────┘
```

## 2. Separación crítica

### Modelo

Los pesos contienen conocimiento paramétrico y capacidades aprendidas. El modelo no debe convertirse en el único almacén de información.

### Knowledge Store

Almacena conocimiento externo con estructura, procedencia, versión, fecha, autoridad, confianza y relaciones.

### Retrieval

Decide qué evidencia debe llegar al modelo. Debe combinar, cuando sea útil:

- búsqueda exacta;
- lexical;
- vectorial;
- híbrida;
- reranking;
- filtros estructurados;
- relaciones del grafo.

### Memory

No es un simple historial de chat. Debe separar:

- contexto temporal;
- estado de trabajo;
- episodios;
- conocimiento semántico;
- procedimientos;
- experiencias reutilizables.

### Planner

Convierte objetivos en subtareas verificables. No debe ejecutar directamente aquello que pueda delegarse a mecanismos deterministas.

### Tools

La capacidad de cálculo, archivos, búsqueda, ejecución de código, Git y otras acciones debe vivir fuera de los pesos cuando sea posible.

### Evaluator

Debe poder comprobar resultados independientemente del generador. Para programación, esto significa ejecutar tests, linters, type-checkers y validaciones específicas cuando proceda.

### Runtime

Controla:

- permisos;
- estado;
- límites;
- timeouts;
- recursos;
- trazas;
- errores;
- recuperación;
- cancelación.

## 3. Knowledge Compiler

El componente estratégico de ingestión será un compilador de conocimiento:

```
Fuente
  ↓
Parser
  ↓
Normalización
  ↓
Segmentación semántica
  ↓
Extracción
  ↓
Conceptos / hechos / reglas / procedimientos
  ↓
Deduplicación
  ↓
Contradicción y provenance
  ↓
Representación compacta
  ↓
Índices
  ├── exacto
  ├── lexical
  ├── vectorial
  └── grafo
```

No toda información debe convertirse automáticamente en una afirmación permanente. La procedencia y el estado de validación forman parte del dato.

## 4. Principio de determinismo

Antes de llamar a un LLM debe preguntarse:

> ¿Puede resolver esta operación un algoritmo determinista más barato y verificable?

Ejemplos:

- aritmética → código;
- parsing → parser;
- búsqueda exacta → índice;
- tests → runner;
- formato → formatter;
- validación de tipos → type checker.

El LLM se reserva para las partes donde su flexibilidad aporta valor.

## 5. Enrutamiento de modelos

IA-praxis no debe asumir un modelo único.

Un router futuro podrá seleccionar entre:

- modelo pequeño para clasificación/extracción;
- modelo de razonamiento para tareas complejas;
- modelo especializado;
- herramienta determinista;
- ningún modelo cuando no sea necesario.

La decisión deberá medirse por costo y fiabilidad.

## 6. Restricción de recursos

La arquitectura debe ser compatible con hardware modesto.

Se investigarán:

- cuantización;
- pruning/sparsity;
- distillation;
- LoRA/QLoRA;
- KV-cache compression/quantization;
- caching;
- prompt/context compression;
- retrieval compression;
- speculative decoding;
- batching;
- model routing;
- delegación a modelos pequeños.

La optimización será experimental: ninguna técnica se adoptará solo por popularidad.

