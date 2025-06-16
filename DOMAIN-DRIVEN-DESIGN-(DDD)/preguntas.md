# Preguntas y Respuestas sobre Domain-Driven Design (DDD)

## ¿Qué es Domain-Driven Design (DDD) y cuál es su objetivo principal?
Domain-Driven Design (DDD) es una metodología de diseño de software centrada en el dominio del problema y en la colaboración con expertos del mismo. Su objetivo principal es modelar el software de manera que refleje con precisión las reglas, procesos y lenguaje del dominio real, facilitando un diseño más alineado con las necesidades del negocio.

## ¿Cuál es la diferencia entre una Entidad y un Objeto de Valor en DDD?
Una **Entidad** es un objeto del dominio que tiene una identidad única persistente a lo largo del tiempo, independientemente de sus atributos.  
Un **Objeto de Valor** no tiene identidad propia; se define completamente por sus atributos y es intercambiable con otros objetos del mismo valor. Los objetos de valor son inmutables.

## ¿Qué es un Bounded Context y por qué es importante en DDD?
Un **Bounded Context** (contexto delimitado) es un límite lógico dentro del cual un modelo de dominio tiene significado y consistencia. Es importante porque permite gestionar la complejidad dividiendo el sistema en partes independientes, evitando ambigüedades y promoviendo integraciones explícitas entre contextos distintos.

## ¿Cuál es el propósito del Lenguaje Ubicuo (Ubiquitous Language) en DDD?
El **Lenguaje Ubicuo** es un lenguaje común y compartido entre desarrolladores y expertos del dominio. Su propósito es eliminar malentendidos y garantizar que el software refleje correctamente los conceptos del negocio, utilizando una terminología coherente en código, pruebas y documentación.

## ¿Qué es un Agregado (Aggregate) y cómo garantiza la consistencia en el dominio?
Un **Agregado** es un conjunto de entidades y objetos de valor que se tratan como una unidad para las actualizaciones de datos. Tiene una **raíz del agregado** que actúa como punto de entrada. Garantiza la consistencia restringiendo el acceso directo a otras partes del agregado y aplicando las reglas del negocio a través de la raíz.

## ¿Cómo se relacionan los Repositorios en DDD con la infraestructura de persistencia?
Los **Repositorios** actúan como intermediarios entre el dominio y la infraestructura de almacenamiento. Permiten acceder y almacenar Agregados sin exponer detalles de la base de datos, facilitando un diseño más limpio, desacoplado y centrado en el dominio.

## ¿Qué son los Eventos de Dominio y cómo mejoran la comunicación entre Bounded Contexts?
Los **Eventos de Dominio** son mensajes que representan algo significativo que ocurrió en el dominio. Mejoran la comunicación entre Bounded Contexts al permitir una integración desacoplada basada en la publicación y suscripción a eventos, promoviendo escalabilidad y resiliencia.

## ¿Cómo se diferencian los Servicios de Aplicación y los Servicios de Dominio en DDD?
- **Servicios de Aplicación:** coordinan casos de uso y orquestan operaciones del dominio, sin contener lógica del negocio.
- **Servicios de Dominio:** contienen lógica del negocio que no pertenece naturalmente a ninguna entidad u objeto de valor, y forman parte del modelo de dominio.

## ¿Cómo DDD facilita el diseño de software en sistemas complejos y escalables?
DDD facilita el diseño al:
- Dividir el sistema en Bounded Contexts gestionables.
- Modelar explícitamente las reglas del negocio.
- Promover un lenguaje común.
- Desacoplar las distintas capas de la aplicación.
Esto permite escalar el desarrollo y mantener una alta cohesión interna en cada parte del sistema.

## ¿Cómo se puede combinar DDD con Clean Architecture en una aplicación de microservicios?
DDD y Clean Architecture son complementarios:
- **DDD** aporta el modelado estratégico y táctico del dominio.
- **Clean Architecture** organiza el sistema en capas bien definidas (entidades, casos de uso, interfaz, infraestructura).
En microservicios, cada Bounded Context puede implementarse como un microservicio independiente siguiendo los principios de Clean Architecture, manteniendo el dominio en el núcleo de cada servicio y desacoplando detalles de infraestructura.
