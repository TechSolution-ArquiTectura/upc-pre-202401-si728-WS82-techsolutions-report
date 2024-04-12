# Capítulo IV:  Strategic-Level Software Design

## 4.1 Strategic-Level Domain-Driven Design

### 4.1.1 Design Purpose

El propósito de diseño fundamental de nuestra aplicación web se centra en abordar la problemática identificada de la falta de acceso fácil y eficaz a películas no comerciales que se proyectan en cineclubes para los cinéfilos apasionados. Reconocemos que existe una audiencia ávida de cine independiente, clásico y cultural que no está siendo completamente atendida por las plataformas convencionales de streaming y exhibición. Nuestra solución está diseñada específicamente para satisfacer las necesidades de este segmento objetivo al proporcionar un medio intuitivo y eficaz para descubrir y acceder a estas películas fuera de lo común.

Al enfocarnos en conectar a los amantes del cine con experiencias cinematográficas únicas y fuera de lo común, estamos directamente abordando la problemática identificada. Reconocemos que estos cinéfilos tienen intereses y gustos que van más allá de las películas comerciales de Hollywood y desean explorar una amplia gama de opciones independientes y culturales.

Además, nuestra solución se orienta a satisfacer las necesidades del negocio al fomentar la comunidad cinéfila. Al proporcionar una plataforma donde los usuarios pueden compartir recomendaciones, críticas y detalles sobre proyecciones en cineclubes locales, estamos creando un espacio donde los cinéfilos pueden interactuar, participar activamente y contribuir al crecimiento de la comunidad. Esto no solo mejora la experiencia del usuario, sino que también aumenta la participación y la retención, lo que a su vez beneficia a nuestro negocio al consolidar nuestra posición como el destino principal para los amantes del cine independiente y cultural.

### 4.1.2 Attribute-Driven Design Inputs

#### 4.1.2.1 Primary Funcionality (Primary User Stories)

