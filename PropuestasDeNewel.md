# Las propuestas de Newell.

Newell en 1982 analizó las causas de la crisis de la IC. Hasta esto, se consideraba que:
- UN sistema computacional se descomponía en 5 niveles:
1. N. Dispositivos, el más bajo, transistores, diodos.
2. N. Circuitos, circuitos integrados.
3. N. Lógico formado por puertas lógicas, biestables, registros, contadores.
4. N. Simbólico Nivel de programación.
5. Configuración Nivel de configuración de conmutación Procesador memoria. (CPM)
    - Describe configuraciones abstractas a partir de los ultimos 2 niveles
    - En este se definen las arquitectutas hardware y software.

![imagen](https://user-images.githubusercontent.com/55484111/115211730-25222a00-a100-11eb-9da1-2ea0d9bcc352.png)


Cada nivel queda descrito por:
- El medio que procesa.
- Los componentes que proporcionan las primitivas de procesamiento.
- Leyes de composición que permiten ensamblar componentes
- Leyes de comportamiento del sistema quye depende del comportamiento de sus componetes y la estructura del sisitema.

Principal problema de newell:
- Diferencia entre conocimiento y la representación de este.
- Origen del problema:
  - Al ser el nivel simbólico el más alto.
    - El conocimiento como su representación se colocaban aquí.
    - Esto es el refeljo del paradigma de extracción del conocimiento. 
- Para resolverlo, se propone el nivel de conocimiento.

Hipótesis del Nivel de Conocimiento:
- Existe un nivel adicional en los sistemas computacionales justo encima del nivel simbólico caractizado po:
  - El conocimiento como medio
  - El principio de racionalidad como ley de comportamiento.

- Características.
  - Sistema: agente.
  - Componentes: Objetivos, acciones, cuerpos de conocimiento.
  - Medio: Conocimineto.
    - El agente procesa el conocimiento que tiene para determinar las acciones a tomar.
  - Ley de comportamiento: principio de racionalidad.
    - Si el conocimiento que posee el agente le indica que una de sus acciones puede llevarle a la 
      consecución de sus objetivos, entonces el agente seleccionarña dicha acción. 
      
- Un agente del nivel de conocimiento esta compuesto por:
  - Un cuerpo fisico que le permite interaccionar con el entorno mediante una serie de acciones.
  - Cuerpo de conocimiento, es como una memoria que contiene todo lo que el agente sabe en un 
    determinado instante. 
- Objetivos:
  - Un objetivo es una parte diferenciada del cuerpo de conocimiento que define un determinado estado del entorno
    que se quiere alcanzar.

- El conocimiento se puede descirbir tanto en:
  - Terminos funcionales. ¿Que hace? 
  - Terminos estructurales. Propiedades y relaciones

- El conocimiento **NO** se puede describir como una secuencia de estados en los que encontrar las esctructuras físicas.
- Esto hace que el conocimiento sea una entidad abstracta y que no se pueda hacer explícito con la misma facilidad que los medios del resto de niveles.

- Si a esto le unimos el hecho que antes el conocimiento era parte del nivel simbólico, la construcción de SBC debia superar:
- La dificultad de la detección y explicitación del conocimiento.
- El intento de codificarlo en el nivel simbólico.

El nivel simbólico solo debería reflejar un conjunto reducido de los posibles comportamientos que no podemos
representar un comportamiento indeterminista mediante estructuras deterministas.

La solución de estos problemas es la consideración del NIVEL DE CONOCIMIENTO.

En el nivel de conocimiento no existe ninguna ley de composición que indique como ensamblar los elementos.
Esta ausencia de estructura es clave ya que el comportamiento del sistema se define en base a lo que el agente sabe y no en la forma en como se unen
sus compoenentes.
Lo que hace que el comportamiento del sistema solo dependa de lo que el agente sepa, quiera y los medios con los que interacciona con el exterior.
Esta característica será el punto de partida de la idea de la reutilización del conocimiento. 










