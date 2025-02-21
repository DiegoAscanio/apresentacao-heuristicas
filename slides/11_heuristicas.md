<style scoped>
    h2 {
        font-size: 18pt;
    }
    section {
        font-size: 14pt;
    }
</style>

## Meta Heurística de Busca Local Probabilística - _Simulated Annealing_

Implementada em [python](https://raw.githubusercontent.com/DiegoAscanio/TP-heuristicas/refs/heads/main/passo_05_solucoes_heuristicas.py) sobre o pseudo-código estudado em sala de aula, com os movimentos de exploração de vizinhança usados na heurística construtiva.

- Apenas uma pequena modificação na função de resfriamento, para considerar tanto \\(\\alpha\\) quanto \\(\\gamma\\) como parâmetros de resfriamento:

\\[
T_{k+1} = \\alpha \\cdot \\frac{T\_k}{ 1 + \\gamma \\cdot \\sqrt{T\_k}}
\\]