| Epic / User Story ID | Título                                      | Descripción                                                                                                                                               | Criterios de Aceptación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Relacionado con (Epic ID) |
|----------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| US01                 | Acceso al catálogo de películas            | Los usuarios deben poder acceder al catálogo de películas disponibles en cartelera.                                                                     | **Escenario 1:** Visualizar películas en cartelera: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Películas” de la barra de navegación Entonces se muestra una fila de cards que contiene el poster promocional de la película Y un paginator en la parte inferior. **Escenario 2:** No se encuentran películas en cartelera: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Películas” de la barra de navegación Entonces se muestra en la pantalla el mensaje “Por el momento no tenemos películas en cartelera” | Epic 4: Exploración de Contenido y Comunidad |
| US02                 | Búsqueda rápida de películas               | Los usuarios deben poder buscar rápida y fácilmente películas de su interés para obtener detalles, horarios y locaciones.                              | **Escenario 1:** Aplicar filtros para la búsqueda de una película: Dado que el usuario se encuentra en la sección “Películas” Cuando aplica algún filtro disponible [“Género”,” Ordenar por”] Y selecciona el botón “Filtrar” Entonces la sección se actualiza y muestra las películas de acuerdo con el filtro aplicado. **Escenario 2:** No se encuentra la película por el filtro aplicado: Dado que el usuario aplicó los filtros correspondientes de búsqueda Cuando selecciona el botón “Filtrar” Entonces la aplicación le mostrará el mensaje “No se encontraron coincidencias” **Escenario 3:** Búsqueda de película por título: Dado que el usuario se encuentra en la sección “Películas” Cuando ingresa las primeras palabras de la película en el buscador Y presiona “enter” Entonces la aplicación le mostrará las películas coincidentes con el texto ingresado **Escenario 4:** No se encuentra la película por el título ingresado: Dado que el usuario ingresa el nombre de la película Cuando selecciona “enter” Entonces la aplicación le mostrará el mensaje “No se encontraron coincidencias” | Epic 4: Exploración de Contenido y Comunidad |
| US03                 | Reservar boletos en cineclubes            | Los usuarios deben poder reservar boletos para funciones en cineclubes.                                                                                 | **Escenario 01:** Reservar un boleto exitosamente: Dado que soy un cinéfilo registrado Y hay una película que quiero ver en un cineclub Cuando selecciono la película de la sección “Películas” Y la función de la tabla de opciones Entonces debería poder reservar un boleto exitosamente **Escenario 02:** Ver información de la película y funciones disponibles: Dado que estoy en la página de reservas de un cineclub Cuando selecciono una película y una función específica Entonces debería poder ver la información de la película, como el título, sinopsis y cast. Y debería poder ver la información de la función, como la fecha, la hora y el cineclub en el que se proyectará. **Escenario 03:** Reservar un boleto exitosamente: Dado que soy un cinéfilo registrado en la plataforma Y existe una película que deseo ver en un cineclub disponible Cuando selecciono la película deseada desde la sección "Películas" Y elijo la función específica de la tabla de opciones Entonces debería ser capaz de realizar una reserva exitosa de un boleto para esa función en particular Y recibir una confirmación de la reserva, indicando el número de boletos y los detalles de la función. | Epic 2: Administración y Reserva de datos    |
| US06                 | Acceso a lista de cineclubes              | Los usuarios deben poder acceder a una lista de cineclubes disponibles.                                                                                 | **Escenario 1:** Visualizar Cineclubes disponibles: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Cineclubs” de la barra de navegación Entonces se muestra una fila de cards que contiene el poster promocional de la los cineclubs Y un paginator en la parte inferior. **Escenario 2:** No se encuentran cineclub en la plataforma: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Cineclubs” de la barra de navegación Entonces se muestra en la pantalla el mensaje “Por el momento no tenemos el Cineclub en la plataforma” | Epic 4: Exploración de Contenido y Comunidad |
| US07                 | Búsqueda rápida de cineclubes             | Los usuarios deben poder buscar rápidamente cineclubes de su interés para obtener detalles, horarios y locaciones.                                      | **Escenario 1:** Aplicar filtros para la búsqueda de una película: Dado que el usuario se encuentra en la sección “Cineclubs” Cuando aplica algún filtro disponible [“Categoría”,” Ordenar por”, “Distritos”] Y selecciona el botón “Filtrar” Entonces la sección se actualiza y muestra los cineclubes de acuerdo con el filtro aplicado. **Escenario 2:** Búsqueda de cineclub por título: Dado que el usuario se encuentra en la sección “Cineclubs” Cuando ingresa las primeras palabras de la película en el buscador Y presiona “enter” Entonces la aplicación le mostrará los cineclubs coincidentes con el texto ingresado | Epic 4: Exploración de Contenido y Comunidad |
| US08                 | Ver perfil de un cineclub                 | Los usuarios deben poder ver el perfil de un cineclub para obtener información y detalles relevantes.                                                     | **Escenario 1:** Visualizar perfil del cineclub escogido: Dado que el usuario se encuentra en la sección Predeterminado “Explorar” Cuando seleccione a la opción de “Cineclubs” Y selecciona un cineclub Entonces se mostrará el perfil del cineclub en el cual le brindará su información. | Epic 4: Exploración de Contenido y Comunidad |
| US09                 | Modificar información de funciones en cineclubes | Los propietarios de cineclubes deben poder modificar la información de funciones y horarios para mantenerla actualizada.                     | **Escenario 1:** Modificación de Horario de Proyección: Dado que soy el propietario del cineclub y estoy autenticado en la aplicación web. Cuando accedo a la sección de "Programación" y selecciono una función existente. Entonces el sistema me muestra los detalles de la función, incluido el horario de proyección. **Escenario 2:** Cambio de Horario de Proyección: Dado que estoy viendo los detalles de una función. Cuando ajusto el horario de proyección y confirmo los cambios. Entonces el sistema actualiza el horario en la base de datos y me muestra un mensaje de confirmación. **Escenario 3:** Actualización de Información de Película: Dado que estoy viendo los detalles de una función. Cuando modifico los detalles de la película, como el título, género, director, etc. Entonces el sistema actualiza la información en la base de datos y muestra un mensaje de confirmación. **Escenario 4:** Cambio de Sala de Proyección: Dado que estoy viendo los detalles de una función. Cuando selecciono una sala de proyección diferente para la función. Entonces el sistema actualiza la asignación de sala en la base de datos y me muestra un mensaje de confirmación. **Escenario 5:** Agregar Nueva Función: Dado que soy el propietario del cineclub y estoy autenticado en la aplicación web. Cuando accedo a la sección de "Programación" y elijo "Agregar Nueva Función". Entonces el sistema me permite ingresar los detalles de la película y el horario de proyección. **Escenario 6:** Cancelar Modificaciones: Dado que estoy viendo los detalles de una función y realizando cambios. Si decido cancelar los cambios en cualquier momento antes de confirmar. Entonces el sistema me muestra un mensaje de confirmación para asegurarse de que deseo cancelar y no se aplican las modificaciones. **Escenario 7:** Horario en Conflicto: Dado que estoy modificando el horario de proyección de una función. Si el nuevo horario coincide con otro evento o función en la misma sala. Entonces el sistema me muestra un mensaje de error indicando que el horario está en conflicto y sugiere elegir otro horario. **Escenario 8:** Error en la Actualización: Dado que estoy realizando cambios en los detalles de una función. Si ocurre un error en la actualización de la base de datos debido a problemas técnicos. Entonces el sistema muestra un mensaje de error y recomienda intentarlo nuevamente o ponerse en contacto con el soporte técnico. | Epic 3: Registro y Gestión de Cineclubs |
| US10                 | Ver promociones de cineclubes             | Los usuarios deben poder ver las promociones ofrecidas por los cineclubes para obtener descuentos y beneficios.                                         | **Escenario 1:** Visualizar promociones en cartelera: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Películas” de la barra de navegación Entonces se muestra una fila de cards que muestra las promociones en la plataforma Y un paginator en la parte inferior. **Escenario 2:** No se encuentran películas en cartelera: Dado que el usuario se encuentra en la página por defecto “Explorar” Cuando selecciona la opción “Promociones” de la barra de navegación Entonces se muestra en la pantalla el mensaje “Por el momento no tenemos Promociones en cartelera” | Epic 4: Exploración de Contenido y Comunidad |
| US11                 | Crear y administrar promociones           | Los propietarios de cineclubes deben poder crear y administrar promociones y descuentos para atraer a más público.                                     | **Escenario 1:** Creación de una Nueva Promoción: Dado que soy el propietario del cineclub y estoy autenticado en la aplicación web. Cuando accedo a la sección de "Promociones y Descuentos". Entonces el sistema muestra la lista actual de promociones y opciones para agregar una nueva promoción. **Escenario 2:** Agregar Detalles de la Promoción: Dado que estoy creando una nueva promoción. Cuando ingreso los detalles como el nombre, descripción y el tipo de descuento (porcentaje o monto fijo). Entonces el sistema me permite avanzar al siguiente paso para definir las condiciones de la promoción. **Escenario 3:** Definir Condiciones de la Promoción: Dado que estoy creando una nueva promoción. Cuando elijo las condiciones que activarán la promoción, como seleccionar películas específicas, fechas y horarios. Entonces el sistema valida las condiciones y me permite continuar. | Epic 5: Administración de Promociones |
| US12                 | Pagar boleto con diversas opciones de pago | Los usuarios podrán pagar los boletos reservados con diferentes métodos de pago (tarjetas, criptomonedas) mediante la aplicación.                        | **Escenario 01:** Cinéfilo ingresa un número de tarjeta de una red de pago admitida: Dado que el cinéfilo se encuentra en la pasarela de pagos Cuando ingresa el dato [“número de tarjeta”] Y esta pertenezca a una red de pago válida Entonces se mostrará un indicador en el campo que indique que es válido. **Escenario 02:** Cinéfilo ingresa datos admitidos para la tarjeta seleccionada: Dado que el cinéfilo se encuentra en la pasarela de pagos E ingresa una tarjeta válida Cuando ingresa los datos [“datos del titular”, “CCV”, “código postal”, “email”] Y sean correctos Entonces el sistema enviará la información para procesar el pago. **Escenario 03:** Cinéfilo no cuenta con fondos para la transacción: Dado que el cinéfilo ingresó los datos correctos de su tarjeta Cuando el sistema procese el pago Y no cuente con fondos suficientes Entonces retorna a la pantalla un error indicando que ocurrió un error durante la transacción **Escenario 04:** Cinéfilo cuenta con fondos para la transacción: Dado que el cinéfilo ingresó los datos correctos de su tarjeta Cuando el sistema procese el pago Y cuente con fondos suficientes Entonces retorna a la pantalla un mensaje indicando que se procesó la compra correctamente Y se envía al email un mensaje con el boleto. **Escenario 05:** Cinéfilo elige pagar con criptomonedas usando MetaMask: Dado que el cinéfilo se encuentra en la pasarela de pagos Cuando selecciona la opción de pago con criptomonedas Entonces se le solicitará que conecte su cartera MetaMask al sitio web. **Escenario 06:** Cinéfilo no tiene MetaMask instalado o su sesión no está iniciada: Dado que el cinéfilo seleccionó pagar con criptomonedas Cuando no tiene MetaMask instalado o su sesión no está activa Entonces se le mostrará un mensaje solicitando la instalación de MetaMask o iniciar sesión. **Escenario 07:** Cinéfilo tiene MetaMask instalado y selecciona su cartera: Dado que el cinéfilo tiene MetaMask instalado y su sesión iniciada Cuando selecciona su cartera y confirma el monto a pagar Entonces el sistema enviará la transacción a la blockchain para su procesamiento. **Escenario 08:** La transacción de criptomonedas es exitosa: Dado que el cinéfilo realizó el pago con criptomonedas Cuando la transacción es confirmada en la blockchain Entonces se mostrará un mensaje de éxito y se enviará el boleto al email del cinéfilo. **Escenario 09:** La transacción de criptomonedas falla: Dado que el cinéfilo realizó el pago con criptomonedas Cuando la transacción no se puede completar (por falta de fondos, error en la red, etc.) Entonces se mostrará un mensaje de error y se le ofrecerá la opción de intentar de nuevo o elegir otro método de pago. | Epic 2: Administración y Reserva de entradas |


