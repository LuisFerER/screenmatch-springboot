# 🎬 Screenmatch

**Screenmatch** es una aplicación de consola desarrollada con Spring Boot que permite buscar, filtrar y listar series y episodios utilizando datos obtenidos de la [OMDb API](https://www.omdbapi.com/). El proyecto forma parte del aprendizaje de tecnologías Java en el contexto de un curso de Alura Latam.

---

## 🧰 Tecnologías utilizadas

- Java 17
- Spring Boot 3.2.0
- Spring Data JPA
- JPQL
- PostgreSQL
- Maven
- Lambdas y Streams
- Jackson
- OpenAI GPT-3 Java SDK (para lógica complementaria)

---

## 🖥️ Menú de opciones en consola

Al ejecutar el proyecto, se muestra un menú interactivo en consola con las siguientes opciones:

```
1 - Buscar series
2 - Buscar episodios
3 - Mostrar series buscadas
4 - Buscar Series por título
5 - Top 5 mejores series
6 - Buscar Series por categoría
7 - Filtrar series
8 - Buscar episodios por título
9 - Top 5 episodios por serie

0 - Salir


## 🚀 Ejecución del proyecto

### Requisitos previos

- Java 17+
- PostgreSQL instalado y corriendo
- API Key de OMDb ([Solicítala aquí](https://www.omdbapi.com/apikey.aspx))
- IntelliJ IDEA (opcional)

### Configuración

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/screenmatch.git
   cd screenmatch
   ```

2. Configura tu archivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/screenmatch
   spring.datasource.username=tu_usuario
   spring.datasource.password=tu_contraseña
   omdbapi.apikey=TU_API_KEY
   ```

3. Ejecuta el proyecto desde tu IDE o por terminal con Maven:
   ```bash
   ./mvnw spring-boot:run
   ```

---

## 📁 Estructura del proyecto

```
src/
 └── main/
      ├── java/
      │   └── com.aluracursos.screenmatch/
      │        ├── model/           # Entidades y DTOs
      │        ├── repository/      # Interfaces de persistencia (JPA)
      │        ├── service/         # Lógica de negocio y consumo de API
      │        ├── principal/       # Clase Principal para menú interactivo
      │        └── ScreenmatchApplication.java
      └── resources/
           └── application.properties
```

---

## 🌐 API Externa

El proyecto consume información de la **OMDb API**, la cual provee datos sobre películas y series mediante peticiones HTTP.

- URL base: `https://www.omdbapi.com/`

---

## ❤️ Agradecimientos

Este proyecto fue realizado como parte del programa de formación en Java con **Alura Latam** y **Oracle Next Education (ONE)**.

> **Gracias al equipo de Alura Latam y Oracle por esta gran oportunidad de aprendizaje.**

---

## 📜 Licencia

Este proyecto está desarrollado con fines educativos. Actualmente no posee una licencia definida.
