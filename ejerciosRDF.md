
# Autor: Rafael Egea Jurado

## Fallos encontrados
- En algunos ejercicios, hemos encontrado que los print, no usan () por lo tanto daban fallo al ejecutar con la nueva versión de python. Simplemente los hemos añadido
los parentesis. 

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
Creamos un ejercicio que parsee un fichero.

    from rdflib import Graph

    g = Graph()
    g.parse("http://bigasterisk.com/foaf.rdf", format="turtle")

    print(len(g))

    import pprint
    for stmt in g:
        print(stmt)


