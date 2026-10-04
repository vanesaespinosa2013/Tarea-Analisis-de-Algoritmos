# 1143. Longest Common Subsequence

# Enlace: [LeetCode 1143 - Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)

### Familia: Programación dinámica

**Idea:** Definí `dp[i][j]` como la longitud de la subsecuencia común más larga entre los primeros `i` caracteres de `text1` y los primeros `j` de `text2`. Si los caracteres son iguales, sumé 1 al resultado de `dp[i-1][j-1]`. Si son diferentes, tomé el mayor entre `dp[i-1][j]` y `dp[i][j-1]`. Para ahorrar memoria, utilicé solo dos filas, ya que cada una depende de la anterior.

**Complejidad:** El tiempo es `O(m * n)`, porque se calcula cada posición de la tabla una sola vez. El espacio es `O(min(m, n))`, porque solo se necesitan dos filas para realizar los cálculos, donde `m` y `n` son las longitudes de cada texto.

# Evidencia
![Enunciado — Longest Common Subsequence](Longest%20Common%20Subsequence%20-%20Enunciado.png)

![Accepted — Longest Common Subsequence](Longest%20Common%20Subsequence%20-%20Accepted.png)