
# Autor: Rafael Egea Jurado

# Fallos encontrados
- En algunos ejercicios, hemos encontrado que los print, no usan () por lo tanto daban fallo al ejecutar con la nueva versión de python. Simplemente los hemos añadido
los parentesis. 

# RDF

## Ejercicio 1.
- Muestra en formato xml el grafo cargado.

## Ejercicio2 
- Carga el grafo, asocia dc a EX y foaf a FOAF, añade el archivo exe2.rdf y lo pone en formato xml. Recorre el grafo por alguien que de nombre tenga a bob e imprime su
- identificación. Posteriormente, con esta, recorre otra vez el grafo para ver quien es la acosadora secreta (secretStalking) de bob.

## Ejercicio 3
- Similiar al anterior pero serializa a n3.

## Ejercicio 4
- Muestra todos los statementes del grafo.
- Imprime el grafo serializado a n3

## Resto de ejercicios
- Una vez que entendemos las bases y que significan las funciones, entender el resto de programas es relativamente simple.



## Ejemplo Propuesto.
### RDFLIB
Creamos un fichero simple, que contenga comida y muestre como se interrelacionan.

        <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
          xmlns:eg="http://example.org/foovocab#"
          xmlns:foaf="http://xmlns.com/foaf/0.1/">
            <foaf:Comida rdf:nodeID="PatatasConCarne">
                <foaf:name>PatatasConCarne</foaf:name>
                <foaf:Tiene rdf:nodeID="Patatas"/>
                <foaf:Tiene rdf:nodeID="Carne"/>
            </foaf:Comida>
            <foaf:Comida rdf:nodeID="Patatas">
                    <foaf:name>Patatas</foaf:name>
            </foaf:Comida>
            <foaf:Comida rdf:nodeID="Carne">
                <foaf:name>Carne</foaf:name>
            </foaf:Comida>

        </rdf:RDF>

Con el anterior, creamos un programa que imprima el anterior en formato el xml y busque el id de un plato que se llame "patatas"


        #!/usr/bin/env python
        # -*- coding: iso-8859-1 -*-

        #from rdflib import ConjunctiveGraph, 

        from rdflib import Graph
        from rdflib import Namespace
        from rdflib import Literal

        FOAF = Namespace("http://xmlns.com/foaf/0.1/")
        EX = Namespace("http://example.org/foovocab#")


        def main():
            s = Graph()
            s.bind('dc',EX)
            s.bind('foaf',FOAF)

            s.parse("ejemplo.rdf")
            print (s.serialize(format="xml"))

            print ('Encuentra algo que se llame patatas')
            for comida in s.subjects(FOAF["name"], Literal("Patatas")):

                print  ('El plato es:', comida)




        if __name__ == '__main__':
            main()

Ejecución:

    rafa@rafa-PE70-6QE:~/Imágenes/ejerciciosRDF/rdflib/ejemploRdf$ python3 ejemploRDF.py 
    b'<?xml version="1.0" encoding="UTF-8"?>\n<rdf:RDF\n   xmlns:foaf="http://xmlns.com/foaf/0.1/"\n   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"\n>\n 
        <rdf:Description rdf:nodeID="N7d2b909c69304c6da4068340599b2925">\n    
        <foaf:name>PatatasConCarne</foaf:name>\n  
        <foaf:Tiene rdf:nodeID="Ndf9535d95e16410ea5e75d7454c6ceeb"/>\n    
        <foaf:Tiene rdf:nodeID="N54dcff0be02f413a8a2d27ae1e7af199"/>\n    
        <rdf:type rdf:resource="http://xmlns.com/foaf/0.1/Comida"/>\n  
        </rdf:Description>\n  
        <rdf:Description rdf:nodeID="Ndf9535d95e16410ea5e75d7454c6ceeb">\n                     
        <foaf:name>Carne</foaf:name>\n    
        <rdf:type rdf:resource="http://xmlns.com/foaf/0.1/Comida"/>\n  
        </rdf:Description>\n  
        <rdf:Description rdf:nodeID="N54dcff0be02f413a8a2d27ae1e7af199">\n    
        <foaf:name>Patatas</foaf:name>\n    
        <rdf:type rdf:resource="http://xmlns.com/foaf/0.1/Comida"/>\n           
    </rdf:Description>\n</rdf:RDF>\n'
    Encuentra algo que se llame patatas
    El plato es: N54dcff0be02f413a8a2d27ae1e7af199


    

# Sparql

## p1.py
Simplemente carga un fichero rdf y hace una consulta que imprime.

## pers-1-old.py

El flujo de la ejecución sigue los siguientes pasos:
1. Entra en el main
2. Llama a q1 y entra en la función
3. Inicializa una variable _my_data_ con los datos
4. Inicializa una variable g con Graph()
5. Inicializa una variable resul con el resultado de parsear g con una ontologia .owl
6. inicializa otra ontologia pero no la guarda,
7. Imprime el valor de result.
8. Imprime la longitud de g
9. Imprime el grafo de g en formato xml
10. Inicializa una variable con la consulta a realizar
11. Realiza la consulta
12. La imprime

## q1.py y q1-1.py
Son practicamente iguales que el anterior, la complejidad de la consulta realizada aumenta un poco quizas pero son muy parecidos

## q2-2.py

Este se diferencia con los demás en que no carga un fichero externo, sino que lo hace desde el mismo código del programa en formato n3, 
despues imprime la longitud, el contenido del grafo en formato xml y n3, guarda la consulta, la ejecuta y muestra el resultado.

## Resto de programas

El resto de los programas es practicamente igual, cambia un poco la complejidad pero en esencia son practicamente iguales.

## Ejemplo propuesto.

A partir del fichero rdf creado anteriormente, creamos un programa que imprima los nombres de las comidas guardadas.


    import rdflib

    if __name__=='__main__':
        g = rdflib.Graph()
        g.load("ejemplo.rdf")

        for row in g.query('select ?s where { [] foaf:name ?s .}'):
            print (row.s)


Ejecución:

    rafa@rafa-PE70-6QE:~/Imágenes/ejerciciosRDF/rdflib/ejemploRdf/sparql$ python3 ejemploSparQL.py 
    Carne
    Patatas
    PatatasConCarne









