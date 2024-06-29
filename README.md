Proyecto de Desarrollo de Servicios Backend

Este proyecto se centra en el desarrollo de servicios backend utilizando Java EE y Spring, con énfasis en la creación de una capa de acceso a datos, una capa de servicios y una API REST. Además, se utiliza Postman para probar el cliente de la API REST.
Objetivos

    Crear una capa de acceso a datos.
    Crear una capa de servicios.
    Crear una API REST.
    Utilizar Postman como cliente para probar la API REST.

Contenidos Teóricos

    Java EE y Spring
    Yaml
    Controladores REST
    Persistencia con DAO
    Uso de herramientas como Postman
    Arquetipos
    Basic Auth
    Proyecto multi-módulo
    DAO → *.xml y *.java
    DaoHelper
    EntityResult
    Peticiones REST
    SQL Types
    Maestros
    EntityResult (cont.)
    Manejo de múltiples servicios y DAO
    Basic Expression
    Consultas complejas
    Permisos

Tecnologías Utilizadas

    Java EE
    Spring
    Ontimize
    Postman
    Base de datos relacional (SQL)

Estructura del Proyecto

El proyecto está organizado en diferentes módulos para mantener una arquitectura limpia y modular.

css

├── api
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── proyecto
│   │   │   │           └── api
│   │   │   │               ├── interfaces
│   │   │   │               │   └── UserApi.java
│   │   │   │               └── ...
├── boot
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── proyecto
│   │   │   │           └── boot
│   │   │   │               └── Application.java
├── model
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── proyecto
│   │   │   │           └── model
│   │   │   │               ├── dao
│   │   │   │               │   ├── DaoHelper.java
│   │   │   │               │   ├── UserDao.java
│   │   │   │               │   └── ...
│   │   │   │               ├── service
│   │   │   │               │   ├── UserService.java
│   │   │   │               │   └── ...
│   │   │   │               └── resources
│   │   │   │                   └── dao
│   │   │   │                       └── UserMapper.xml
├── ws
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── proyecto
│   │   │   │           └── ws
│   │   │   │               └── controller
│   │   │   │                   ├── UserController.java
│   │   │                       └── ...
├── client
│   └── postman
│       └── ProyectoBackend.postman_collection.json
├── pom.xml
└── README.md

Descripción de los Módulos
1. API

Define las interfaces de la API REST que manejan las solicitudes HTTP y devuelven las respuestas adecuadas.

    UserApi.java: Interfaz para las operaciones relacionadas con User.

2. Boot

Contiene la clase principal que lanza la aplicación Spring.

    Application.java: Clase principal que inicia la aplicación Spring.

3. Model

Define las clases y configuraciones para el acceso a la base de datos y la lógica de negocio.

    DAO (Data Access Object):
        DaoHelper.java: Clase de ayuda para manejar las conexiones y operaciones básicas de la base de datos.
        UserDao.java: DAO para la entidad User.
        resources/dao/UserMapper.xml: Mapeo de SQL para la entidad User.

    Servicio:
        UserService.java: Servicio que contiene la lógica de negocio para la entidad User.

4. WS (Web Service)

Contiene los controladores REST que manejan las solicitudes HTTP y devuelven las respuestas adecuadas.

    UserController.java: Controlador REST para gestionar las operaciones relacionadas con User.

5. Cliente

Contiene la colección de Postman para probar la API REST.

    ProyectoBackend.postman_collection.json: Colección de Postman con las peticiones necesarias para probar la API REST.

Instrucciones de Ejecución
Configuración del Entorno

    Configurar la base de datos:
    Ejecuta los scripts SQL necesarios para crear el esquema de la base de datos y poblarla con datos iniciales.

    Configurar las dependencias de Maven:
    Asegúrate de tener configurado Maven y ejecuta el comando para descargar las dependencias:

    sh

    mvn clean install

Compilar y Ejecutar el Proyecto

    Compilar el proyecto:
    Utiliza Maven para compilar el proyecto.

    sh

mvn clean package

Ejecutar la aplicación:
Despliega la aplicación en un servidor de aplicaciones compatible con Spring, como Apache Tomcat.

sh

    mvn spring-boot:run

Probar la API REST con Postman

    Importar la colección de Postman:
    Abre Postman y importa el archivo ProyectoBackend.postman_collection.json.

    Ejecutar las peticiones:
    Utiliza las peticiones de la colección para interactuar con la API REST. Prueba diferentes endpoints y verifica las respuestas.
