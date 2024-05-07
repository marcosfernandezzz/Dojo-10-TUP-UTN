
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
Consigna: 

### Parte 1
Analizar el algoritmo “Quicksort” dado en clases, indicando paso a paso qué hace el algoritmo. ¿Se les ocurre alguna forma de implementar el algoritmo sin utilizar recursión? ¿Notan diferencias en cuanto a performance? ¿Cuáles?

[QuickSort](https://onlinegdb.com/AcAYk0fyi).
: 

### Parte 2

Ver el video de la coreografía que simula el ordenamiento de vectores y tomar nota de los pasos clave observados durante el proceso.
Basándote en la coreografía, formalizar un algoritmo que represente la estrategia utilizada para ordenar los elementos del vector.
Describir detalladamente cada paso del algoritmo, incluyendo las operaciones realizadas en cada etapa.
Realizar un análisis comparativo entre el algoritmo formalizado y otros algoritmos de ordenamiento vistos (por ejemplo, burbuja y selección).
Discutir las ventajas y desventajas del algoritmo propuesto en términos de tiempo de ejecución, número de comparaciones necesarias y complejidad en el peor caso.
Presentar las conclusiones y reflexiones sobre la efectividad y eficiencia del algoritmo propuesto en relación con los objetivos de ordenamiento.


## Codigo con ejemplos de los algoritmos Insert y Bubble
Este codigo mustra un ejemplo de como utilizar estos algoritmos y un breve ejemplo de uso.


~~~ Python (lenguaje en el que esta escrito)

def insert_sort(matriz):
    for i in range(1, len(matriz)):
        key = matriz[i]
        j = i - 1
        while j >= 0 and key < matriz[j]:
            matriz[j + 1] = matriz[j]
            j -= 1
        matriz[j + 1] = key


def bubble_sort(matriz):
    n = len(matriz)
    for i in range(n):
        for j in range(0, n - i - 1):
            if matriz[j] > matriz[j + 1]:
                matriz[j], matriz[j + 1] = matriz[j + 1], matriz[j]


# Ejemplos de uso
matriz = [64, 34, 25, 12, 22, 11, 90]
print("Array original:", matriz)
insert_sort(matriz)
print("Después de Insertion Sort:", matriz)

matriz2 = [23, 34, 89, 12, 77, 11, 90]
print("Array original:", matriz)
bubble_sort(matriz2)
print("Después de Bubble Sort:", matriz2)

~~~

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
