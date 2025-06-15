## Preguntas sobre Clean Architecture en Microservicios con Spring Boot

### ¿Cuál es el propósito principal de Clean Architecture en el desarrollo de software?
El propósito principal de **Clean Architecture** es **separar las preocupaciones** del software en capas bien definidas para lograr un sistema **independiente de frameworks, bases de datos, interfaces de usuario o cualquier agente externo**. Esto permite que el núcleo del negocio sea mantenible, testeable y adaptable a cambios tecnológicos.

---

### ¿Qué beneficios aporta Clean Architecture a un microservicio en Spring Boot?
- **Desacoplamiento total** entre lógica de negocio e infraestructura.
- **Facilidad de pruebas unitarias** sin necesidad de cargar el contexto de Spring.
- **Mejor organización del código** en capas claras.
- **Facilidad para cambiar tecnologías (bases de datos, frameworks)** sin afectar la lógica del dominio.
- **Mayor mantenibilidad y escalabilidad**, especialmente útil en sistemas distribuidos como microservicios.

---

### ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?
1. **Entidad (Domain Model)**: Contiene las reglas de negocio más puras, independientes de cualquier tecnología.
2. **Caso de uso (Application)**: Coordina las operaciones del sistema. Orquesta la lógica del negocio aplicando las reglas del dominio.
3. **Interfaz (Interface Adapters)**: Traduce datos desde y hacia el exterior (controllers, DTOs, mappers, etc.).
4. **Infraestructura (Frameworks & Drivers)**: Contiene detalles técnicos como controladores web, base de datos, APIs externas, etc.

---

### ¿Por qué se recomienda desacoplar la lógica de negocio de la infraestructura en un microservicio?
Porque permite:
- **Testear el dominio sin dependencias externas**.
- **Reutilizar el negocio en otros contextos**.
- **Sustituir tecnologías fácilmente** (como cambiar de base de datos o framework sin afectar el core).
- **Mantener el enfoque en el valor del negocio**, no en la tecnología.

---

### ¿Cuál es el rol de la capa de aplicación y qué tipo de lógica debería contener?
La capa de **aplicación** se encarga de:
- **Orquestar los casos de uso del sistema**.
- Llamar a los servicios de dominio.
- **Coordinar flujos** entre entidades y repositorios.
- No debe contener lógica de negocio profunda, sino lógica de aplicación.

---

### ¿Qué diferencia hay entre un UseCase y un Service en Clean Architecture?
- **UseCase**: Representa una operación o flujo del sistema, enfocado en **un objetivo del negocio** (ej: CrearUsuario, ProcesarPago).
- **Service**: Puede tener un rol más técnico o utilitario, pero en Clean Architecture, los servicios del dominio representan **lógica de negocio transversal**.

En Clean Architecture, se recomienda implementar la lógica de negocio como **UseCases explícitos**, separados y autónomos.

---

### ¿Por qué se recomienda definir Repositories como interfaces en la capa de dominio en lugar de usar directamente JpaRepository?
- **Independencia del framework**: JpaRepository es parte de Spring Data y acopla el dominio a una tecnología específica.
- **Facilita pruebas**: Puedes usar mocks o fakes sin necesidad de Spring.
- **Flexibilidad**: Puedes cambiar a otra tecnología de persistencia (MongoDB, Cassandra, etc.) sin modificar el dominio.
- **Claridad**: Define qué operaciones necesita el dominio, no todo lo que JpaRepository ofrece.

---

### ¿Cómo se implementa un UseCase en un microservicio con Spring Boot y qué ventajas tiene?
**Implementación básica:**
1. Crear una interfaz `UseCase`.
2. Crear una clase que implemente la lógica.
3. Inyectar los repositorios definidos en el dominio.
4. Usar esta clase desde un controller o servicio.

**Ventajas:**
- Código **altamente testeable**.
- Independencia de Spring: se puede usar sin contexto.
- Lógica bien encapsulada.
- Facilita el cambio tecnológico sin romper el dominio.

---

### ¿Qué problemas podrían surgir si no aplicamos Clean Architecture en un proyecto de microservicios?
- **Alto acoplamiento** entre capas.
- **Dificultad para probar la lógica de negocio**.
- **Duplicación de lógica** al escalar microservicios.
- **Cambios tecnológicos impactan todo el sistema**.
- **Mala organización del código**, dificultando el mantenimiento y la evolución del software.

---

### ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad en un entorno basado en microservicios?
- **Cada microservicio tiene límites claros**, lo que permite su evolución independiente.
- **La lógica de negocio se conserva limpia y reusable**, facilitando su ampliación.
- **Infraestructura desacoplada**, permitiendo escalar tecnologías sin afectar el núcleo.
- **Mejor colaboración entre equipos**, al tener contratos claros entre capas.
- **Reducción de deuda técnica**, promoviendo buenas prácticas desde el diseño.

