# Evolução do estoque — agosto a outubro de 2026

## Pergunta de negócio

Como mudou o estoque registrado entre 03/08/2026 e 15/10/2026, e qual é a concentração do valor anunciado nos itens com mais de 180 dias em pátio?

## Escopo de locação

Os indicadores de idade e valor abaixo descrevem os registros listados no relatório, inclusive marcações de locação. A operação informou que há **3 carros ex-locados disponíveis para venda**; os demais registros marcados como LOCADO continuam em locação. Como ainda não existe correspondência segura entre os três carros confirmados e as linhas anonimizadas, os indicadores gerais não devem ser interpretados como estoque de revenda totalmente isolado.

## Indicadores principais

| Indicador | 03/08/2026 | 15/10/2026 |
|---|---:|---:|
| Registros | 184 | 163 |
| Carros / motos | 91 / 93 | 73 / 90 |
| Com preço | 123 | 150 |
| Sem preço | 61 | 13 |
| Cobertura de preço | 66,85% | 92,02% |
| Soma dos preços anunciados | R$ 8.266.200 | R$ 8.468.420 |
| Com preço e mais de 180 dias | 34 | 38 |
| Valor anunciado acima de 180 dias | R$ 3.176.580 | R$ 4.531.630 |
| Percentual do valor anunciado acima de 180 dias | 38,43% | 53,51% |

A soma considera os preços anunciados, não o custo de aquisição nem a margem. Em outubro, dois registros com preço estavam marcados como indisponíveis. Excluindo-os, 36 registros disponíveis com mais de 180 dias somavam R$ 4.194.650, equivalentes a 51,59% do valor anunciado disponível.

## Repasse: valor anunciado

| Indicador | 03/08/2026 | 15/10/2026 |
|---|---:|---:|
| Veículos de repasse com preço | 26 | 37 |
| Carros de repasse | 21 | 27 |
| Motos de repasse | 5 | 10 |
| Valor anunciado total de repasse | R$ 1.238.650 | R$ 1.699.550 |
| Valor de repasse acima de 180 dias | R$ 358.930 | R$ 663.920 |
| Repasse / soma dos preços anunciados | 14,98% | 20,07% |

Os 37 veículos marcados como repasse no relatório de outubro têm preço anunciado informado. Esse valor não representa custo de aquisição ou margem de lucro.

## Locação: classificação operacional pendente

A operação informou que há **3 carros ex-locados no estoque de revenda** e que os demais registros marcados como LOCADO seguem em locação. O relatório público tem 16 registros com a marcação LOCADO e um com LOCADORA, mas a marcação não permite identificar, sozinha, quais são os três ex-locados. Até haver pareamento seguro desses três carros com as linhas anonimizadas, não se calcula valor anunciado ou média de dias para esse subgrupo.

## Interpretação

O número de registros caiu de 184 para 163, enquanto a cobertura de preços subiu de 66,85% para 92,02%. Essa diferença de cobertura limita comparações diretas entre os valores totais e percentuais dos dois relatórios.

No relatório de outubro, 38 registros com preço superam 180 dias de pátio, representando 53,51% da soma dos preços anunciados. Excluindo registros indisponíveis, a parcela permanece relevante: 51,59% do valor anunciado dos registros com preço disponíveis.

A comparação privada dos dois relatórios identificou 120 registros correspondentes. Em 76 pares com preço informado nos dois relatórios, seis apresentaram alterações de preço, cuja variação líquida foi de -R$ 58.000. A correspondência individual não está incluída nos arquivos públicos.

## Limitações

- Os relatórios são fotografias pontuais, não uma série diária de vendas.
- Preço anunciado não equivale a custo, preço efetivo de venda, caixa ou lucro.
- A cobertura de preços é diferente entre os relatórios.
- Registros parecidos podem representar unidades distintas; não foram removidos automaticamente.
- A marcação `LOCADO` na fonte não equivale automaticamente a ex-locado; o pareamento dos três ex-locados foi deixado pendente para não inventar classificação.\n- Os arquivos públicos são anonimizados. O relatório operacional original não faz parte do repositório.

## Arquivos

- `estoque_lucas.csv`: fotografia de agosto.
- `estoque_2026-10-15_anonimizado.csv`: fotografia de outubro.
- `historico_indicadores_estoque.csv`: indicadores agregados por fotografia.
- `comparativo_estoque.ipynb`: código de análise reproduzível.
