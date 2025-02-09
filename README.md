# Reto_09

---
**Nota:** Los ejercicios del 1-3 se encuentran en el notebook anexo a este repositorio

---
#### 4. Revisar que son los algoritmos de sorting, entender bubble-sort (enlace a implementación).


#### • Algoritmos de Sorting (Clasificación)
Los algoritmos de sorting son métodos utilizados para organizar elementos de una lista o arreglo en un orden específico, generalmente ascendente o descendente. Son fundamentales en informática, ya que optimizan operaciones como búsquedas y análisis de datos.

#### • Bubble Sort (Ordenamiento de Burbuja)
Es un algoritmo simple de clasificación que compara y intercambia repetidamente elementos adyacentes si están en el orden incorrecto. Su nombre deriva del movimiento de los elementos más grandes "subiendo" hacia su posición correcta, similar a burbujas.

#### Pasos del Bubble Sort:

* Comparación y intercambio: Recorre la lista comparando pares de elementos adyacentes.

* Si el elemento actual es mayor que el siguiente, se intercambian.

Repetición: El proceso se repite hasta que no se requieren más intercambios, indicando que la lista está ordenada.

Ejemplo:
Para el arreglo `[5, 3, 8, 4, 2]`:

Primer pasada:

`[3, 5, 4, 2, 8]` (el 8 llega al final).

Segunda pasada:

`[3, 4, 2, 5, 8]` (el 5 se posiciona).

Tercera pasada:

`[3, 2, 4, 5, 8]` (el 4 se posiciona).

Cuarta pasada:

`[2, 3, 4, 5, 8]` (lista ordenada).


* Implementación en Python (Optimizada):

```
python
Copy
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr
```

* Ventajas y Desventajas:

✅ Simple: Fácil de entender e implementar.

✅ Estable: Mantiene el orden de elementos iguales.

✅ Eficiente en pequeños conjuntos de datos o listas casi ordenadas.

❌ Ineficiente: No recomendado para datos grandes debido a O(n²).

*Variante: Cocktail Shaker Sort (recorre la lista en ambas direcciones), pero mantiene complejidad O(n²).*

* ## Conclusión
Bubble Sort es ideal para propósitos educativos o pequeñas listas. Sin embargo, en aplicaciones prácticas con datos extensos, se prefieren algoritmos más eficientes como Quick Sort o Merge Sort.
