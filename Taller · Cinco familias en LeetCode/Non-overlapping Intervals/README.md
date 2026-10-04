# 435. Non-overlapping Intervals

## Enlace: [LeetCode 435 - Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)

### Familia: greedy

**Idea:** Primero ordené los intervalos según su fin, para quedarme siempre con el que termina primero y así dejar más espacio para los siguientes. Después recorrí la lista y, si un intervalo empieza antes de que termine el último que conservé, significa que se solapan y lo elimino. De lo contrario, lo conservo y actualizo el último fin.

**Complejidad:** El tiempo es `O(n log n)` debido al ordenamiento inicial, mientras que el recorrido es `O(n)`. El espacio extra es `O(1)`, porque solo necesito guardar un contador y el fin del último intervalo conservado, donde `n` es la cantidad de intervalos.


## Evidencia

![Enunciado — Non-overlapping Intervals](Non-overlapping%20Intervals%20-%20Enunciado.png)

![Accepted — Non-overlapping Intervals](Non-overlapping%20Intervals%20-%20Accepted.png)