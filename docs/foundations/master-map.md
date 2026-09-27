# Mapa maestro de IA-praxis

**Fecha:** 2026-09-27  
**Estado:** FUNDACIÓN DOCUMENTAL  
**Propósito:** definir el mapa conceptual que guiará investigación, implementación y evaluación.

## 1. Jerarquía conceptual

IA-praxis se estudia como una cadena de capacidades, no como un único modelo:

1. Matemáticas y fundamentos computacionales
2. Neurona artificial
3. Redes neuronales
4. Aprendizaje automático
5. Deep Learning
6. Representaciones y embeddings
7. Atención
8. Transformer
9. Modelos fundacionales y LLM
10. Conocimiento externo
11. Recuperación (retrieval)
12. Memoria
13. Razonamiento
14. Planificación
15. Herramientas
16. Ejecución en entorno
17. Evaluación
18. Agente
19. Agentes especializados
20. Multi-agente
21. Sistema autónomo adaptativo

La cadena no implica que cada nivel sea estrictamente necesario para todos los sistemas. Es un mapa de dependencias conceptuales.

## 2. Ficha obligatoria de cada concepto

Cada concepto que entre al corpus de IA-praxis deberá poder describirse mediante:

- **Definición:** qué es.
- **Mecanismo:** cómo funciona.
- **Problema que resuelve.**
- **Entradas y salidas.**
- **Costo:** RAM, CPU/GPU, almacenamiento, latencia y llamadas al modelo.
- **Alternativas:** otras formas de resolver el mismo problema.
- **Limitaciones y fallos.**
- **Implementación Python:** cuando sea pertinente.
- **Implementaciones/referencias:** repositorios y herramientas relevantes.
- **Papers/fuentes primarias:** cuando existan.
- **Dependencias conceptuales.**
- **Relación con IA-praxis.**
- **Método de evaluación.**

## 3. Familias de arquitectura que debemos estudiar

### 3.1 Arquitectura de modelos

MLP, CNN, RNN, LSTM, GRU, Transformer encoder, Transformer decoder, encoder-decoder, Mixture-of-Experts, State Space Models y arquitecturas híbridas.

### 3.2 Arquitectura de sistemas

Pipeline, chain, router, planner/executor, ReAct, plan-and-execute, reflection/critic, supervisor, hierarchical agents, graph agents, event-driven, blackboard, debate y swarm.

### 3.3 Arquitectura de conocimiento

RAG, búsqueda léxica, búsqueda semántica, búsqueda híbrida, reranking, knowledge graph, GraphRAG, índices jerárquicos y recuperación multi-vector.

### 3.4 Arquitectura de memoria

Contexto inmediato, working memory, memoria episódica, semántica, procedural, memoria de largo plazo, consolidación, compresión y experience replay.

## 4. Capas de IA-praxis

La arquitectura de referencia queda dividida en:

- **Model:** inferencia generativa/reasoning.
- **Knowledge:** conocimiento externo estructurado.
- **Retrieval:** localización del conocimiento relevante.
- **Memory:** persistencia y experiencia.
- **Reasoning:** transformación de evidencia en conclusiones.
- **Planning:** descomposición y ordenamiento de objetivos.
- **Tools:** capacidades deterministas y externas.
- **Runtime:** ejecución, estado, permisos y observabilidad.
- **Evaluation:** medición y crítica.
- **Learning:** incorporación controlada de nuevas capacidades.
- **Interface:** interacción con usuario y sistemas.
- **Security:** límites, aislamiento y control.

## 5. Principio central

El proyecto no debe asumir que aumentar el número de parámetros es la única vía para aumentar capacidad.

La hipótesis experimental de IA-praxis es:

> **Capacidad efectiva = modelo + conocimiento externo + recuperación + memoria + razonamiento + planificación + herramientas + evaluación + runtime**

La expresión no es una fórmula matemática de rendimiento. Es un modelo de ingeniería que permite aislar y medir contribuciones.

## 6. Primera especialización

La primera especialización será **programación** y, dentro de ella, **Python**.

La competencia se representará como una estructura con:

- prerrequisitos;
- conceptos;
- sintaxis;
- semántica;
- ejemplos;
- patrones;
- anti-patrones;
- ejercicios;
- tests;
- tareas prácticas;
- errores frecuentes;
- dependencias;
- evidencia de dominio.

El objetivo es medir qué sabe hacer el sistema, no únicamente qué información puede recuperar.

## 7. Métrica de cobertura

No se utilizará un único porcentaje de "conocimiento".

Se medirán dimensiones separadas:

- cobertura conceptual;
- exactitud;
- profundidad;
- capacidad procedural;
- razonamiento;
- uso de herramientas;
- transferencia a tareas nuevas;
- autoconocimiento de límites.

La cobertura deberá poder desglosarse por dominio y subdominio.

## 8. Regla experimental

Toda mejora arquitectónica relevante deberá compararse contra una línea base y reportar al menos:

- calidad/accuracy;
- tasa de errores;
- alucinaciones;
- éxito de tarea;
- RAM;
- CPU/GPU;
- almacenamiento;
- latencia;
- tokens;
- número de llamadas al modelo;
- tamaño del contexto;
- cobertura del conocimiento.

