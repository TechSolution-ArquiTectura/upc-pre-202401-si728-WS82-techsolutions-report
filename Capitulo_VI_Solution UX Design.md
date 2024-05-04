# 6.1. Style Guidelines.

## 6.1.1. General Style Guidelines.

Como organización se considera el diseño web una parte muy importante del proyecto, ya que debe ser agradable, cómodo de navegar por nuestros clientes finales, estar en sintonía con nuestra marca y lo que queremos transmitir como empresa.

Para la elaboración de la guía de estilos de TuCine nos basaremos en 5 elementos esenciales:

### Misión:
Promover la cultura cinematográfica y apoyar el ciclo de vida del cine en Perú. A través de nuestra aplicación móvil, pretendemos distribuir y promover películas especializadas y no comerciales, apoyar a cineastas, artistas locales y crear una comunidad dedicada al arte cinematográfico.

### Visión:
Nuestra visión consta de ser una plataforma líder para la promoción y difusión de películas de nicho y no comerciales, los cuales serán reconocidos por la gran calidad y excelencia que proporciona nuestro servicio. Nos esforzamos por ser una empresa innovadora en la distribución cinematográfica y también por ser un punto de encuentro para cinéfilos y gente gustante del cine de nicho.


### Público Objetivo:
Cinéfilos de rango de edad entre 18 a 50 años con una preferencia por el cine alternativo, además, buscan conocer y compartir su afición con otras personas. Propietarios de cineclubes que necesiten una mayor visibilidad y que ofrecen como servicio la proyección de películas del género alternativo.

### Personalidad de la marca:
TuCine ofrece una diversidad de locaciones para disfrutar esa película especial, conoce y organiza salidas grupales con personas aficionadas al cine.

### Valores fundamentales:

• Confianza, lealtad, seguridad y empatía. El deseo por mejorar y ofrecer un mejor servicio cada día.

• Dimensiones del tono de comunicación y lenguaje aplicado tomando en cuenta que nuestro público objetivo son personas que gustan de un arte más maduro elegimos un tono formal, pero a la vez amigable y respetuoso con el objetivo de que nuestros clientes se sientan cómodos con nuestro trato y el servicio brindado.

• Del mismo modo, buscaremos lograr la confiabilidad de nuestros usuarios al contar con un equipo, testimonios o historias de clientes satisfechos con el servicio de TuCine.

• Las palabras banderas de nuestra marca serán las siguientes: novedoso, confiable, seguro, emocionante y divertido.

### Colors
![component](Resources/GeneralStyles/6.1.1.png)


### Typography
![component](Resources/GeneralStyles/6.1.2.png)

### Spacing
![component](Resources/GeneralStyles/6.1.3.png)

### Buttons
![component](Resources/GeneralStyles/6.1.4.png)

## 6.1.2. Web, Mobile & Devices Style Guidelines.

Para la elaboración del Style Guidelines de la web de TuCine se utilizarán los componentes de PrimeNg. Primevue es una librería open source de desarrollo que nos brinda un conjunto de componentes (+80) de diseños llamativos y receptivos amigables con Angular y también disponibles en React, Vue y Java.

Entre los componentes se implementaron los que más se relacionaban con el core del negocio. En el Style Guide se encuentran los botones de acciones y redes sociales. Los iconos categorizados por funcionalidad, los campos de texto, Breadcrumbs, Placeholders, entre otros. Una vista previa de estos componentes se puede ver en Figma. Para el desarrollo de nuestros mock-ups de la aplicación web, hemos utilizado pantallas comunes de la versión desktop

# 6.2. Information Architecture.

## 6.2.2. Labeling Systems.
• Encabezados (headings): Estas etiquetas benefician al usuario para poder comprender toda la información de un apartado en el que se encuentre con tan solo leerla.

• Etiquetas textuales: Son etiquetas que se usan comúnmente para indicar ciertos apartados.

• Etiquetas icónicas (iconics labels): Consiste en utilizar imágenes para que esta etiqueta pueda tener significado pleno sin necesidad de texto adicional, pero, normalmente, van acompañadas de etiquetas textuales para que el usuario no se confunda. Estas dos etiquetas en cuestión se evidencian en la barra de navegación de nuestro mockup
## 6.2.3. Searching Systems.
En esta sección del informe se busca definir nuestra arquitectura de la información para que el usuario final no se vea abrumado con tanta información. La aplicación proporciona vasta información sobre recintos, películas y publicaciones es por ello que se contará con los siguientes elementos:

### Campo de búsqueda: 
Estará ubicada en la dentro de la barra de navegación, el usuario podrá ingresar la palabra que crea esta asociada a la película, cineclub, publicación o grupo que busca.

![component](Resources/GeneralStyles/6.1.5.png)