### 4.1.2.2 Quality attribute Scenarios

| Atributo      | Fuente                      | Estímulo                                                       | Artefacto                 | Entorno            | Respuesta                                                                 | Medida                                                                                                              |
|---------------|-----------------------------|----------------------------------------------------------------|---------------------------|--------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Usabilidad    | Usuario                     | Realizar una búsqueda de películas                             | Sistema de búsqueda       | Web                | El sistema presenta resultados relevantes y fácilmente navegables         | Tiempo promedio de búsqueda, tasa de éxito en la búsqueda, satisfacción del usuario                               |
| Disponibilidad | Usuario / Sistema externo   | Intento de reservar un boleto                                  | Sistema de reservas / Web / API externa | Web                | El sistema procesa la reserva sin errores                                | Porcentaje de reservas exitosas, tiempo medio de respuesta del sistema                                               |
| Rendimiento   | Usuario                     | Acceder al catálogo de películas                               | Servidor de la aplicación | Web                | El catálogo se carga rápidamente, independientemente de la cantidad de películas | Tiempo de carga de la página, tiempo de respuesta del servidor                                                      |
| Seguridad     | Usuario                     | Iniciar sesión en la plataforma                                | Sistema de autenticación  | Web                | El sistema verifica con éxito las credenciales del usuario y protege la información confidencial | Porcentaje de autenticaciones exitosas, tasa de detección de intentos de intrusión                                  |
| Fiabilidad    | Usuario / Sistema externo   | Realizar una reserva de boletos                                | Sistema de reservas / Web / Servidor de pagos | Web / Servidor de pagos | El sistema completa la reserva sin fallas y procesa el pago correctamente    | Porcentaje de reservas completadas sin errores, tasa de éxito en el procesamiento de pagos                         |
| Escalabilidad | Sistema interno             | Alta demanda para pagar boletos                                | Servidores de la aplicación / Web/Servidor de pagos | Web/Servidor de pagos | El sistema maneja de manera eficiente y efectiva el aumento de pagos repentino en el tráfico de usuarios | Tiempo de respuesta del servidor bajo cargas pesadas, capacidad para escalar horizontalmente                      |


