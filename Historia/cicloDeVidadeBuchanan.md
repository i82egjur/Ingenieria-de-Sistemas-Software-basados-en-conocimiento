# Modelo de ciclo de vida de Buchanan.

Desde un punto de vista ingenieril sobre la construcción de los primeros sistemas expertos, podemos considerar
que construir un SBC es un proceso de transferir el conocimiento humano a un base de conocimiento
implementada en un computador.
- El conocimiento se extraía mediante entrevistas al experto.
- Esta transferencia se basaba en la idea de que el conocimiento puede recogerse e implementarse en un computador
- Buchanan culmino el paradigma de la IC como proceso de transferencia.
  - Este presento el desarrollo de un SBC como un proceso de adquisición de conocimiento entendido como:
    - Transferencia y transformación de la experiencia  a un programa.

![imagen](https://user-images.githubusercontent.com/55484111/115199677-be970f00-a0f3-11eb-8eba-a1fb7c66f38d.png)

Según Buchanan, la construcción de un sistema experto es un proceso de revisión casi constante, que puede implicar:
- Redefinir conceptos y representaciones
- Refinamiento del sistema  repitiendo las 2 ultimas etapas hasta alcanzar el comportamiento deseado.
- Este metodología es importante es el primer planteamiento de una metodologia de desarrollo de SBCs.
- Se plantearon numerosas modificaciones a esta.

Estas metodología tuvieron relativo exito hasta los noventa, donde pasamos de la transferencia hacia
el modelado para solucionar.
- Cuello de botella de adquirir conocimiento.
- Solucionar carencias como:
  - Explicaciones complicadas debido a la ausencia de separación en el conocimiento sobre "que", "como"
  y "por qué".
  - El sistema no tenia conciencia de sus propias limitaciones, se daban respuestas poco útiles en vez de decir no.
  - Mantenimiento complicado.
    - Validación de conocimiento es complejo
    - Dispersión del conocimiento, hacia que la extensión de la base de conocimiento fuera complejo.
    - La independencia y modularidad de un conjunto de reglas no era tan evidente ya que añadir reglas podria
    producir interacciones negativas con el resto de las reglas.
 
 - Este modelo, no permitia adaptar la configuración a situaciones concretas y los requisitos tenian que estar 
   completos al inicio, lo que complicaba la adaptabilidad.
  
 - La experiencia acumulada en la aplicación de este modelo trajo que la propuesta de Buchanan del modelo
 en cascada no era el idoneo para el desarrollo de SBCs.
   
