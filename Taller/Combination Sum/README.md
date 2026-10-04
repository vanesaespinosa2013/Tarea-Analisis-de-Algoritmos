# 39. Combination Sum

## Enlace: [LeetCode 39 - Combination Sum](https://leetcode.com/problems/combination-sum/)

**Familia:** backtracking  
**Idea:** se ordenan los candidatos y se explora un árbol de decisiones. En
cada paso se elige un candidato desde el índice `start` (se agrega a
`path`), se recurre con `remaining - c` pasando el mismo índice `i` para
permitir repetirlo, y luego se deshace (`path.pop()`). Avanzar solo hacia
adelante evita combinaciones duplicadas, y como el arreglo está ordenado se
poda con `break` cuando `c > remaining`. Al llegar a `remaining == 0` se
guarda una copia de la combinación.  
**Complejidad:** tiempo O(n^(t/min)) en el peor caso, con n = número de
candidatos, t = target y min = menor candidato (la profundidad máxima del
árbol es t/min); en la práctica es mucho menor por la poda, y a eso se suma
O(k·t/min) por copiar las k combinaciones válidas. Espacio O(t/min) por la
pila de recursión y `path` (sin contar la salida).

## Evidencia
![Enunciado — Combination Sum](Combination%20Sum%20-Enunciado.png)
![Accepted — Combination Sum](Combination%20Sum%20-%20Accepted.png)