# Taller: Spec-Driven Development y Evolución de las Metodologías Ágiles en la Era de la IA

Este documento sintetiza las ideas principales, conceptos clave y enfoques de desarrollo expuestos en el material audiovisual analizado para el taller.

---

## 1. Spec-Driven Development: AI Assisted Coding Explained

**Fuente:** IBM Technology  
**Enlace:** https://youtu.be/mViFYTwWvcM

### Resumen Ejecutivo
La incorporación de Modelos Extensos de Lenguaje (LLM) y agentes de codificación está desplazando el esfuerzo principal del desarrollo de software: de escribir y revisar código manualmente a saber especificar con precisión qué se desea construir. El **Spec-Driven Development (SDD)** surge como una disciplina de ingeniería que integra el rigor del Ciclo de Vida de Desarrollo de Software (SDLC) con la generación asistida por inteligencia artificial.

### Conceptos Clave
* **Cambio de Paradigma:** La habilidad crítica para el ingeniero de software moderno consiste en traducir intenciones y reglas de negocio en especificaciones claras y sin ambigüedad para los modelos de IA.
* **Vibe Coding:** Enfoque iterativo basado en prompts informales de implementación directa. Aunque es útil para prototipado rápido, genera resultados inconsistentes entre ejecuciones, obliga al modelo a adivinar decisiones técnicas y omite fases esenciales del SDLC (diseño, pruebas formales, documentación).
* **Especificación como Fuente de Verdad:** En SDD, el artefacto principal no es el código fuente, sino la especificación detallada, la cual actúa como contrato que gobierna el diseño, la implementación y la verificación automatizada.

### Proceso de Desarrollo en SDD
1. **Prompt de Comportamiento:** Se instruye al modelo sobre qué debe hacer el sistema, sus restricciones y reglas de negocio, evitando dictar detalles prematuros de implementación.
2. **Generación de Especificación y Requisitos:** Se consolida un documento contractual que define la jerarquía del proyecto y establece un punto de control y aprobación humana antes de escribir código.
3. **Documento de Diseño:** Los requisitos aprobados se transforman en arquitectura técnica y en una lista estructurada de tareas pendientes (TODOs) que el desarrollador puede auditar y ajustar.
4. **Implementación y Verificación:** El agente de IA genera el código siguiendo el diseño aprobado y crea casos de prueba automatizados derivados directamente de los criterios definidos en la especificación.

### Comparativa Metodológica
| Enfoque | Punto de Partida | Rol de la Documentación / Pruebas | Comportamiento con IA |
| :--- | :--- | :--- | :--- |
| **Desarrollo Tradicional** | Intuición e implementación directa de código. | Documentación y pruebas al final del ciclo. | Propenso a deuda técnica si se delega sin control. |
| **Test-Driven Development (TDD)** | Casos de prueba unitarios antes del código. | Las pruebas validan el comportamiento esperado. | SDD extiende este principio a todo el diseño del sistema. |
| **Vibe Coding** | Prompt abierto sobre una funcionalidad. | Inexistente o generada de forma reactiva. | Alta variabilidad; el modelo asume arquitectura libremente. |
| **Spec-Driven Development (SDD)** | Especificación formal de comportamiento y reglas. | La especificación impulsa diseño, código y pruebas. | Determinismo, trazabilidad y control humano en cada fase. |

### Caso Práctico: Módulo de Autenticación
* **Con Vibe Coding:** Solicitar una ruta `/login` sin restricciones produce múltiples implementaciones arbitrarias y requiere ciclos extensos de corrección por prueba y error.
* **Con SDD:** Se especifica explícitamente el endpoint (`POST /login`), los parámetros de entrada (`user`, `pass`), el manejo de errores ante datos faltantes y los criterios de aceptación (respuesta HTTP `200` ante credenciales válidas), permitiendo al agente implementar y generar pruebas unitarias consistentes.

---

## 2. La IA ha Matado a Scrum (Esto es lo que viene Ahora)

