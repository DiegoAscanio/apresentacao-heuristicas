<style scoped>
    h2 {
        font-size: 18pt;
    }
    section {
        font-size: 14pt;
    }
</style>

## Meta Heurística Populacional - Algoritmo Genético

Proposta de implementar um AG com as seguintes características:

- Genes ternários (-1, 0, 1) (movimentos respectivos de subtração, manutenção e adição de uma unidade em uma quantia)
- Cromossomos de tamanho $n$
- Indivíduos que representam movimentos possíveis para ir de uma solução a outra
- Seleção por rolamento de roleta
- Cruzamento gene a gene com probabilidade de 50% de escolha de um dos ascendentes
- Mutação de gene(s) com probabilidade parametrizável
- Elitismo de ao menos metade dos melhores indivíduos
- Aplicação cumulativa dos movimentos selecionados às soluções da população para inicialização da próxima geração.

</div>
</div>
