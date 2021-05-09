

# Ingeniería del conocimiento
## Modelo de conocimiento.

- Introducción. La construcción de un SBC es una actividad de modelado usada para consturir un sistema con capacidad para resolver probleas de forma similar a un humano.
en un determinado dominio de aplicación. La experiencia humana en cualquier dominio se puede analizar en terminos de categorias, patrones y estructuras de conocimiento, estables
y genéricas.

- El conocimiento es una entidad funcional estructurada, cuyas partes pueden jugar distintos papeles en el proceso de resolución de problemas

### El modelo de conocimiento en commonKADS

- EL modelo de conocimiento es una herramienta que ayuda a clarificar la estructura de las tareas intensivas de conocimiento sin hacer referencia a la implementación.

#### Estructura del modelo de conocimiento.
- El conocimiento se divide en conocimiento del dominio, sobre inferencias y sobre tareas.

- Conocimiento del domonio: que incluye la terminología general y hechos del dominio descritos independientemente de tareas particulares.

- Conocimiento sobre inferencias: Las inferencias sob bloques basicos con los que se construyen los procesos de razonamiento realizados sobre el conocimiento del dominio.

- Conocimiento sobre tareas: Se refiere a la terminología, modelo computacionales y hechos asociados con la ejecución de un tipo de tarea sin tener que centrarse en un dominio concreto.
-                             Este se describe mediante los objetivos que se quieren perseguir y la forma en como alcanzarlos.


### Conocimiento del dominio
- Conocimiento relevante del dominio de la aplicación objeto del modelado. que incluye la terminología general y hechos del dominio descritos independientemente de tareas particulares.
- Se divide en esquema del dominio y base del conocimiento.
#### Esquema del dominio.
- Incluye la terminología general utilizada para describir el conoimiento del dominio particular
- Describe esquematicamente la información y el conocimiento estático del dominio de la aplicación.
- Tres constructores básicos:
  - Conceptos Se usan para definir colecciones de objectos con caracteristicas similares, es a veces dificil saber si un elemento del dominio debe considerarse concepto o un atributo,
  para ello, vemos si tiene existencia propia o depende de otro, pero dependerá de la relevancia del elemento y la experiencia del ingeniero
  - Relaciones entre los conceptos definidas por medio de sus argumentos
  - Tipos de reglas. Permite modelar en un  único tipo un conjunto de reglas que comparten una estructura similar
  - Modularización y reutilización

### Base del conocimiento
- Amplia el esquema del dominio con los hechos específicos del dominio. Representa las instancias de los tipos especificados en el esquema del dominio.
-La existencia de bases de conocimiento es una caracteristica distintiva del modelado del conocimiento ya que en otras fases de análisi no se suele tratar esto,
pero cuando modelamos el conocimiento, si resulta importante,


### Conocimiento sobre inferencias.
Aquí describimos como utilzar estas estructuras estáticas para llevar a cabo procesos de razonamiento.
- Principales elementos que usaremos:
  - Inferencias
  - Roles de conocimiento
  - Funciones de transferencia.

El conocimiento sobre las inferencias describe el nivel más bajo de la descomposición funcional, las inferencias, que son unidades básicas de procesamiento de la información.
cada inferencia queda completamente descritas mediante sus entradas y salidas, sin tener en cuenta lo intermedio.
Pararemos cuando la tengamos una traza comprensible del razonamiento efectuado por el sistema.

Las inferencias solo pueden hacer referencia al conocimiento a través de los roles de conocimiento.
Estos son etiquetas que indican el papel que juega el conocimiento en el proceso de razonamiento.
- Tipos de roles:
  - Estáticos El conocimiento utilizado para realizar el proceso de la inferencia
  - Dinamicos Las entradas y salidas de las inferencias.

Principal ventaja, consigue desacoplar la especificación de las inferencias del conocimiento del dominio, lo que nos permite:
  - Poder realizar en paralelo la especificación de las inferencias y del conocimiento del dominio.
  - Reutilizar las descripciones de las inferencias de otros problemas.
  - Nos proporciona un vocabulario para especificar la forma de uso del conocimiento en el proceso de razonamiento, independientemente del dominio de aplicación elegido.


#### Funciones de transferencia.

