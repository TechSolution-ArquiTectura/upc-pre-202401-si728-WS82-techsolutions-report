# Capítulo IV:  Strategic-Level Software Design

## 4.1 Strategic-Level Domain-Driven Design

### 4.1.1 Design Purpose

El propósito de diseño fundamental de nuestra aplicación web se centra en abordar la problemática identificada de la falta de acceso fácil y eficaz a películas no comerciales que se proyectan en cineclubes para los cinéfilos apasionados. Reconocemos que existe una audiencia ávida de cine independiente, clásico y cultural que no está siendo completamente atendida por las plataformas convencionales de streaming y exhibición. Nuestra solución está diseñada específicamente para satisfacer las necesidades de este segmento objetivo al proporcionar un medio intuitivo y eficaz para descubrir y acceder a estas películas fuera de lo común.

Al enfocarnos en conectar a los amantes del cine con experiencias cinematográficas únicas y fuera de lo común, estamos directamente abordando la problemática identificada. Reconocemos que estos cinéfilos tienen intereses y gustos que van más allá de las películas comerciales de Hollywood y desean explorar una amplia gama de opciones independientes y culturales.

Además, nuestra solución se orienta a satisfacer las necesidades del negocio al fomentar la comunidad cinéfila. Al proporcionar una plataforma donde los usuarios pueden compartir recomendaciones, críticas y detalles sobre proyecciones en cineclubes locales, estamos creando un espacio donde los cinéfilos pueden interactuar, participar activamente y contribuir al crecimiento de la comunidad. Esto no solo mejora la experiencia del usuario, sino que también aumenta la participación y la retención, lo que a su vez beneficia a nuestro negocio al consolidar nuestra posición como el destino principal para los amantes del cine independiente y cultural.

