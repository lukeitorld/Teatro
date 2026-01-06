# Teatro
Un motor para crear videojuegos de texto interactivo, inspirado en Twine, diseñado para ejecutarse en la consola y escrito en el lenguaje de programación **Latino**.

## ¿Qué es Teatro?
**Teatro** es un módulo que funciona como motor de ficción interactiva o juegos conversacionales.  
Proporciona métodos y una estructura base para construir aventuras de texto en la consola, donde cada historia se desarrolla a través de **escenas** que incluyen un título, una descripción y un conjunto de opciones que el jugador puede elegir.

El nombre *Teatro* refleja su enfoque narrativo: las historias se representan como obras teatrales, en las que cada escena abre un nuevo acto y las decisiones del jugador marcan el rumbo de la obra.

## ¿Qué es Latino?
Latino es un lenguaje de programación con sintaxis en Español creado en C, inspirado en Lua y Python. Éste proyecto nace de la necesidad de incrementar la educación de nivel básico y avanzado, para que niños, adolescentes y también adultos se motiven a entrar en el mundo de la programación y desarrollar aplicaciones en una sintaxis a su idioma. Además, Latino es también para desarrolladores que les gustaría programar en Español, ya que Latino es completamente funcional en cualquier API en raw.
## ¿Cómo usar?

Debido a una limitación actual en el sistema de módulos de **Latino** (no es posible exportar funciones con argumentos), para utilizar **Teatro** es necesario descargar el script y crear el juego directamente dentro del mismo módulo.

Por ejemplo, para definir la escena del menú principal, al final del código del módulo podemos escribir:


```latino
menu = crear_escena(
    "Menú Principal",
    "Bienvenido a Teatro, el módulo para hacer aventuras conversacionales",
    0,
    ["Opción 1", "Opción 2", "Opción 3"]
)

cambiar_escena(menu)
```
<img width="1147" height="164" alt="image" src="https://github.com/user-attachments/assets/3a53b9db-e27a-42af-8418-ebfb76a01837" />
Luego quedaría agregar la lógica que quieres que se ejecute cuando se presiona el número correspondiente a la acción, para cual hay que usar la función leer(). 

