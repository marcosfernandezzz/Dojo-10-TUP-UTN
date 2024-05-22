
# Documentación Dojo 10
![Markdown](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1200px-Markdown-mark.svg.png)


## Integrantes 
- Franco Mancilla
- Joaco Freyre
- Lorenzo Gomez Martins
- Marcos Fernandez
- Sebastian H. Amaral

# Proyecto: Trabajo Práctico Ordenamiento

## Descripción
### Consigna: 

### Parte 1
Analizar el algoritmo “Quicksort” dado en clases, indicando paso a paso qué hace el algoritmo. ¿Se les ocurre alguna forma de implementar el algoritmo sin utilizar recursión? ¿Notan diferencias en cuanto a performance? ¿Cuáles?

[QuickSort](https://onlinegdb.com/AcAYk0fyi).
: 


### Parte 2

- Ver el video de la coreografía que simula el ordenamiento de vectores y tomar nota de los pasos clave observados durante el proceso.
- Basándote en la coreografía, formalizar un algoritmo que represente la estrategia utilizada para ordenar los elementos del vector.
- Describir detalladamente cada paso del algoritmo, incluyendo las operaciones realizadas en cada etapa.
- Realizar un análisis comparativo entre el algoritmo formalizado y otros algoritmos de ordenamiento vistos (por ejemplo, burbuja y selección).
- Discutir las ventajas y desventajas del algoritmo propuesto en términos de tiempo de ejecución, número de comparaciones necesarias y complejidad en el peor caso.
- Presentar las conclusiones y reflexiones sobre la efectividad y eficiencia del algoritmo propuesto en relación con los objetivos de ordenamiento.

## Parte 1
Pasos del algoritmo "Quicksort":
1_ Se crea la funcion swap, la cual devuelve una tupla con los valores de a y b intercambiados
2_ Se crea la funcion particionar, a la cual se le pasan 3 parametros: un array, el minimo y el maximo.
a. Se define un pivote dentro de un array, el cual corresponde al ultimo elemento del mismo.
b. Define el indice i como el indice que está anterior al minimo.
c. Se crea un bucle for que va desde el minimo hasta el maximo -1 (ya que es un "desde" inclusivo y un "hasta" exclusivo)
d. Compara el elemento j del array. Si este es menor o igual al pivote establecido, ejecuta el siguiente codigo: aumenta el indice i en uno, e intercambia los lugares de los elementos en la posicion i y j
e. Luego, coloca el pivote en su posicion correcta, quedando asi este ordenado definitivamente, y dejando a su izquierda un subarreglo con elementos mas pequeños que su valor, y a su derecha un subarreglo con elementos mas grandes que su valor
f. Por ultimo, retorna la posicion final del pivote.

2_ Se define la funcion quick_sort, a la cual se le brindan nuevamente los parametros del array, minimo y maximo.
a. Se agrega un condicional, el cual compara si el minimo es menor al maximopara determinar si hay un subarreglo que necesita ser ordenado.
b. En caso de ser verdadero, llama a la funcion particionar para obtener el indice de particion, y lo almacena en la variable "pi".
c. Por ultimo, ordena los subarreglos de la izquierda y derecha del pivote.

Sinceramente no hemos logrado descubrir como realizar un algoritmo de ordenamiento QuickSort sin utilizar recursiividad.

## Parte 2:

a.Paso a paso del video:

Insertion sort pasos:
1. Se ordena de izquierda a derecha (en el video esta en modo espejo)
2. Se compara el primer numero con el segundo; si el primero es mayor al segundo, intercambian valores.
3. Ahora, el "nuevo" elemento de la segunda posicion se compara con el tercero, y asi sucesivamente.
4. Los valores ordenados van quedando del lado izquierdo, y en caso de pasar a un nuevo elemento (aumentando el indice) se lo compara con todos los anteriores.
5. El algoritmo termina cuando ya se hayan comparado todos los numeros de la izquierda con el elemento del indice actual.


b. Codigo del algoritmo InsertSort: 

Este codigo mustra un ejemplo de como utilizar este algoritmo y un breve ejemplo de uso.

~~~ Python (lenguaje en el que esta escrito)

def insert_sort(matriz):
    for i in range(1, len(matriz)):
        key = matriz[i]
        j = i - 1
        while j >= 0 and key < matriz[j]:
            matriz[j + 1] = matriz[j]
            j -= 1
        matriz[j + 1] = key


# Ejemplos de uso
matriz = [64, 34, 25, 12, 22, 11, 90]
print("Array original:", matriz)
insert_sort(matriz)
print("Después de Insertion Sort:", matriz)

~~~

c. Paso a paso del InsertSort:
1. Se define la funcion y se le pasa una lista como parametro.
2. Se crea un bucle for, el cual va desde el segundo elemento de la lista hasta el ultimo elemento de la misma.
3. Se guarda el elemento que vamos a comparar en la variable "valor"
4. Se define el indice j como el anterior a i
5. Se crea un bucle el cual se va a ejecutar solo si j no es menor a 0 (para que no se vaya de rango) y si el elemento anterior al que estamos comparando es mayor al valor actual.
6. Si la condicion es verdadera, desplaza los elementos mayores que el valor actual a un espacio a la derecha para dejar espacio para "rellenar" el valor actual.
7. Se decrementa el valor del indice j para seguir buscando la posicion correcta para el valor.
8. Por ultimo, se inserta el valor en la posicion correcta y se retorna la lista ordenada.


## :snake: Link al proyecto
- [proyecto]()
## :tv: Link al video del proceso
- [video]()

---
### Fuentes

- [Lenguaje Markdown](https://markdown.es/sintaxis-markdown/#linkauto).

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

- [Tutorial](https://youtu.be/EdJixU5IDgQ).

- [Emojis](https://gist.github.com/rxaviers/7360908).

---