#### 4.1.2.3 Constraints

| Technical Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
|--------------------|--------|-------------|--------------------------|---------------------------|
| E001               | Iniciar Sesión | COMO cinéfilo /propietario QUIERO iniciar sesión en la aplicación PARA acceder a sus beneficios | Ver descripción en las user stories | Epic 1: Gestión de Cuentas y Accesos (E001) |
| E002               | Pagar boleto reservado en pasarela con diversas opciones de pago | COMO cinéfilo QUIERO pagar por los boletos de una función reservada PARA verla en el cineclub donde se proyecta. | Ver descripción en las user stories | Epic 2: Administración y Reserva de Entradas (E002) |
| E003               | Afiliar un cineclub | COMO propietario QUIERO crear una cuenta en la aplicación PARA acceder a sus beneficios | Ver descripción en las user stories | Epic 3: Registro y Gestión de Cineclubes (E003) |
| E004               | Ver películas en cartelera | COMO cinéfilo QUIERO acceder al catálogo de películas en cartelera PARA ver si existe alguna de mi interés | Ver descripción en las user stories | Epic 4: Exploración de Contenido y Comunidad (E004) |
| E005               | Administrar promociones y descuentos | COMO propietario de un cineclub QUIERO crear y administrar promociones y descuentos PARA atraer a más público y aumentar las ventas | Ver descripción en las user stories | Epic 5: Administración de Promociones (E005) |
| E006               | Administrar perfil de cineclub | COMO propietario QUIERO tener la opción de gestionar una cuenta de negocio afiliada a mi cuenta propietario PARA manejar y alterar datos de mi cuenta negocio | Ver descripción en las user stories | Epic 6: Gestión de Perfiles de Usuario (E006) |


### 4.1.3 Architectural Drivers Backlog.

| Driver ID | Título de Driver | Descripción | Importancia para Stakeholders | Impacto en Architecture Technical Complexity |
|-----------|-------------------|-------------|-------------------------------|---------------------------------------------|
| AD001     | Seguridad         | Garantizar la seguridad de los datos de los usuarios y transacciones financieras. | Alta                          | Alta                                        |
| AD002     | Escalabilidad     | Permitir que el sistema pueda manejar un crecimiento en el número de usuarios y transacciones sin degradación del rendimiento. | Alta                          | Alta                                        |
| AD003     | Fiabilidad        | Asegurar que el sistema sea confiable y esté disponible en todo momento. | Alta                          | Alta                                        |
| AD004     | Mantenibilidad   | Facilitar el mantenimiento y la evolución del sistema a lo largo del tiempo. | Alta                          | Media                                       |
| AD005     | Usabilidad       | Garantizar una experiencia de usuario intuitiva y satisfactoria. | Alta                          | Baja                                        |
| AD006     | Interoperabilidad | Permitir la integración con otros sistemas y servicios externos. | Media                         | Alta                                        |

