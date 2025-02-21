<style scoped>
    section {
        font-size: 14pt;
    }
</style>

## Representação do Problema

Cada instância do problema é caracterizada por:

1. Um vetor de cotações (_odds_) de tamanho \\(n\\) onde \\(n\\) é a quantidade de possíveis resultados disjuntos do evento esportivo.
2. Um montante \\(M\\) disponível para apostas.

## Representação da Solução

A solução \\(s_\\text{LR}\\) — solução sem restrições de integralidade (linearmente relaxada) — é um vetor dado pela resolução do problema como um problema de decisão a partir de um sistema linear de \\(n\\) variáveis \\(s_{i}, i = 1, 2, \ldots, n\\) que têm como valores:

\\[
s = \\left[
    \\frac{M}{\\text{odds}\_{1} \\cdot \\sum_{i=1}^{n} \\frac{1}{\\text{odds}\_{j}}}, \\ 
    \\frac{M}{\\text{odds}\_{2} \\cdot \\sum_{i=1}^{n} \\frac{1}{\\text{odds}\_{j}}}, \\ 
    \\ldots, \\ 
    \\frac{M}{\\text{odds}\_{n} \\cdot \\sum_{i=1}^{n} \\frac{1}{\\text{odds}\_{j}}}
\\right]
\\]

É possível observar que esta solução, do problema de decisão, pode ser obtida em tempo computacional da ordem de \\(O(n)\\). Considerando a adição de restrições de integralidade, o problema perde esta característica, por se tornar NP-difícil e em instâncias maiores do que 1024 eventos disjuntos, _solvers_ de programação linear consolidados (como o scipy) já começam a demandar tempo computacional considerável, o que justifica a adoção de estratégias heurísticas.
