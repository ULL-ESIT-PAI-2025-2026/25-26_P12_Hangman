# Práctica 12. El juego del Ahorcado. 

### Factor de ponderación: 10 
### Estimación de horas de trabajo para realizar la práctica: 6

### Objetivos
Los objetivos de este ejercicio son poner en práctica:
* Integración continua para un proyecto de prácticas de la asignatura
* La arquitectura Modelo-Vista-Controlador (MVC)
* El uso del framework Bulma para dotar de estilos a una aplicación web simple.
* Programación orientada a eventos en TypeScript.
* Programación Gráfica en TypeScript usando la API Canvas.
* Metodologías y conceptos de diseño y Programación Orientada a Objetos en TypeScript.
* Principios y buenas prácticas de programación Orientada a Objetos.
* Algunos de los patrones de diseño que se han estudiado en la asignatura.
* El uso de elementos HTML.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
1. Su proyecto ha de incluir un fichero de configuración del flujo de desarrollo que permita automatizar mediante 
   [GitHub Actions](https://github.com/features/actions)
   la ejecución de las diferentes tareas del proyecto
1. Se valorará la realización de las diferentes tareas que se proponen
* El comportamiento del programa debe ajustarse a lo descrito en este documento
* Capacidad de la programadora de introducir cambios en el programa desarrollado
* Conocer y ser capaz de trabajar con el Framework
  [Bulma CSS](https://bulma.io/)
* La documentación de la aplicación incluirá un fichero README.md con la información correspondiente al
  proyecto desarrollado
* La estructura de directorios del proyecto será conforme a los requisitos establecidos en la asignatura
* Se acredita conocimiento y puesta en práctica de principios y buenas prácticas de programación orientada a objetos
* Saber corregir bugs en sus programas utilizando un depurador 
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema
* Acreditar el conocimiento las etiquetas de 
  [JSDoc](https://jsdoc.app/)
* Ser capaz de generar documentación para sus programas TS utilizando
  [TypeDoc](https://typedoc.org/)
  y de visualizar dicha documentación en un servidor web
* Acreditar su capacidad para configurar y utilizar 
  [ESLint](https://eslint.org/)
  y que es capaz de trabajar con la misma en Visual Studio Code
* Se comprobará que el código de su aplicación se adhiere a las reglas de las Guías de Estilo de Google para
  [TypeScript](https://google.github.io/styleguide/tsguide.html)
  y
  [JavaScript](https://google.github.io/styleguide/jsguide.html)
  Usando 
  [typescript-eslint](https://typescript-eslint.io/)
  si le resulta necesario para ello.
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de las Guías de Estilo de Google
  para Javascript y/o TypeScript
* Todas las prácticas realizadas hasta la fecha, incluída la que se presenta para su evaluación, se encuentran alojadas en repositorios privados de GitHub.

### Integración Continua
Estudie el trabajo expuesto en clase sobre
[Integración Continua](XXX)
para recordar cómo utilizar GitHub Actions para configurar un flujo de trabajo para su proyecto.

Incluya en su proyecto un fichero de configuración del flujo que permita automatizar la ejecución de las
diferentes tareas.

Incluya en su flujo de trabajo al menos las siguientes etapas:
* Análisis estático de su código utilizando ESLint. Utilice 
[typescript-eslint](https://typescript-eslint.io/)
para habilitar el análisis de código TypeScript en ESLint y configure el linter para que analice la
conformidad de su código con la Guía de Estilo de Google para TS.
* Generación de la documentación de su proyecto utilizando
[TypeDoc](https://typedoc.org/)
* Despliegue de su aplicación en una 
[GitHub Page](https://pages.github.com/) 
asociada con el repositorio de su proyecto.

Si hay alguna otra tarea que resulte de interés para su desarrollo, inclúyala igualmente en el flujo.

### El juego del Ahorcado
En esta práctica se propone desarrollar en Vanilla TypeScript una aplicación web SPA 
diseñada conforme al patrón Modelo Vista Controlador, que implemente el conocido juego del 
[Ahorcado](https://es.wikipedia.org/wiki/Ahorcado_\(juego\))

El juego, conocido en inglés como *Hangman*, es un popular juego de adivinanza que se juega 
habitualmente con papel y lápiz, aunque también existen versiones digitales, como la que se propone realizar.

El objetivo del juego es adivinar una palabra secreta que el ordenador ha elegido, 
antes de que se complete un dibujo de un ahorcado.

El ordenador elige una palabra y la escribe en forma de casillas en blanco, donde cada casilla representa 
una letra de la palabra. 
Por ejemplo, si la palabra es "goat", se representaría como "_ _ _ _" donde cada guión corresponde con una casilla
en blanco.

El jugador intenta adivinar la palabra, letra por letra. 
Por cada letra que adivina, el ordenador debe revelar su posición en la palabra si es correcta. 
Si la letra no está en la palabra, se registra como un intento fallido.

Generalmente, se permite un número limitado de intentos fallidos. 
Cada intento fallido se representa con una parte del dibujo del ahorcado (cabeza, tronco, brazos, etc.). 
Si el dibujo se completa antes de que el jugador descubra la palabra, el juego termina y el ordenador gana.
El juego puede terminar de dos maneras:
Victoria del jugador: Si el jugador descubre todas las letras de la palabra antes de completar el dibujo del ahorcado.
Victoria del ordenador: Si el adivinador agota todos sus intentos sin adivinar la palabra.

Utilice para su aplicación un diccionario de palabras que incluya exclusivamente nombres de países en español.

### Indicaciones de caracter general
El programa que desarrolle ha de ser orientado a objetos y utilizar una arquitectura MVC.
Ponga en práctica en su desarrollo los fundamentos, principios y buenas prácticas de la OOP así como los
conocimientos que haya adquirido en el uso de patrones de diseño.

Utilice un fichero distinto para el código de cada una de las clases que intervienen en su programa.

Encapsule las clases en módulos que exporten la correspondiente clase a quien precise usarla.

La estructura de directorios de su proyecto de práctica debe ser conforme con la establecida para las prácticas de PAI.

Configure adecuadamente ficheros `package.json` y `tsconfig.json` en el directorio raíz de su ejercicio 
que permitan la instalación de las dependencias de su proyecto.

Actualice el fichero `README.md` con la información que considere relevante de su proyecto de práctica y haga que ese fichero
sea la primera página de la documentación (TypeDoc) de la práctica.

Haga que en el elemento `title` del código HTML de todas las páginas web de su poroyecto figure su nombre y apellidos.

Utilice el depurador integrado en el navegador para confirmar que el flujo de ejecución de su programa es el correcto.

No intente desarrollar su aplicación en un único paso.

Previo al desarrollo, realice un diseño de su aplicación identificando las diferentes clases que
intervienen en el programa. 
Utilice lápiz y papel para hacer un esquema de las relaciones entre las diferentes clases.

Después de esa planificación inicial, trabaje mediante sucesivos refinamientos de una primera aproximación.
También puede resultarle conveniente realizar pequeñas aplicaciones auxiliares que le sirvan para comprobar y
aprender el funcionamiento de algún aspecto concreto de la aplicación.

Cuando finalice su aplicación, utilice 
[Mermaid.js](https://mermaid.js.org/), 
[Lucidchart](https://www.lucidchart.com/pages) o cualquier otra herramienta que conozca para trasladar sus
diseños en papel a un diagrama en formato digital que pueda mostrar a través de una web.

Configure en el directorio `/public` de su práctica, la página `index.html`, 
que servirá de "página índice" tanto para su aplicación como para los ejercicios de la sesión de evaluación.
Enlace también en esa página tanto la página que contiene la documentación (Typedoc) de su proyecto
como otra que mostrará el diagrama UML de las clases que intervienen en su programa.

### Interfaz gráfica y especificaciones de la aplicación
Tenga en cuenta las siguientes especificaciones a la hora de diseñar su programa:

Intente que su aplicación imite en la medida de lo posible el aspecto y funcionalidades de
[esta página](https://www.englishclub.com/esl-games/hangman/animals-easy.php),
una vez clicado el botón `START`, que se tomará como referencia.

Su aplicación no ha de contemplar el botón de arranque, sino que al inicializarse ha de mostrar ya el juego en
curso.

También la dinámica del juego de su aplicación debe imitar a la de referencia.

Utilice libremente los elementos HTML que considere más adecuados para la interfaz gráfica de su aplicación y
dote de estilo a esos elementos utilizando Bulma.

Sobre un fondo de color gris se representarán las casillas vacías correspondiente a la palabra a adivinar así
como las casillas correspondientes a cada una de las letras del alfabeto.

Se representará gráficamente el patíbulo, la horca y el ahorcado, para lo cual se propone utilizar los ficheros
[Hangman-X.png](https://en.wikipedia.org/wiki/File:Hangman-6.png)
(cambie X por un valor entre 1 y 6) para obtener los 6 ficheros que corresponden con la secuencia del juego).
Si lo desea, puede Ud. utilizar otras imágenes diferentes de esta propuesta.

### Presentación de resultados
Configure una página GitHub asociada con su repositorio de trabajo que sirva de índice para estas otras
páginas de su proyecto:
* La aplicación *Hangman* que habrá desarrollado. Esa aplicación se configurará como una SPA.
* La documentación de la aplicación.
* El diagrama UML de las clases utilizadas en la aplicación.
* Una página que albergará el ejercicio que se le pedirá realizar en la sesión de evaluación de esta práctica.

Todas estas páginas deberán tener un estilo personalizado que imite utilizando Bulma el aspecto (tipografía, colores) de las *páginas ULL*.

## Referencias
* [Ahorcado](https://es.wikipedia.org/wiki/Ahorcado_\(juego\))
* [GitHub Actions](https://github.com/features/actions)
* [GitHub Pages](https://pages.github.com/)
* [Bulma](https://bulma.io/)
* [TypeDoc](https://typedoc.org/)
* [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
* [Jest](https://jestjs.io/)
* [PAI Code Examples](https://github.com/ULL-ESIT-PAI-2024-2025/PAI-class-code-examples)
