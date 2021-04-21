
# Las tareas genéricas y las estructuras de tareas.
El concepto de tarea genérica de Chandrasekaran:
- Se basa en la idea de que tiene que existir tipos de conocimiento y requisitos de control comunes al razonamiento de diagnóstico en diferentes dominios.
- Representación de conocimiento de las tarea de diagnóstico utilizando un vocabulario común.
- Esta idea se pueda aplicar a otros tipos de razonamiento.
- La experiencia humana está compuesta por un conjunto organizado de conocimiento.

Lo anterior lleva a la definición de una teoría general como una estructura de conocimiento que especifica.
- Una tarea de utilidad genral.
- Un método para llevarla a cabo.
- Elementos de conocimiento del dominio que necesita dicho método.

Estas tareas generales pueden ser vistas como bloques constructivos para la composición de tareas mas complejas. Definen:
- Tipo de problema a resolver.
- Objetivo que se persigue
- NO se dice como llevarla a cabo.

Problemas:
- Distinción entre tarea e instancia de la clase tarea.
## Método, subtareas e inferencias.
- Los métodos son los medios que nos permiten llevar a cabo una tarea.
- Un método es un conjunto de subtareas que permiten pasar del estado inicial de una tarea al estado objetivo.
- Puede contener información adicional sobre como las subtareas se ordenan en el tiempo.
- Las tareas obtenidas pueden ser aplicadas directamente o por medio de otros métodos, y por consiguiente de otras subtareas.

## Estructuras de Tareas.
- La estructura de tareas es un árbol de tareas, metodos y subtareas aplicadas de forma recursiva hasta que las tareas puedan ser ralizadas con el 
conocimiento del dominio del que se dispone.
- para una tarea se puede utilizar más de un método.
  - El uso de ET nos permite definir procesos de razonamiento en el nivel de conocimiento sin hacer referencia a la implementación.