### 4.1.2 Attribute-Driven Design Inputs
| Epic / User Story ID | Título                                 | Descripción                                                                                                                                                                                                                                                   | Criterios de Aceptación                                                                                                                                                                                                                                                                                    | Relacionado con (Epic ID) |
|-----------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| US01                  | Acceso al catálogo de películas       | Los usuarios deben poder acceder al catálogo de películas disponibles en cartelera.                                                                                                                                                                         | - Escenario 1: Iniciar sesión con correo electrónico   Dado que el usuario ya se registró previamente   Cuando completa el campo “Correo electrónico” y “Contraseña” correctos y selecciona el botón “Iniciar sesión”   Entonces el sistema le muestra la interfaz principal de la aplicación. - Escenario 2: Inicio de sesión con datos incorrectos   Dado que el usuario completo los campos con datos incorrectos   Cuando selecciona el botón “Iniciar sesión”   Entonces los inputs incorrectos son enmarcados y se muestran mensajes de error por cada campo incorrecto. | -                         |
| US02                  | Búsqueda rápida de películas          | Los usuarios deben poder buscar rápida y fácilmente películas de su interés para obtener detalles, horarios y locaciones.                                                                                                                                  | - Escenario 1: Elección de usuario   Dado el usuario se encuentra en la landing page   Cuando selecciona el botón “Registrarse”   Entonces la página le dirige a pantalla elección de tipo de usuario   Y muestra los botones “Registro cinéfilo” y “Registro propietario”    Escenario 2: Registro como cinéfilo   Dado que el usuario seleccionó “Registro cinéfilo”   Y se muestra el formulario “Crear cuenta”   Cuando completa la sección “Datos personales” con los campos requeridos   Y la sección “E-mail de acceso” con los campos requeridos Y selecciona el botón “Crear cuenta”   Entonces el sistema registra la información y la redirige a la interfaz principal de la aplicación.    Escenario 3: No completa todos los campos   Dado que el usuario deja un campo vacío de alguna sección   Cuando selecciona el siguiente campo   Entonces se muestra un mensaje “Campo requerido” y se enmarca en rojo el campo vacío.    Escenario 4: Se registra con una cuenta de correo a usada   Dado que el usuario se ingresa un correo previamente registrado   Cuando selecciona “Crear cuenta”   Entonces se muestra un mensaje de error “Correo previamente registrado”. | -                         |
| US03                  | Reservar boletos en cineclubes        | Los usuarios deben poder reservar boletos para funciones en cineclubes.                                                                                                                                                                                     | - Escenario 1: Crear primer negocio   Dado el usuario ingreso a la sección “Negocios afiliados”   Y el sistema le muestra la opción de crear primer negocio   Cuando elige añadir negocio   Entonces el sistema le mostrara un formulario con la información requerida para crear el negocio     Escenario 2: Registro como propietario   Dado que el usuario seleccionó “Negocios afiliados”   Y se muestra el formulario “Aregar negocio”   Cuando completa la sección “Datos personales” con los campos requeridos   Y la sección “Datos del cineclub” con los campos requeridos   Y la sección “Perfil de cineclub” con los campos requeridos   Y la sección “E-mail de acceso” con los campos requeridos Y selecciona el botón “Crear cuenta”   Entonces el sistema registra la información y la redirige a la interfaz principal de la aplicación.     Escenario 3: Ver información básica del cineclub   Dado que estoy en la sección “cineclubs”   Cuando selecciono un cineclub específico   Entonces debería poder ver la información básica del cineclub, como el nombre, la ubicación y la descripción     Escenario 4: Ver películas en cartelera del cineclub   Dado que estoy en el perfil de un cineclub   Cuando visualizo las películas en cartelera del cineclub   Entonces debería poder ver una lista de las películas que se están proyectando actualmente en ese cineclub y sus respectivos horarios. | -                         |
| US06                  | Acceso a lista de cineclubes          | Los usuarios deben poder acceder a una lista de cineclubes disponibles.                                                                                                                                                                                     | - Los usuarios pueden ver una lista de cineclubes con información relevante.                                                                                                                                                                                                                              | -                         |
| US07                  | Búsqueda rápida de cineclubes          | Los usuarios deben poder buscar rápidamente cineclubes de su interés para obtener detalles, horarios y locaciones.                                                                                                                                       | - Escenario 1: Aplicar filtros para la búsqueda de una película   Dado que el usuario se encuentra en la sección “Películas”   Cuando aplica algún filtro disponible [“Género”,” Ordenar por”]   Y selecciona el botón “Filtrar”   Entonces la sección se actualiza y muestra las películas de acuerdo con el filtro aplicado.     Escenario 2: No se encuentra la película por el filtro aplicado   Dado que el usuario aplicó los filtros correspondientes de búsqueda   Cuando selecciona el botón “Filtrar”   Entonces la aplicación le mostrará el mensaje “No se encontraron coincidencias”. | -                         |
| US08                  | Ver perfil de un cineclub              | Los usuarios deben poder ver el perfil de un cineclub para obtener información y detalles relevantes.                                                                                                                                                       | - Escenario 01: Cinéfilo ingresa un número de tarjeta de una red de pago no admitida   Dado que el cinéfilo se encuentra en la pasarela de pagos   Cuando ingresa el dato [“número de tarjeta”]   Y este no coincida con el tipo de pago   Entonces se mostrará un error en el campo indicando el número inválido.    Escenario 02: Cinéfilo ingresa un número de tarjeta de una red de pago admitida   Dado que el cinéfilo se encuentra en la pasarela de pagos   Cuando ingresa el dato [“número de tarjeta”]   Y esta pertenezca a una red de pago válida   Entonces se mostrará un indicador en el campo que indique que es válido | -                         |
| US09                  | Modificar información de funciones en cineclubes | Los propietarios de cineclubes deben poder modificar la información de funciones y horarios para mantenerla actualizada.                                                                                                                                   | - Escenario 1: Visualizar cineclubs   Dado que el usuario se encuentra en la página por defecto “Explorar”   Cuando selecciona la opción “Cineclubes” de la barra de navegación   Entonces se muestra una fila de cards que contiene una imagen representativa del cineclub con una breve descripción   Y un paginator en la parte inferior     Escenario 


#### 4.1.2.1 Primary Funcionality (Primary User Stories)

#### 4.1.2.3 Constraints

### 4.1.3 Architectural Drivers Backlog.

### 4.1.4 Architectural Design Decisions.

### 4.1.5. Quality Attribute Scenario Refinements.

## 4.2. Strategic-Level Domain-Driven Design.

### 4.2.1 EventStorming.

### 4.2.2. Candidate Context Discovery.

### 4.2.3. Domain Message Flows Modeling.

### 4.2.4. Bounded Context Canvases.

### 4.2.5. Context Mapping.

## 4.3. Software Architecture.

### 4.3.1. Software Architecture System Landscape Diagram.

### 4.3.1. Software Architecture Context Level Diagrams.

### 4.3.2. Software Architecture Container Level Diagrams.

### 4.3.3. Software Architecture Deployment Diagrams.
 








