# 200. Number of Islands

## Enlace: [LeetCode 200 - Number of Islands](https://leetcode.com/problems/number-of-islands/)

### Familia: Grafos  

**Idea:** Representé la cuadrícula como un grafo, donde cada `1` es un nodo que se conecta con las celdas de arriba, abajo, izquierda y derecha. Cada isla es un grupo de celdas conectadas. Por eso, recorrí la matriz y, cuando encontré una celda de tierra que no había visitado, sumé una isla y utilicé BFS para recorrer y marcar todas las celdas que pertenecían a ella, evitando contarlas de nuevo.

**Complejidad:** El tiempo es `O(m * n)`, porque cada celda se visita como máximo una vez. El espacio es `O(min(m, n))` por la cola del BFS, donde `m` es la cantidad de filas y `n` la cantidad de columnas.

## Evidencia
![Enunciado — Number of Islands](Number%20of%20Islands%20-%20Enunciado.png)

![Accepted — Number of Islands](Number%20of%20Islands%20-%20Accepted.png)