### 4.1.4 Architectural Design Decisions.

| Driver ID | Título de Driver | Pattern 1        | Pattern 2         | Pattern 3        |
|-----------|-------------------|------------------|-------------------|------------------|
| AD001     | Seguridad         | Capas de seguridad | Autenticación multifactor | Encriptación de extremo a extremo | 
|           |                   | Pro: Proporciona defensa en profundidad. | Pro: Aumenta la seguridad al requerir múltiples formas de autenticación. | Pro: Protege los datos durante toda su transmisión y almacenamiento. |
|           |                   | Con: Puede aumentar la complejidad del sistema. | Con: Puede ser percibido como una barrera para los usuarios. | Con: Puede ralentizar la velocidad de transferencia de datos. |
| AD002     | Escalabilidad     | Escalamiento vertical | Escalamiento horizontal | Escalamiento elástico |
|           |                   | Pro: Aumenta la capacidad de procesamiento de cada nodo. | Pro: Distribuye la carga de trabajo entre múltiples servidores. | Pro: Permite adaptarse a picos de demanda al agregar o eliminar recursos automáticamente. |
|           |                   | Con: Limitado por la capacidad de hardware. | Con: Requiere una gestión cuidadosa para mantener la coherencia de los datos. | Con: Puede resultar en costos imprevistos si no se configura correctamente. |
| AD003     | Fiabilidad        | Detección y recuperación de fallos | Redundancia de datos | Gestión de transacciones atómicas |
|           |                   | Pro: Minimiza el tiempo de inactividad detectando y corrigiendo automáticamente los fallos. | Pro: Asegura la disponibilidad de los datos incluso en caso de fallo de un dispositivo. | Pro: Garantiza que las operaciones complejas se completen en su totalidad o no se realicen en absoluto. |
|           |                   | Con: Puede aumentar la complejidad de la lógica de negocio. | Con: Requiere más almacenamiento y recursos de red. | Con: Puede aumentar el tiempo de respuesta de las transacciones. |
| AD004     | Mantenibilidad    | Arquitectura basada en microservicios | Modularidad | Versionado de API |
|           |                   | Pro: Facilita la actualización y mantenimiento de componentes individuales. | Pro: Permite el desarrollo y mantenimiento independiente de cada módulo. | Pro: Proporciona una forma controlada de introducir cambios en la interfaz de programación de aplicaciones. |
|           |                   | Con: Aumenta la complejidad de la gestión de múltiples servicios. | Con: Puede haber una sobrecarga de comunicación entre módulos. | Con: Requiere una estrategia de migración cuidadosamente planificada para evitar la ruptura de la compatibilidad. |
| AD005     | Usabilidad        | Diseño centrado en el usuario | Pruebas de usabilidad | Retroalimentación del usuario |
|           |                   | Pro: Mejora la experiencia del usuario al centrarse en sus necesidades y expectativas. | Pro: Identifica problemas de usabilidad temprano en el proceso de desarrollo. | Pro: Permite ajustar el diseño según las preferencias y comentarios de los usuarios. |
|           |                   | Con: Puede llevar más tiempo y recursos dedicados a la investigación de usuarios. | Con: Requiere la participación activa de usuarios reales, lo que puede ser difícil de coordinar. | Con: Las opiniones de los usuarios pueden ser subjetivas y variadas. |
| AD006     | Interoperabilidad | Uso de estándares abiertos | Implementación de APIs RESTful | Uso de formatos de datos comunes |
|           |                   | Pro: Facilita la integración con sistemas de terceros al seguir normas ampliamente aceptadas. | Pro: Permite una comunicación flexible y eficiente entre sistemas heterogéneos. | Pro: Simplifica el intercambio de datos al utilizar formatos conocidos y compatibles. |
|           |                   | Con: Puede limitar las opciones de tecnología y proveedores. | Con: Requiere una cuidadosa documentación y gestión de las APIs. | Con: La adopción de estándares puede llevar tiempo y esfuerzo adicional en la implementación. |

### 4.1.5 Quality Attribute Scenario Refinements

