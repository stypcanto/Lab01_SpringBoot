# 🚀 Proyecto Spring Boot: Aplicación Web con MVC

Este proyecto es una aplicación web básica desarrollada con **Spring Boot**, siguiendo el patrón arquitectónico **MVC (Modelo-Vista-Controlador)**. Su propósito es servir como punto de partida para aprender cómo crear controladores y renderizar vistas HTML usando Thymeleaf.

## 🧠 Tecnologías Utilizadas

- Java 17
- Spring Boot
- Spring MVC
- Thymeleaf (motor de plantillas)
- Maven

## 📁 Estructura del Proyecto

```bash
src/
├── main/
│ ├── java/
│ │ └── com/stypcanto/spring/springboot_application/
│ │ ├── SpringbootApplication.java # Clase principal que arranca la aplicación
│ │ └── controllers/
│ │ └── EjemploController.java # Controlador con un endpoint de ejemplo
│ └── resources/
│ ├── application.properties # Configuraciones de la aplicación
│ ├── static/ # Archivos estáticos (CSS, JS, imágenes)
│ └── templates/
│ └── detalles_info.html # Vista que se muestra en el navegador
└── test/
└── java/com/stypcanto/spring/springboot_application/
└── SpringbootApplicationTests.java # Clase para pruebas unitarias
```


## 📌 Funcionalidad Principal

El controlador `EjemploController` maneja solicitudes HTTP GET hacia la ruta `/detalles_info`:

```java
@Controller
public class EjemploController {

    @GetMapping("/detalles_info")
    public String info() {
        return "detalles_info";
    }
}

```

## 🌐 Acceso a la Vista

Cuando accedes a `http://localhost:8080/detalles_info`, se renderiza la vista `detalles_info.html` ubicada en la carpeta `src/main/resources/templates`.

> ⚠️ **Importante**: Asegúrate de tener configurado correctamente el motor de plantillas **Thymeleaf**. Spring Boot lo incluye por defecto en proyectos web.

## ▶️ Cómo ejecutar el proyecto

1. Clona el repositorio o copia el código fuente.

2. Abre el proyecto en tu IDE favorito (como IntelliJ IDEA, Eclipse o Visual Studio Code).

3. En la raíz del proyecto, ejecuta el siguiente comando:

   ```bash
   ./mvnw spring-boot:run
    ```

4.  Abre tu navegador y visita:

 ```bash
   http://localhost:8080/detalles_info
    ```


## 🧭 ¿Qué es un Controller en Spring Boot?

En Spring Boot, un **Controller** (controlador) es una clase que se encarga de manejar las solicitudes HTTP que recibe la aplicación. Forma parte del patrón arquitectónico **MVC (Modelo - Vista - Controlador)** y actúa como intermediario entre la vista (HTML) y la lógica de negocio.

Un controlador:

- Recibe las solicitudes del usuario a través de rutas (URLs).
- Procesa la información o delega la lógica al servicio correspondiente.
- Devuelve una respuesta, que puede ser una vista HTML, un objeto JSON o un mensaje.

### 📌 Ejemplo de Controller

```java
@Controller
public class EjemploController {

    @GetMapping("/detalles_info")
    public String info() {
        return "detalles_info"; // Renderiza la vista detalles_info.html
    }
}