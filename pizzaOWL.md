  
  
  
# Reasoner

En el apartado 4.9, al utilizar el reasoner, protege tendia a cerrarse, y a ir muy lento con la configuración inicial de protege en mi ordenador personal con Windows 10.
Tras un tiempo investigando, esto es por tener un heap de tamaño excesivamente bajo. Para solucionarlo, en el fichero "run.bat" cambiamos lo siguiente:
En la tercera linea aumentamos el tamaño a 2048M.
![image](https://user-images.githubusercontent.com/55484111/114521933-26a4ab80-9c43-11eb-8fd3-489d46596e2e.png)

Después de esto, ejecutamos el fichero por linea de comandos: ./run.bat

Una vez realizado esto, ya funciona correctamente.