| Scenario Refinement for Scenario 1 |                                                                                                                                                                     |                                                                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Scenarios(s)                       | Garantizar la seguridad de los datos de los usuarios y transacciones financieras.                                                                                   |                                                                                                                                 | 
| Bussiness Goals:                   | Asegurar la integridad y confidencialidad de la información del usuario y las transacciones financieras.                                                            |                                                                                                                                 |
| Relevant Quality Attribute:        | Seguridad                                                                                                                                                           |                                                                                                                                 |
|                                    | Stimulus                                                                                                                                                            | Intento de acceso no autorizado a los datos del usuario o transacciones financieras.                                            |
|                                    | Stimulus source                                                                                                                                                     | Usuarios malintencionados, errores de configuración, intentos de hackeo.                                                        |
| Scenario                           | Enviroment                                                                                                                                                          | Sistema en producción, red abierta, potencialmente no confiable.                                                                |
| Components                         | Artifact                                                                                                                                                            | Sistema de autenticación, bases de datos de usuarios y transacciones, redes seguras.                                            |
|                                    | Response                                                                                                                                                            | Denegar el acceso, enviar alertas, registrar el intento de acceso no autorizado.                                                |
|                                    | Response measure                                                                                                                                                    | Tiempo de respuesta para bloquear el acceso no autorizado, precisión en la detección de amenazas, número de alertas enviadas.   |
| Questions:                         | ¿Cómo podemos asegurar que el sistema responda rápidamente a los intentos de acceso no autorizado? ¿Qué nivel de precisión necesitamos en la detección de amenazas? |                                                                                                                                 |
| Issues                             | Gestión de falsos positivos, necesidad de actualizaciones continuas de seguridad, cumplimiento de regulaciones de privacidad y seguridad.                           |                                                                                                                                 |

| Scenario Refinement for Scenario 2 |                                                                                                                                                                                                           |                                                                                                                    |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Scenarios(s)                       | Permitir que el sistema pueda manejar un crecimiento en el número de usuarios y transacciones sin degradación del rendimiento.                                                                            |                                                                                                                    | 
| Bussiness Goals:                   | Garantizar que el sistema pueda escalar para satisfacer las demandas crecientes de los usuarios y las transacciones.                                                                                      |                                                                                                                    |
| Relevant Quality Attribute:        | Escalabilidad                                                                                                                                                                                             |                                                                                                                    |
|                                    | Stimulus                                                                                                                                                                                                  | Aumento repentino en el número de usuarios concurrentes o transacciones.                                           |
|                                    | Stimulus source                                                                                                                                                                                           | Aumento en la popularidad del servicio, campañas de marketing exitosas, eventos especiales.                        |
| Scenario                           | Enviroment                                                                                                                                                                                                | Aumento en la carga del sistema, picos de tráfico, recursos de hardware limitados.                                 |
| Components                         | Artifact                                                                                                                                                                                                  | Servidores, bases de datos, equilibrio de carga.                                                                   |
|                                    | Response                                                                                                                                                                                                  | Escalar horizontal o verticalmente, redistribuir la carga, implementar cachés.                                     |
|                                    | Response measure                                                                                                                                                                                          | Tiempo de respuesta del sistema, capacidad para manejar picos de tráfico, eficiencia en la distribución de carga.  |
| Questions:                         | ¿Cómo podemos garantizar que el sistema pueda escalar de manera rentable y eficiente? ¿Cuál es el límite máximo de usuarios y transacciones que el sistema puede manejar sin degradación del rendimiento? |                                                                                                                    |
| Issues                             | Gestión de la infraestructura de escalabilidad, costos asociados con el escalado, mantenimiento de la coherencia de los datos en entornos distribuidos. .                                                 |                                                                                                                    |




## 4.2  Strategic-Level Attribute-Driven Design

### 4.2.1 EventStorming

En la fase de Event Storming, el equipo de "TuCine" aplicó un análisis  de los eventos del dominio para diseccionar y entender la operatividad del proyecto. Esta técnica visual y colaborativa facilitó la identificación de eventos críticos, comandos y políticas, resultando en un modelo comprensivo del negocio. El ejercicio fue esencial no solo para mapear el flujo de la aplicación, sino también para alinear las capacidades técnicas con los requerimientos empresariales y las expectativas de los usuarios.

**Paso 1: Domain Events**

![Domain Events](Resources/event_storming/Domain_Events.jpg)

**Paso 2: TimeLine**
 
![Time Line](Resources/event_storming/Time_Line.jpg)

**Paso 3: Pain Points**
 
![Pain Points](Resources/event_storming/Pain_Points.jpg)

**Paso 4: Pivotal Points**
 
![Pivotal Points](Resources/event_storming/Pivotal_Points.jpg)

**Paso 5: Commands**

![Commands](Resources/event_storming/Commands.jpg)

**Paso 6: Policies**

![Policies](Resources/event_storming/Policies.jpg)

**Paso 7: Read Models**
 
![Read Models](Resources/event_storming/Read_Models.jpg)

**Paso 8: External Systems**

![External Systems](Resources/event_storming/External_Systems.jpg)

**Paso 9: Aggregates**

![Aggregates](Resources/event_storming/Aggregates.jpg)

**Paso 10: Bounded Contexts**

![Bounded Contexts](Resources/event_storming/Bounded_Contexts.jpg)

### 4.2.2. Candidate Context Discovery

