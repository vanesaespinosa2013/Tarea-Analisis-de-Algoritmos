# 39. Combination Sum

## Enlace: [LeetCode 39 - Combination Sum](https://leetcode.com/problems/combination-sum/)

### Familia: backtracking
  
**Idea:** En cada paso seleccioné un candidato y lo agregué al camino actual. Luego hice una llamada recursiva usando lo que faltaba para llegar al objetivo. Después quité el último elemento con `pop` para poder probar otras opciones. Como los números se pueden repetir, mantuve el mismo índice al hacer la llamada recursiva. También ordené los candidatos para poder detener una rama cuando el número actual ya era mayor que el valor que faltaba.

**Complejidad:** El tiempo es `O(n^(t/min))` en el peor caso, aunque con la poda se reducen las opciones que se deben revisar. El espacio es `O(t/min)` por la profundidad máxima de la recursión, donde `n` es la cantidad de candidatos, `t` es el `target` y `min` es el candidato más pequeño.

## Evidencia
![Enunciado — Combination Sum](Combination%20Sum%20-Enunciado.png)
![Accepted — Combination Sum](Combination%20Sum%20-%20Accepted.png)