**Fuente:** Javier Garzás  
**Enlace:** https://www.youtube.com/watch?v=jrTrihcZZlc

### Resumen Ejecutivo
Los marcos de trabajo ágiles tradicionales como Scrum fueron concebidos en la década de 1990 para gestionar la incertidumbre y coordinación exclusivamente entre equipos humanos. La irrupción de la inteligencia artificial generativa ha alterado radicalmente la velocidad de producción, la estructura de los equipos y la naturaleza de los artefactos, dejando obsoletos los pilares clásicos de Scrum y dando paso a nuevos modelos de gestión.

### Pilares de Scrum Impactados por la IA
* **Velocidad y Cadencia de Sprints:** Las iteraciones estándar de dos semanas pierden vigencia cuando la combinación de herramientas No-Code e IA generativa permite construir e incrementar productos funcionales en días o incluso horas.
* **Tamaño de los Equipos:** La regla tradicional de equipos de $7 \pm 2$ personas resulta sobredimensionada. La productividad individual potenciada por IA reduce drásticamente el número de integrantes necesarios, eliminando la necesidad de ceremonias diarias de sincronización intensiva.
* **Interacción Humano-IA:** Scrum fue diseñado para la comunicación interpersonal. Actualmente, perfiles de negocio pueden generar prototipos funcionales de forma autónoma mediante IA, redefiniendo la colaboración técnica.

### Obsolescencia de Roles y Artefactos
* **Evolución de Roles:**
  * El *Product Owner* tradicional evoluciona hacia el **AI Product Manager**, enfocado en potenciar el descubrimiento y entrega de producto con capacidades de IA.
  * El *Scrum Master* pierde relevancia operativa al reducirse los sprints y ceremonias formales.
  * Emergen perfiles híbridos como el **AI Product Builder**, encargados de ensamblar soluciones mediante arquitectura asistida por IA.
* **Mutación de Artefactos:**
  * Las **Historias de Usuario**, diseñadas para transmitir contexto entre personas, resultan insuficientes para instruir a máquinas.
  * Surgen las **Especificaciones (Specs)** como mecanismo preciso para indicar a los agentes de IA qué construir, mientras el *Product Backlog* tradicional se transforma para convivir con flujos automatizados.

### Tendencias y Nuevas Líneas de Trabajo
1. **Nuevos Roles Especializados:** Consolidación de líderes técnicos y de producto capacitados en IA generativa y ecosistemas No-Code/Low-Code.
2. **Ciclos de Vida de Doble Carril:**
   * *Carril de Vibe Coding:* Enfocado en validación ultrarrápida mediante prototipos no productivos con mínima intervención técnica.
   * *Carril de Vibe Engineering:* Enfocado en llevar soluciones a producción garantizando estándares de arquitectura, seguridad, escalabilidad y calidad.
   * Ambos carriles coexisten con el mantenimiento de sistemas heredados (*Legacy*).
3. **Adopción de Spec-Driven Development (SDD):** Estandarización de especificaciones estructuradas para guiar a la IA, evitando caer en un exceso de burocracia documental que reactive el modelo en cascada tradicional.
4. **Nuevo Enfoque de QA y Testing:** Transformación del aseguramiento de calidad hacia la auditoría del código generado automáticamente, implementando mecanismos de control, límites operativos y supervisión automatizada (modelos de IA auditando salidas de otros modelos).

---

## 3. Síntesis Integradora

Ambos materiales convergen en una misma conclusión operativa para la ingeniería de software moderna: **la inteligencia artificial ha desplazado el cuello de botella desde la codificación hacia la especificación y validación**. Mientras el análisis de Javier Garzás explica por qué las estructuras organizativas y ceremonias de Scrum dejan de ajustarse a equipos reducidos de alta velocidad, el enfoque de IBM Technology proporciona el mecanismo técnico concreto (**Spec-Driven Development**) para gobernar a los agentes de IA con rigor de ingeniería sin regresar a procesos rígidos en cascada.