**Start-with-Value**
Se identificó las partes centrales del dominio que aportan el mayor valor al negocio. Este enfoque permitió priorizar los aspectos críticos de la aplicación "TuCine", enfocándonos en la distribución y promoción de películas de nicho. Se identificaron eventos clave como "Película añadida", "Reserva realizada" y "Comentario publicado", que son esenciales para la experiencia del usuario y la proposición de valor del negocio.

![Domain Events](Resources/event_storming/Domain_Events.jpg)

**Start-with-Simple**
Se crearon modelos simples pero funcionales, descomponiendo el timeline en pasos secuenciales claros. Esta técnica ayudó a visualizar el flujo de eventos desde la búsqueda de una película hasta la realización de una reserva. Al simplificar el modelo, se pudo identificar claramente las interacciones entre los usuarios, cineclubes, y la plataforma, facilitando la definición de límites para cada bounded context.

**Look-for-Pivotal-Events**
Se identificaron eventos pivotales que indicaran cambios de estado significativos en el proceso de negocio, como “Usuario registrado”, “Película añadida”, "Compra confirmada" o "Comentario publicado". Estos eventos marcan transiciones importantes que pueden definir los límites de diferentes contexts, ayudando a separar las funcionalidades de administración de reservas y gestión de comentarios/opiniones en contexts distintos.

![Pivotal Points](Resources/event_storming/Pivotal_Points.jpg)

**Bounded Contexts Definidos**

El equipo logró distinguir varios bounded contexts que encapsulan funcionalidades específicas dentro del sistema "TuCine". Estos contexts se identificaron con base en eventos de dominio, comandos, políticas y agregados que comparten cohesión y operan bajo un conjunto común de reglas y políticas. Los bounded contexts identificados a partir de la sesión son los siguientes:

***Gestión de Cuentas:*** Este contexto abarca toda la funcionalidad relacionada con la administración de cuentas de usuario, incluyendo la creación, edición y cancelación de cuentas, así como la autenticación y el manejo de credenciales.

***Administración Cineclub:*** En este contexto, se concentran las operaciones relacionadas con la gestión de cineclubes, desde la creación de un cineclub, pasando por la administración de sus funciones, hasta la actualización de la información relacionada con las películas y eventos especiales.

***Reservas y Compras***: Se refiere al conjunto de procesos y decisiones que giran en torno a la compra de boletos y las reservas. Incluye la selección de asientos, el proceso de pago y la validación de transacciones, así como la gestión de promociones y descuentos.

***Comentarios de Cinéfilos:*** Este contexto encapsula la interacción social de la plataforma, donde los usuarios pueden crear y compartir reseñas y comentarios, lo que fomenta la discusión y participación de la comunidad.

***Administración de Funciones de Películas:*** Este contexto se ocupa de la programación y administración de las funciones de películas, incluyendo la creación de nuevos horarios, la modificación de funciones existentes y la eliminación de funciones pasadas.

### 4.2.3. Domain Message Flows Modeling

Los Domain Message Flows en "TuCine" ilustran cómo los mensajes se transmiten entre los bounded contexts. Identifican los comandos que inician acciones, los eventos que representan resultados y las consultas que fluyen a través del sistema, asegurando una integración cohesiva y funcionalidades bien definidas dentro de la aplicación.


![Domain Message Flows Step1](Resources/domain_message_flows/Domain_Message_Flows_Step1.jpg)

![Domain Message Flows Step2](Resources/domain_message_flows/Domain_Message_Flows_Step2.jpg)

![Domain Message Flows Step3](Resources/domain_message_flows/Domain_Message_Flows_Step3.jpg)

### 4.2.4. Bounded Context Canvases

**Gestión de Cuentas**

![Account Management](Resources/bounded_context_canvas/Account_Management.jpg)

**Administración Cineclub**

![Cineclub Management](Resources/bounded_context_canvas/Cineclub_Management.jpg)

**Reservas y Compras**

![Reservations and Purchases](Resources/bounded_context_canvas/Reservations_Purchases.jpg)

**Comentarios de Cinéfilos**

![Comments](Resources/bounded_context_canvas/Comments.jpg)

**Administración de Funciones de Películas**

![Showtimes Management](Resources/bounded_context_canvas/Showtimes_Management.jpg)

### 4.2.5. Context Mapping

**Proceso de Elaboración de Context Maps**

 La elaboración de context maps para visualizar y analizar las relaciones estructurales entre los bounded contexts identificados en el proyecto "TuCine". Este proceso implicó un examen de la información recolectada durante la sesión de EventStorming, y la utilización de la misma para generar diseños candidatos de context mapping.

Para explorar las dinámicas y dependencias entre los bounded contexts, el equipo se planteó una serie de preguntas críticas que permitieron evaluar las consecuencias de diversas reestructuraciones del modelo de dominio. Estas preguntas guiaron las decisiones arquitectónicas, buscando optimizar la coherencia, evitar la duplicidad y mejorar la integridad del sistema.

