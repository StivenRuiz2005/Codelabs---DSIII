# Preguntas y Respuestas sobre la Metodología ADD

## ¿Cuál es el propósito principal de la metodología ADD en el diseño de arquitecturas de software?
El propósito principal de la metodología ADD (Attribute-Driven Design) es guiar la creación de arquitecturas de software basadas en los atributos de calidad requeridos por el sistema, asegurando que las decisiones arquitectónicas respondan de forma estructurada y justificada a las necesidades del negocio y los requerimientos técnicos.

## ¿Qué atributos de calidad se consideran en ADD y por qué son importantes en el proceso de diseño?
En ADD se consideran atributos como rendimiento, disponibilidad, seguridad, modifiabilidad, usabilidad, entre otros. Son importantes porque impactan directamente en la satisfacción del usuario final, el mantenimiento del sistema y su comportamiento bajo condiciones específicas, guiando las decisiones arquitectónicas desde una perspectiva no funcional.

## Explica la importancia de la selección del módulo a diseñar en ADD. ¿Cuáles son los criterios principales para elegir un módulo?
La selección del módulo es crucial porque define el alcance inmediato del diseño y permite enfocar las decisiones. Los criterios principales incluyen: prioridad de los requerimientos de calidad, riesgo técnico, impacto funcional y dependencia con otros módulos.

## ¿Cómo influyen las tácticas arquitectónicas en la toma de decisiones dentro de ADD? Menciona dos ejemplos de tácticas y su aplicación.
Las tácticas arquitectónicas son soluciones genéricas que ayudan a cumplir atributos de calidad. Influyen al ofrecer patrones de decisión concretos.  
**Ejemplo 1:** *Caching* para mejorar el rendimiento.  
**Ejemplo 2:** *Autenticación* para incrementar la seguridad del sistema.

## ¿Cuál es la relación entre los escenarios de calidad y la evaluación de la arquitectura en ADD?
Los escenarios de calidad permiten definir de forma precisa cómo deben evaluarse los atributos de calidad en la arquitectura. Son esenciales para validar que las decisiones tomadas cumplen los objetivos no funcionales establecidos.

## Describe los principales pasos del proceso ADD y cómo se interrelacionan.
1. Seleccionar el módulo a diseñar.
2. Identificar los requerimientos de calidad relevantes.
3. Elegir tácticas y patrones arquitectónicos.
4. Crear o refinar la estructura del módulo.
5. Evaluar el diseño frente a los escenarios de calidad.
6. Documentar las decisiones.
Estos pasos se interrelacionan de forma iterativa, permitiendo revisiones y ajustes conforme se avanza en el diseño.

## ¿Por qué es crucial documentar las decisiones arquitectónicas en ADD? Menciona al menos tres elementos que deben incluirse en la documentación.
Documentar es vital para mantener la trazabilidad, facilitar la comunicación y apoyar futuras modificaciones.  
Elementos que deben incluirse:
- Justificación de las decisiones tomadas.
- Tácticas aplicadas y su relación con los atributos de calidad.
- Escenarios de calidad y cómo se satisfacen.

## En un proyecto real, ¿cómo se puede evaluar si una arquitectura diseñada con ADD cumple con los atributos de calidad esperados?
Se puede evaluar mediante revisiones arquitectónicas, análisis de escenarios, pruebas específicas de atributos (como pruebas de carga o de seguridad), y validación con stakeholders a través de prototipos o simulaciones.

## ¿Cuáles son los beneficios de utilizar ADD en comparación con otros enfoques de diseño arquitectónico?
- Enfoque sistemático y centrado en la calidad.
- Mejora la trazabilidad entre requerimientos y decisiones.
- Facilita la justificación y documentación de la arquitectura.
- Promueve una arquitectura alineada con objetivos del negocio.

## ¿Qué desafíos pueden surgir al aplicar ADD en un equipo de desarrollo y cómo podrían abordarse?
Desafíos comunes:
- Falta de experiencia en identificación de atributos de calidad.
- Dificultad para definir escenarios concretos.
- Problemas de comunicación en equipos multidisciplinarios.
Se pueden abordar con capacitación, uso de plantillas estandarizadas y sesiones colaborativas de análisis y diseño.
