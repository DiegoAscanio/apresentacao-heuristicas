<style scoped>
    h2 {
        font-size: 18pt;
    }
    section {
        font-size: 16pt;
    }
</style>

## Consideracoes Finais - Contribuições _off-label_

- Avanço de _draws_ em custo lg(k) em RNGs congruenciais permitiu paralelizar a geração das instâncias de teste.
- Permitiu também fazer inferências e simulações com base em amostragem estatística - _Lazy Simulation_.
    - Pois, a partir de uma semente inicial, se eu consigo avançar o RNG k iterações em custo lg(k), logo, eu gero a k-ésima amostra em custo lg(k).

- Se em uma população de n-elementos, eu consigo fazer inferências estatísticas com k amostras, $k << n$, então, eu consigo fazer $k * lg(k) << n$ simulações que servem para inferir sobre toda a população.
  - Conceito emprestado lá das linguagens funcionais - _lazy evaluation_ - avaliar o dado quando estritamente necessário, ao menos um trabalho na literatura — [(SMITH et al., 1998)](#referencias) — chama de _Lazy Simulation_.

## Trabalhos Futuros

- Parametrizar no iRace
- Implementar o genético
- Implementar a busca tabu
