# 200. Number of Islands

## Enlace: [LeetCode 200 - Number of Islands](https://leetcode.com/problems/number-of-islands/)

**Familia:** grafos (componentes conexas en una cuadrícula)  
**Idea:** la cuadrícula se modela como un grafo implícito donde cada celda "1"
es un nodo conectado a sus 4 vecinos. Se recorre cada celda; al encontrar
una tierra sin visitar se cuenta una isla y se hace BFS para marcar toda
su componente como visitada (se hunde poniendo "0").  
**Complejidad:** tiempo O(m·n), con m = filas y n = columnas, porque cada celda
se visita y se encola a lo sumo una vez; espacio O(min(m, n)) para la cola
del BFS en el peor caso (O(m·n) si se usara DFS recursivo en una isla
serpenteante o una matriz `visited` aparte).

## Evidencia
![Enunciado — Number of Islands](Number%20of%20Islands%20-%20Enunciado.png)

![Accepted — Number of Islands](Number%20of%20Islands%20-%20Accepted.png)

