# Preguntas y Respuestas sobre Spring Boot

## ¿Qué es Spring Boot y para qué sirve?
Spring Boot es un framework que simplifica la creación de aplicaciones Java basadas en Spring, ofreciendo configuración automática, servidores embebidos y una estructura predefinida para facilitar el desarrollo y despliegue rápido.

## ¿Qué hace la anotación @SpringBootApplication?
Es una anotación que combina `@Configuration`, `@EnableAutoConfiguration` y `@ComponentScan`, permitiendo configurar, escanear componentes y habilitar la configuración automática de Spring Boot en una sola anotación.

## ¿Cómo se inicia una aplicación Spring Boot?
Mediante un método `main` en la clase principal con `SpringApplication.run(NombreClase.class, args)`.

## ¿Qué función tiene la anotación @RestController?
Indica que la clase es un controlador REST que maneja peticiones HTTP y devuelve directamente el resultado como JSON o texto plano.

## ¿Cómo defines una URL en un controlador de Spring Boot?
Usando anotaciones como `@GetMapping`, `@PostMapping`, `@PutMapping` o `@DeleteMapping`, especificando la ruta como parámetro.

## ¿Cuál es el puerto por defecto en el que corre Spring Boot?
El puerto por defecto es el **8080**.

## ¿Cómo cambias el puerto de la aplicación?
Editando el archivo `application.properties` y agregando:  
`server.port=PUERTO_DESEADO`

## ¿Qué comando de Maven permite ejecutar una aplicación Spring Boot?
`mvn spring-boot:run`

## ¿Cómo puedes probar un endpoint de Spring Boot en el navegador?
Ingresando la URL correspondiente al endpoint, por ejemplo:  
`http://localhost:8080/mi-endpoint`

## ¿Para qué sirve el archivo application.properties?
Para configurar parámetros de la aplicación como el puerto del servidor, rutas de base de datos, credenciales, perfiles activos, entre otros.
