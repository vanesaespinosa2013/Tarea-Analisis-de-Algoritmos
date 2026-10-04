# 435. Non-overlapping Intervals

## Enlace: [LeetCode 435 - Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)

**Familia:** greedy (con ordenamiento previo)  
**Idea:** minimizar las eliminaciones equivale a maximizar los intervalos que
se conservan. Se ordenan por fin y se recorren una vez; el criterio local es
conservar el intervalo que termina primero, pues deja más espacio para los
siguientes. Si el inicio actual es < al fin del último conservado, se
solapan y se descarta el actual (cuenta como eliminado); si no, se
conserva y se actualiza el fin.  
**Complejidad:** tiempo O(n log n) por el ordenamiento (el barrido es O(n)),
con n = número de intervalos; espacio O(1) adicional (O(log n) por la pila
del sort, según la implementación).

## Evidencia

![Enunciado — Non-overlapping Intervals](Non-overlapping%20Intervals%20-%20Enunciado.png)

![Accepted — Non-overlapping Intervals](Non-overlapping%20Intervals%20-%20Accepted.png)