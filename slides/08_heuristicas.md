<style scoped>
    section {
        font-size: 12pt;
    }
</style>

## Heurísticas - Critério Guloso

Porque o erro metodológico de esquecer o sinal de **-** foi relatado? Porque isso aqui é ciência! E todo resultado deve ser apresentado! Mesmo que errado, por pouco, mas, para quem for reproduzir, fica a lição de prestar bastante atenção a estes pequenos detalhes que possam passar despercebidos.

Destarte, pelo fato do problema original ser de decisão, de igualdade, das distâncias entre soluções de maximização e minimização serem pequenas quando introduzidas pequenas folgas de integralidade e pelo grande número de soluções que pertencem ao intervalo apresentado no slide anterior, foi escolhido como critério guloso utilizar o arredondamento para baixo da solução linearmente relaxada do problema de arbitragem, obtida em tempo $O(n)$ como solução inicial para os algoritmos heurísticos construídos.

Logo:

\\[s\_{0} = \left\lfloor S\_\\text{LR} \right\rfloor\\]

Mas, nem sempre soluções inteiras poderão ser obtidas, pois, as restrições das instâncias nem sempre serão satisfeitas.

Portanto, toda solução heurística começará com:

\\[
    S^{\*} = \\overset{\\rightarrow}{0} \\\\
    Z^{\*} = 0
\\]

E, a partir daí, serão feitas operações em buscas de novas soluções para \\(S^{\*}\\) e \\(Z^{\*}\\) que mantenham factibilidade. Se nenhuma solução for encontrada, a solução trivial resolve o problema sem acarretar prejuízos ao apostador.
