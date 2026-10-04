# 1143. Longest Common Subsequence

# Enlace: [LeetCode 1143 - Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)

**Familia:** programación dinámica (DP en tabla 2D)  
**Idea:** estado `dp[i][j]` = longitud de la LCS entre los primeros `i`
caracteres de `text1` y los primeros `j` de `text2`. Si
`text1[i-1] == text2[j-1]`, entonces `dp[i][j] = dp[i-1][j-1] + 1`; si no,
`dp[i][j] = max(dp[i-1][j], dp[i][j-1])`. Como cada fila solo depende de la
anterior, se guardan únicamente dos filas.  
**Complejidad:** tiempo O(m·n), con m = len(text1) y n = len(text2), porque se
llena cada celda de la tabla una vez; espacio O(min(m, n)) al conservar solo
dos filas sobre la cadena más corta (O(m·n) con la tabla completa).

# Evidencia
![Enunciado — Longest Common Subsequence](Longest%20Common%20Subsequence%20-%20Enunciado.png)

![Accepted — Longest Common Subsequence](Longest%20Common%20Subsequence%20-%20Accepted.png)