Etiquetas: Los resultados más relevantes se mostrarán primero,sin embargo, los resultados pueden ser ordenados por medio de las etiquetas que aparecerán en la parte superior, ejemplo: Películas, CineClubs, Grupos y Publicaciones.

Por otro lado, la sección Películas y Cineclubs contará con la opción de filtrado.

![component](Resources/GeneralStyles/6.1.6.png)

## 6.2.4. SEO Tags and Meta Tags.
Los Meta tags son etiquetas invisibles que brindaran datos sobre la página web a los motores de búsqueda y visitantes del sitio web, facilitan que los motores de búsqueda determinen el propósito de nuestra aplicación, por lo tanto, son vitales para el SEO.
### Title tag
<.head>

<.title>TuCine</.title>

</.head>

### Meta description
<.head>

<.meta name="description" content="TuCine ofrece una diversidad de locaciones para disfrutar esa película especial, conoce y organiza salidas grupales con personas aficionadas al cine.">

</.head>


### Robot Meta tag
<.!DOCTYPE html>
 
<.html><.head>

<.meta name="robots" content="noindex" />

<./head>

<.body>(…)</.body>

</.html>

### Alt Text

Las imágenes deben ser accesibles tanto para los motores de búsqueda como para las personas. Además, en caso no cargará la imagen proporciona unaalternativa de texto a las imágenes que se mostrará.

<.div class="download-ios-and">

<.img src="pictures/googlePlay.png" alt="Google play">

<.img src="pictures/appStore.png" alt="App Store">

<./div>
## 6.2.5. Navigation Systems.
A través de nuestra aplicación, los usuarios pueden navegar de manera intuitiva gracias al uso de lenguaje claro y conciso que caracteriza a cada sección. Pueden presionar en la palabra o íconos respectivos para dirigirse a la sección especificada. También, pueden utilizar los botones desplegados que intercomunican secciones y habilitan nuevas interacciones. Los usuarios pueden recorrer el contenido de manera aleatoria, ya que pueden acceder a cualquier sección en el momento que lo requieran. Evidentemente, las páginas de registro o inicio de sesión serán siempre primeras en caso el usuario aún no esté registrado o no haya iniciado sesión en la aplicación
# 6.3. Landing Page UI Design.

## 6.3.1. Landing Page Wireframe.

A continuación, podemos ver los diseños realizados para nuestro landing page de la aplicación, en la 
cual nuestros posibles usuarios podrán tener una vista previa de las funcionalidades de nuestra aplicación
y lo que les podemos ofrecer.
![landing_page wireframe 1](Resources/landing_web_uix/landing_page_wireframe1.png)

## 6.3.2. Landing Page Mock-up.

En las siguientes imágenes se pueden apreciar los Mock-ups de la landing page, considerando 
la estructura trabajada previamente en los wireframes. Se realizaron en Figma.

Link: https://www.figma.com/file/3PjbxbuhPKzi9PagxItJ6R/Open-Source?type=design&node-id=0-1&mode=design

## 6.4. Applications UX/UI Design.

## 6.4.1. Applications Wireframes.

### Registro / Inicio de sesión

![web_design1](Resources/landing_web_uix/web_design_1.png)

### Sección Cineclubs

![web_design2](Resources/landing_web_uix/web_design2.png)

### Sección Cineclubs

![web_design3](Resources/landing_web_uix/web_design3.png)

![web_design4](Resources/landing_web_uix/web_design_4.png)

### Perfil Película

![web_design5](Resources/landing_web_uix/web_design5.png)

### Explorar

![web_design6](Resources/landing_web_uix/web_design6.png)

### Creación de Grupos

![web_design7](Resources/landing_web_uix/web_design7.png)

### Mensajería

![web_design8](Resources/landing_web_uix/web_design8.png)

### Grupos

![web_design9](Resources/landing_web_uix/web_design9.png)

### Perfil de Usuario

![web_design10](Resources/landing_web_uix/web_design10.png)

## 6.4.2. Applications Wireflow Diagrams.

El usuario ingresa la película de su preferencia en el buscador global ubicado en la barra de navegación. 
Selecciona la imagen de la película, para luego mostrar la interfaz con la descripción de la película y
los cineclubs disponibles para reservar.

![web_wireflow](Resources/landing_web_uix/web_wireflow.png)

### Reserva de una función por medio de la búsqueda de una cineclub

El usuario ingresa el cineclub de su preferencia en el buscador global ubicado
en la barra de navegación. Selecciona el slide de su preferencia, para luego 
mostrar el perfil del CineClub con las funciones disponibles.

![web_wireflow2](Resources/landing_web_uix/web_wireflow2.png)

### Creación de grupos

En la opción Grupos de la barra de navegación, se selecciona Crear nuevo grupo
y se procede a completar los campos requeridos.

![web_wireflow3](Resources/landing_web_uix/web_wireflow3.png)

