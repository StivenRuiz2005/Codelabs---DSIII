# Preguntas y Respuestas sobre Clean Architecture

## ¿Qué problema busca resolver Clean Architecture en el desarrollo de software?
Clean Architecture busca resolver el problema del **acoplamiento excesivo** entre la lógica de negocio y los detalles técnicos (como frameworks, bases de datos o interfaces de usuario), permitiendo que el sistema sea más fácil de **mantener, probar, escalar y adaptar** a cambios tecnológicos.

## ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?
1. **Entidad (Entities):** contiene las reglas de negocio más generales y estables del sistema.
2. **Casos de Uso (Use Cases):** orquesta la lógica específica de aplicación, coordinando entidades para cumplir objetivos del negocio.
3. **Interfaz (Interface Adapters):** traduce datos entre los formatos de la aplicación (casos de uso) y los del mundo exterior (controladores, gateways, etc.).
4. **Infraestructura (Frameworks & Drivers):** contiene frameworks, bases de datos, controladores web, y otros detalles externos.

## ¿Qué relación tiene Clean Architecture con el principio de Inversión de Dependencias (DIP) en SOLID?
Clean Architecture aplica directamente el principio de Inversión de Dependencias (DIP), haciendo que las **dependencias siempre apunten hacia adentro**, desde capas externas hacia las internas. Es decir, la lógica de negocio **nunca depende** de los detalles técnicos, sino que estos dependen de **abstracciones** definidas por la lógica.

## ¿Por qué es importante desacoplar la lógica de negocio de la infraestructura en una aplicación?
Porque permite que la lógica de negocio:
- Sea independiente de tecnologías externas.
- Pueda cambiar de base de datos o framework sin reescribir reglas del negocio.
- Sea más testeable y reutilizable.
Esto reduce el costo de mantenimiento y facilita la evolución del software.

## ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad de un sistema?
- **Escalabilidad:** permite crecer en funcionalidad sin romper otras partes del sistema, al tener límites bien definidos.
- **Mantenibilidad:** facilita el cambio aislado de tecnologías y componentes, gracias a las interfaces y la separación de responsabilidades.

## ¿Qué diferencia hay entre la capa de dominio y la capa de aplicación en Clean Architecture?
- **Dominio (Entities):** contiene reglas de negocio puras, independientes de casos de uso específicos o detalles técnicos.
- **Aplicación (Use Cases):** define cómo se aplican esas reglas para cumplir acciones específicas del sistema (como "crear pedido" o "transferir fondos").

## ¿Por qué los controladores (controllers) y la base de datos deben estar en la capa de infraestructura?
Porque son detalles de implementación **externos** al dominio. Su rol es **interactuar con el exterior** (red, UI, almacenamiento) y traducir esa información a un formato comprensible por los casos de uso o entidades, siguiendo el principio de inversión de dependencias.

## ¿Qué ventajas tiene usar una interfaz en la capa de dominio para definir repositorios en lugar de usar directamente JpaRepository?
- Permite **desacoplar** el dominio del framework de persistencia (como JPA o Spring Data).
- Facilita el uso de distintas implementaciones (mock, in-memory, base de datos).
- Hace que el dominio **no dependa** de detalles técnicos ni librerías externas.

## ¿Cómo interactúan los casos de uso (UseCases) con las entidades de dominio en Clean Architecture?
Los casos de uso **orquestan** entidades de dominio para ejecutar acciones concretas. Utilizan métodos de las entidades para aplicar reglas del negocio, sin saber cómo se implementan los detalles externos como persistencia o interfaces gráficas.

## ¿Cómo se puede aplicar Clean Architecture en una aplicación de microservicios con Spring Boot?
- Definiendo cada microservicio como un **Bounded Context** con sus propias capas (entidades, casos de uso, interfaces, infraestructura).
- Usando **interfaces** en la capa de dominio para desacoplarse de Spring Data y controladores.
- Limitando la dependencia de Spring Boot a la capa de infraestructura (por ejemplo, los `@RestController` y `@Repository` están fuera del núcleo).
- Inyectando dependencias desde afuera hacia adentro (inversión de control).
