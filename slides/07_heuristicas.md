<style scoped>
    section {
        font-size: 16pt;
    }
</style>

## Heurísticas - Critério Guloso

Testes estatísticos realizados comparando soluções exatas inteiras e linearmente relaxadas das instâncias do problema demonstraram que \\(100 \\% \\pm 5\\%\\) das soluções ótimas inteiras pertenciam ao intervalo \\(\\left[\\lfloor S\_{LR} \\rfloor, \\lfloor S\_{LR} \\rfloor + 1\\right]\\) com relevância estatística de \\(99\\%\\).

Entretanto, um erro metodológico ínfimo, porém crucial, foi cometido: o esquecimento da troca de sinal do vetor de coeficientes da função objetivo para resolver o problema desejado de maximização nos solvers que por padrão resolvem problemas de minimização! Um simples caracterer `-` no código fonte do solver foi o suficiente para causar este erro. Porém, como as folgas de integralidade (causadas pela diminuição dos retornos mínimos esperados para cada evento) são muito pequenas, a resolução do problema como uma versão de maximização produziu resultados bastante aceitáveis, também, pelo fato de que o problema original sendo um problema de decisão, fazem com que as soluções de miniimização e maximização sejam equivalentes. Portanto, se a folga de integralidade é pequena, logo, a solução de maximização não está muito distante da solução ótima de minimização.
