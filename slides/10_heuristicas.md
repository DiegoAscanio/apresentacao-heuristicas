<style scoped>
    h2 {
        font-size: 18pt;
    }
</style>

## Heurísticas Construtivas - Heurística Construtiva Com Critério Guloso

```python
import numpy as np
def heuristica_construtiva_com_criterio_guloso(M, odds, B, biased = True):
    """
        Parâmetros:
            M: quantia disponível para apostas
            odds: vetor de odds
            B: retornos mínimos esperados
        Retorna:
            s*: melhor solução encontrada
            z*: valor da melhor solução encontrada
    """
    ponto_de_partida = construir_solucao_inicial(M, odds)
    n = len(odds)
    s_star = np.zeros(n)
    z_star = 0
    # instancia conjunto C de candidatos que contém:
    #   - nenhuma intervenção nas quantias determinadas pelo ponto de partida
    #   - N intervenções aleatórias enviesadas (ou não) para poucas quantidas
    #     de apostas
    for i, candidato in enumerate(candidates_generator(n, n, biased = biased)):
        s = ponto_de_partida + candidato if np.random.random() < 0.5 else ponto_de_partida - candidato
        z = np.dot(s, odds) / n # valor medio
        feasible_solution = np.all(s * odds >= B) and np.sum(s) <= M
        if z > z_star and np.sum(s) <= M and feasible_solution:
            s_star = s
            z_star = z
            ponto_de_partida = s
    return s_star, z_star
```
