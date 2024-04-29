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

El Booking Bounded Context es responsable de la gestión de la compra de boletos en la aplicación TuCine. Este contexto permite a los usuarios comprar boletos para las funciones de películas, asegurando que puedan asistir a las proyecciones seleccionadas.

## 5.4.1 Domain Layer

En la capa de dominio, las siguientes entidades juegan un papel crítico en el manejo de la lógica de negocio asociada con la reserva de entradas:


- Ticket: Representa el boleto comprado por un usuario. Incluye información sobre la fecha de emisión, la fecha de modificación, el número de asientos, el ID del usuario, el precio total, el ID de la futura película y el estado del boleto.
- Promotion: Define una promoción aplicable a la compra de boletos, con detalles como el título, la descripción, la fecha de inicio y finalización, y el porcentaje de descuento.

## 5.4.2 Interface Layer

La capa de interfaz contiene clases que interactúan directamente con los usuarios finales y otros servicios. En este contexto, incluye:

- TicketController: Maneja las solicitudes de los usuarios relacionadas con la creación, modificación y compra de boletos. Se comunica con - TicketService para realizar estas operaciones.
- PromotionController: Gestiona las promociones disponibles para los usuarios al comprar boletos. Interactúa con PromotionService para crear, modificar y eliminar promociones.
- TicketService: Define las operaciones que pueden realizarse con los boletos, como crear, modificar y aplicar promociones.
- PromotionService: Encapsula la lógica de negocio para la gestión de promociones que se aplican a la compra de boletos.

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
