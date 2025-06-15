# Preguntas

### ¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?
Attribute-Driven Design (ADD) es un método de diseño arquitectónico que se enfoca en los **atributos de calidad** (como rendimiento, seguridad, mantenibilidad, etc.) para tomar decisiones arquitectónicas. Su propósito principal es **guiar el diseño de una arquitectura basada en los requerimientos del sistema**, priorizando los atributos de calidad definidos por los stakeholders.

---

### ¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?
ADD y Clean Architecture se complementan. ADD define la **estructura inicial de la arquitectura basada en atributos de calidad**, mientras que Clean Architecture proporciona un marco claro para **organizar el sistema en capas independientes**, promoviendo separación de responsabilidades y facilidad de mantenimiento.

---

### ¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?
1. **Identificar los requerimientos del sistema**, incluyendo atributos de calidad y restricciones.
2. **Seleccionar un módulo o parte del sistema a diseñar**.
3. **Elegir patrones arquitectónicos o tácticas apropiadas** para cumplir con los atributos de calidad.
4. **Dividir módulos en submódulos**, aplicando decisiones de diseño.
5. **Asignar responsabilidades y definir interfaces**.
6. **Validar las decisiones tomadas** en función de los requisitos.
7. **Repetir el proceso recursivamente** para los submódulos.

---

### ¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?
Se identifican a partir de:
- Entrevistas con stakeholders.
- Análisis de requisitos no funcionales.
- Escenarios de calidad (quality attribute scenarios).

Son importantes porque **guían las decisiones arquitectónicas clave** y aseguran que el sistema final cumpla con las expectativas de rendimiento, escalabilidad, seguridad, etc.

---

### ¿Por qué Clean Architecture complementa ADD en la implementación de una solución?
Clean Architecture complementa ADD porque:
- Establece **límites claros entre capas** (por ejemplo, dominio, aplicación, infraestructura).
- Facilita la **independencia del framework, UI y base de datos**.
- Permite que las decisiones tomadas con ADD puedan **materializarse de forma estructurada**, promoviendo un diseño mantenible y testable.

---

### ¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?
- **Dependencias dirigidas hacia el dominio** (Regla de dependencia).
- **Separación de preocupaciones** (cada capa tiene una única responsabilidad).
- **Testabilidad** de cada capa.
- **Flexibilidad para cambios tecnológicos** (frameworks, bases de datos, etc.).
- **Correspondencia con escenarios de atributos de calidad** definidos en ADD.

---

### ¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?
ADD prioriza los atributos de calidad que **reflejan directamente las prioridades del negocio**, como rendimiento, escalabilidad o seguridad. Al alinear las decisiones técnicas con estos atributos, se garantiza que la arquitectura **responda eficazmente a las necesidades y objetivos estratégicos del negocio**.

---

### ¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?
- **Diseño centrado en calidad**, gracias a ADD.
- **Estructura modular y desacoplada**, gracias a Clean Architecture.
- **Claridad en los límites del servicio**, facilitando el mantenimiento y escalado independiente.
- **Facilidad para pruebas y despliegue continuo**.
- **Mayor alineación entre arquitectura técnica y necesidades de negocio**.

---

### ¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?
- **Validación continua** mediante escenarios de calidad.
- **Revisión arquitectónica y prototipos**.
- **Pruebas específicas de atributos de calidad** (stress test, pruebas de seguridad, etc.).
- **Tácticas arquitectónicas explícitas** para abordar atributos clave.
- **Retroalimentación constante de stakeholders**.

---

### ¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?
- **ATAM (Architecture Tradeoff Analysis Method)**.
- **Modelado con C4, UML o ArchiMate**.
- **Pruebas automatizadas y de carga**.
- **ADR (Architectural Decision Records)** para documentar decisiones.
- **Análisis de métricas de calidad del código**.
- **Prototipos y pruebas de concepto (PoC)**.
