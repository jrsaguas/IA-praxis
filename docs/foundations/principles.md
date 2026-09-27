# Principios de diseño de IA-praxis

**Fecha:** 2026-09-27

1. **No aumentar capacidad por fuerza bruta cuando la arquitectura pueda hacerlo de forma más eficiente.**
2. **No almacenar información cuando pueda almacenarse conocimiento estructurado.**
3. **No almacenar conocimiento cuando una representación más pequeña preserve su recuperación y aplicación.**
4. **No llamar al modelo cuando un mecanismo determinista pueda resolver el problema con igual o mayor fiabilidad.**
5. **No utilizar un modelo grande cuando uno pequeño pueda resolver la tarea con la misma fiabilidad.**
6. **Toda mejora debe ser medible.**
7. **La memoria no es un historial infinito.**
8. **El conocimiento debe conservar procedencia y versión.**
9. **La generación y la evaluación deben estar desacopladas.**
10. **La autonomía debe estar limitada por permisos, recursos y políticas explícitas.**
11. **La experimentación debe poder reproducirse.**
12. **Las abstracciones propias se justifican cuando permiten medir o controlar algo que un framework oculta.**
13. **Los frameworks son herramientas, no la arquitectura del proyecto.**
14. **El sistema debe conocer y registrar sus límites mediante evidencia, no mediante una frase genérica de "no sé".**
15. **El aprendizaje continuo debe ser controlado: una interacción no se convierte automáticamente en conocimiento permanente.**

## Hipótesis principal

Un modelo relativamente pequeño puede alcanzar una capacidad práctica considerable si el sistema externaliza de forma eficiente conocimiento, memoria, recuperación, herramientas, planificación y evaluación.

Esta hipótesis deberá probarse experimentalmente y puede resultar falsa en determinados dominios o niveles de dificultad.

## Hipótesis secundaria

La especialización puede representarse como una matriz de competencias verificables en lugar de un concepto global de "saber programación".

Esto permitirá medir adquisición, pérdida, transferencia y profundidad.
