# 5.1 Bounded Context: Account Managment Bounded Context

## 5.1.1 Domain Layer

## 5.1.2 Interface Layer

## 5.1.3 Application Layer

## 5.1.4 Infraestructure Layer

## 5.1.6 Bounded Context Software Architecture Component Level Diagrams

## 5.1.7 Bounded Context Software Architecture Layer Class Diagrams

### 5.1.7.1 Bounded Context Domain Layer Class Diagrams

### 5.1.7.2 Bounded Context Database Design Diagram





# 5.2 Bounded Context: Cineclub Administration Bounded Context

El bounded context de administracion de cineclub es el encargado de dirigir el 
manejo del cineclub. Este bounded context será principalmente usado por el propietario
de cineclub, el cual decidirá que películas agregar o quitar de su cartelera.

## 5.2.1 Domain Layer

Las clases pertenecientes al dominio del bounded context de cineclub administration
serán las siguientes: 
<br>
- Film: Representa una película, la cual puede ser agregada o quitada de cartelera del cineclub
- Cineclub: Representa el cineclub que maneja un propietario
- CineclubType: Representa el tipo de cineclub existente , existen un total de 4 tipos de cineclubs
- ContentRating: Representa el tipo de contenido al cual es dirigido una película. Ej: +18 , +14 , etc
- Award: Representa un premio, que puede haber ganado o no una películas
- Actor: Representa un actor, que puede tener una o varias participaciones en diversas películas
- Category: Representa una categoría perteneciente a una película. Ej: Ciencia Ficción, Terror, etc

## 5.2.2 Interface Layer

Las clases pertenecientes a la capa de interfaz del bounded context de cineclub administration
serán las siguientes:
<br>
- FilmController: Controlador para los procesos relacionados con el manejo de películas
- CineclubController: Controlador para los procesos relacionados con el manejo de cineclubes o un cineclub
- CineclubTypeController: Controlador para los procesos relacionados con el manejo de los tipos de cineclubes existentes.
- ContentRatingController: Controlador para los procesos relacionados con el manejo del contenido clasificado de las películas.
- AwardController: Controlador para los premios de películas
- ActorController: Controlador para los actores que pueden estar presentes en una o varias películas
- CategoryController: Controlador para los procesos relacionados a las categorías existentes para todas las películas 

## 5.2.3 Application Layer

## 5.2.4 Infraestructure Layer

## 5.2.6 Bounded Context Software Architecture Component Level Diagrams

## 5.2.7 Bounded Context Software Architecture Layer Class Diagrams

### 5.2.7.1 Bounded Context Domain Layer Class Diagrams

### 5.2.7.2 Bounded Context Database Design Diagram



# 5.3 Bounded Context: Showtime Managment Bounded Context

## 5.3.1 Domain Layer

## 5.3.2 Interface Layer

## 5.3.3 Application Layer

## 5.3.4 Infraestructure Layer

## 5.3.6 Bounded Context Software Architecture Component Level Diagrams

## 5.3.7 Bounded Context Software Architecture Layer Class Diagrams

### 5.3.7.1 Bounded Context Domain Layer Class Diagrams

### 5.3.7.2 Bounded Context Database Design Diagram






# 5.4 Bounded Context: Booking Bounded Context

## 5.4.1 Domain Layer

## 5.4.2 Interface Layer

## 5.4.3 Application Layer

## 5.4.4 Infraestructure Layer

## 5.4.6 Bounded Context Software Architecture Component Level Diagrams

## 5.4.7 Bounded Context Software Architecture Layer Class Diagrams

### 5.4.7.1 Bounded Context Domain Layer Class Diagrams

### 5.4.7.2 Bounded Context Database Design Diagram



# 5.5 Bounded Context: Comments Bounded Context

## 5.5.1 Domain Layer

## 5.5.2 Interface Layer

## 5.5.3 Application Layer

## 5.5.4 Infraestructure Layer

## 5.5.6 Bounded Context Software Architecture Component Level Diagrams

## 5.5.7 Bounded Context Software Architecture Layer Class Diagrams

### 5.5.7.1 Bounded Context Domain Layer Class Diagrams

### 5.5.7.2 Bounded Context Database Design Diagram