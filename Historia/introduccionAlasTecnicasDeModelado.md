# Introducción a las técnicas de modelado.

El trabajo de Newell en 1982 dejó claro que la discusión en el desarrollo de SBCs se realizaba en términos del nivel simbólico y no entre las tareas y elk tipo de conocimiento
requerido para llevarlas a cabo. Para centrar la discusión en esto se plantea que el análisis se haga de manera independiente de la implementacion, lo cual desemboca
en el modelado del conocimiento.  
La transición de reconocer la existencia del nivel de conocimiento a la aparición de las primeras metodologías fue un proceso de refinado de una serie de ideas
novedosas.  
Dos trabajos fueron esenciales para esto:
- Metofos de Resolución de Problemas con limitación de Roles 
- Tareas Genéricas.

Estos trabajos pueden considerarse paralelos y ponen de manifiesto lo siguiente:
- La idea de limitar los roles que puede jugar el conocimiento en un determinado dominio.
- Los conceptos de tareas y métodos genéricos como elementos constitutivos de los SBCs.

# Métodos con limitación de roles.
Los métodos de R.P con limitación de roles McDermott se pueden considerar como uno de los primeros intentos de usar la reutilización en el desarrollo de los SBC.

Tras el análisis de diversos SBC, macDemorth puso de manifiesto ciertas características de estos.
  1. Conocimiento de control sencillo
  2. Conocimiento de control embebido en la BC
    1. Origina problemas de mantenimiento y falta de reutilización.
2. No se proporciona guía para extraer el conocimiento.

La solución a esto es, separar el MRP de la BC especíofica de la tarea. De forma que permite seleccionar conocimiento del dominio a adquirir y reutilizarse.

Descripción MRP:
Una tarea se resuelve mediante un MRP que aporta conocimiento de control.
Un MRP esta formado por un bucle de 5 a 10 pasos (subtareas)

Conclusiones:
- Existían de tareas que podían ser resueltas por métodos cuyo conocimiento de control era lo suficientemente abstracto para que no se viese influenciada
por el conocimiento del dominio 
- Al definir un método en los términos anteriores, se indicaba implícitamente qué roles pueden jugar los componentes del conocimiento del dominio.
- Un método proporciona una guía lo suficientemente clara de qué conocimineto se tenía qie adquirir y cómo éste se tenía que implementar.
- La definición de los roles provocaba una disminución en la diversidad del conocimineto que se tenía que utilizar en la implementación de la tarea.
- Los MRP proporcionaban las línas básicas para la adquisicón y codificación de conocimiento.


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






