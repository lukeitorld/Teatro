# Teatro
Un motor para crear videojuegos de texto interactivo, inspirado en Twine, diseñado para ejecutarse en la consola y escrito en el lenguaje de programación **Latino**.

## ¿Qué es Teatro?
**Teatro** es un módulo que funciona como motor de ficción interactiva o juegos conversacionales.  
Proporciona métodos y una estructura base para construir aventuras de texto en la consola, donde cada historia se desarrolla a través de **escenas** que incluyen un título, una descripción y un conjunto de opciones que el jugador puede elegir.

El nombre *Teatro* refleja su enfoque narrativo: las historias se representan como obras teatrales, en las que cada escena abre un nuevo acto y las decisiones del jugador marcan el rumbo de la obra.

## ¿Qué es Latino?
Latino es un lenguaje de programación con sintaxis en Español creado en C, inspirado en Lua y Python. Éste proyecto nace de la necesidad de incrementar la educación de nivel básico y avanzado, para que niños, adolescentes y también adultos se motiven a entrar en el mundo de la programación y desarrollar aplicaciones en una sintaxis a su idioma. Además, Latino es también para desarrolladores que les gustaría programar en Español, ya que Latino es completamente funcional en cualquier API en raw.
## ¿Cómo usar?

Teatro puede usarse como un [Módulo] (https://manual.lenguajelatino.org/es/stable/sintaxis/Modulo.html), esto implica que solo debemos seguir los siguientes pasos:
- Descargar el módulo teatro.lat.
- Colocar ```teatro = incluir ("teatro")``` al comienzo del archivo donde trabajemos, junto con  ```estado = teatro.estado``` y ```metodos = teatro.metodos```.
## Ejemplo mínimo: Dos escenas


```latino
teatro = incluir ("teatro")
estado = teatro.estado
metodos = teatro.metodos

//Estructura obligatoria que debe tener una escena: Un diccionario con 4 elementos (nombre: cadena, descripcion: cadena, id:decimal, opciones: lista con 3 datos del tipo cadena)
//Para cambiar de escena al elegir una opcion se puede hacer lo siguiente: escribir la función teatro.metodos.cambiar_escena(escena_a_cambiar) entre >< dentro del texto de una opción.
//la siguiente escena, menu, tiene en su primera opción la capacidad de cambiar a la escena guardada en modulo_teatro.
menu = {
    "nombre": "Menú Principal",
    "descripcion": "Este es el menú",
    "id": 0, 
    "opciones": ["Saber más sobre Teatro.>teatro.metodos.cambiar_escena(modulo_teatro)<", "Nada><", "Nada ><"]
}
modulo_teatro = {
    "nombre": "Manual de Teatro",
    "descripcion": "Teatro es un módulo creado por Lukeitor para servir como un pequeño motor de juegos narrativos. Lo cual implica que trae una serie de métodos y variables que proveen la arquitectura básica y elemental para hacer un juego de aventuras de texto EN la consola. Teatro Vendría a ser el esqueleto básico para diseñar un juego narrativo, pero no un juego en sí mismo. El proyecto está en desarrollo y podría tener errores. En la versión 0.4 se puede: Mostrar escenas en la consola, elegir opciones con los números 1,2 y 3; y ejecutar funciones al elegir una opción.",
    "id": 1, 
    "opciones": ["nada><", "nada><", "nada><"]
}

funcion iniciar()
    //Método del módulo que borra la consola y carga la información de la escena menu.
    teatro.metodos.cambiar_escena(menu)
    jugando = verdadero
    //bucle central del juego. Si hay un error se puede detener con ctr + C o cerrando la consola
    mientras (jugando)
        teatro.metodos.procesar_entrada(leer())
    fin
    
fin
//llamamos al función para que comience el juego
iniciar()
//llamamos al función para que comience el juego
iniciar()
```
## Roadmap
- V 0.40 --> Ejecutar funciones al elegir una opción.
- V 0.43 --> Agregar evento cuando_entra al cambiar de escena.
- V 0.46 --> Agregar capacidad de configurar los colores y estilos de texto.
- V 0.49 --> Agregar sistema de guardar/cargar.
- V 0.50 --> Versión final de Teatro para consola.
- V 0.51~1.00 --> Versión de Teatro con ventana gráfica usando la librería GTK. 