**Análisis de Alternativas de Context Mapping**

Las alternativas consideradas incluyeron el movimiento de capacidades (capabilities) entre contexts, la descomposición y redistribución de sub-capacidades, la fusión y división de bounded contexts, la creación de nuevos contexts a partir de capacidades existentes, y la duplicación estratégica de funcionalidades.

***Movimiento de Capacidades:*** Se discutió el impacto de trasladar la capacidad de gestión de reseñas del contexto "Comentarios de Cinéfilos" al contexto "Reservas y Compras". Se concluyó que, si bien podría centralizar la experiencia del usuario en una sola interfaz, también podría sobrecargar el contexto "Reservas y Compras" y desdibujar la intención de cada contexto.

***Descomposición de Capacidades:*** Se evaluó la posibilidad de dividir el contexto "Administración de Funciones de Películas" en dos: uno enfocado en la programación y otro en la gestión de información de películas. Sin embargo, esto podría crear una barrera artificial que dificultaría la sincronización de cambios entre programación y detalles de películas.

***Creación de un Contexto Compartido:*** Se exploró la idea de formar un nuevo bounded context con las capacidades de promoción compartidas por varios contexts. Este enfoque fomentaría la reutilización y podría actuar como un servicio compartido, pero aumentaría la complejidad de la coordinación entre contexts.

***Duplicación de Funcionalidades:*** Se debatió sobre la duplicación de la funcionalidad de autenticación de usuarios en varios contexts para reducir dependencias. La conclusión fue que esto iría en contra de los principios DRY (Don't Repeat Yourself) y podría llevar a inconsistencias.

***Servicio Compartido:*** Se propuso un servicio compartido para la gestión de usuarios, que centralizaría la autenticación y el manejo de perfiles. Esta alternativa prometía una gestión de usuarios más cohesiva y una reducción de la duplicación.

***Aislamiento de Core Capabilities:*** Se contempló aislar las capacidades nucleares del contexto "Administración Cineclub" para formar un bounded context separado. Se decidió que, aunque podría clarificar las responsabilidades, también podría aumentar la latencia y los costos de sincronización.

**Decisiones y Patrones de Context Mapping**

Cada alternativa se discutió con la intención de llegar a la mejor aproximación posible. El equipo consideró patrones establecidos en Domain-Driven Design para manejar las relaciones entre los bounded contexts:

***Anti-Corruption Layer:*** Se optó por implementar una capa anti-corrupción para preservar la integridad del contexto "Reservas y Compras" al interactuar con sistemas externos.

***Shared Kernel:*** Se decidió contra la creación de un núcleo compartido debido a la naturaleza especializada y las diferencias en las necesidades de los distintos contexts.

## 4.3. Software Architecture.

### 4.3.1. Software Architecture System Landscape Diagram.

![C4-System Landscape Diagram](https://i.ibb.co/wB3M66P/C4-Arqui-1.png)

### 4.3.1. Software Architecture Context Level Diagrams.

El presente diagrama de contexto tiene como objetivo ofrecer una visión panorámica y de alto nivel del
sistema que se está analizando. Este sistema se sitúa en el centro del diagrama, mientras que las entidades
externas con las que interactúa se representan como cajas externas. Estas entidades pueden ser usuarios,
otros sistemas, bases de datos, servicios externos, entre otros. La finalidad de este diagrama es proporcionar
una comprensión clara y concisa de las interacciones clave del sistema con su entorno, permitiendo identificar
los principales flujos de información y las interfaces externas involucradas. A través de esta representación
visual, se busca facilitar el entendimiento inicial del sistema y sentar las bases para un análisis más detallado
de sus componentes y relaciones en niveles subsiguientes de la metodología C4.


![C4-System Context Level Diagram](https://i.ibb.co/GRWNQbR/C4-Arqui-2.png)

### 4.3.2. Software Architecture Container Level Diagrams.

En el diagrama de contenedores muestra cómo está organizado y cómo funcionan las diferentes partes del sistema que estamos analizando.
Imagina cada contenedor como una aplicación o servicio específico que hace algo concreto, como una página web o una base de datos.

En este diagrama, las líneas o flechas entre los contenedores nos muestran cómo se comunican entre sí y
cómo trabajan juntos para hacer que todo el sistema funcione correctamente. Es como un mapa que nos ayuda
a entender qué hace cada parte del sistema y cómo interactúan entre ellas.

![C4-Container Level Diagram](https://i.ibb.co/y5VjmHG/C4-Arqui-3.png)

### 4.3.3. Software Architecture Deployment Diagrams.

![C4-Deployment Diagram](https://i.ibb.co/QKdQwMx/C4-Arqui-4.png)
 








