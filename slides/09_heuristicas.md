<style scoped>
    section {
        font-size: 16pt;
    }
</style>

## Heurísticas - Métodos de exploração de vizinhança

- Adições (subtrações) unitárias aleatórias em quantidades aleatórias de quantias pertencentes a uma solução corrente.

- Adições (subtrações) unitárias aleatórias em pequenas quantidades (enviesadas por meio de roleta viciada) de quantias pertencentes a uma solução corrente.

## Heurísticas Construtivas

A heurística construtiva com critério guloso pretende explorar um espaço de busca de tamanho $O(n + 1)$ onde n representa a quantidade de eventos esportivos disjuntos.

Incia-se com um s - solução inicial nula - e, depois, \\(\\lfloor S_{\\text{LR}} \\rfloor\\). Em sequência, a cada iteração, quantias unitárias são adicionadas / subtraídas aleatoriamente de cada quantia pertencente a \\(S_{\\text{LR}}\\) de acordo com algum dos movimentos de exploração de vizinhança — mencionados acima — selecionado. Se na iteração corrente, \\(f(s) > f(s^\*)\\) então, \\(s^\* = s\\) se $s$ for factível.

Ao fim de $n + 1$ itrações, \\(s^\*\\) é retornada.
