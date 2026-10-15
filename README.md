# Capital parado no pátio: análise de gestão de estoque de uma concessionária

Análise de dados que mede quanto do capital de uma concessionária está imobilizado em estoque, qual parcela está parada há tempo demais e que tipo de veículo trava esse dinheiro — a partir de um relatório de estoque real, anonimizado.

> **Pergunta de negócio:** Quanto do capital da loja está imobilizado em estoque, qual parcela está parada há tempo demais, e que tipo de veículo trava esse dinheiro?

---

## Principais resultados

- **R$ 8,3 milhões imobilizados em estoque** (nos 123 veículos com preço anunciado), sendo mais de 90% concentrados nos carros — as motos, apesar de metade das unidades, pesam pouco no capital.
- **38% do capital — cerca de R$ 3,2 milhões — está parado há mais de 180 dias.** É caixa travado que poderia estar girando.
- **Os ex-locados ficam parados quase um ano em média,** bem acima do estoque normal. A loja opera uma locadora: compra o 0km, fatura com ele na locação e depois o transfere para a venda — então esse carro já rendeu na primeira vida. O problema não é tê-lo, e sim a eficiência da revenda.
- **Repasse não é o problema:** ao contrário do senso comum, carros de repasse giram praticamente no mesmo ritmo que o estoque normal.
- Mesmo com a locadora rendendo antes, **manter 38% do capital parado trava o giro** — e varejo de veículo depende de giro. Recomendação: uma régua de precificação do ex-locado ancorada na quilometragem de saída da frota (na operação, ~30 mil km), para fechar o ciclo rápido e liberar caixa.

## Metodologia

1. **Extração** — o relatório de estoque veio em PDF; os dados foram extraídos de forma programática (pdfplumber) para um CSV estruturado.
2. **Anonimização e limpeza** — nomes das lojas substituídos por "Loja 1/2/3"; identificadores sensíveis (placa e RENAVAM) removidos por completo; códigos internos também não são necessários na versão pública; marcação de veículos "ex-locado" e "repasse" como atributos de análise.
3. **Análise** — distribuição do capital por tipo (carro × moto) e faixa de preço; capital por tempo em estoque (aging); ranking de encalhe e comparação por origem (normal / repasse / ex-locado); curva de preço por ano-modelo; mix de marcas.

## Stack técnico

- **Python** — pandas, numpy
- **Extração de PDF** — pdfplumber
- **Visualização** — matplotlib
- **Ambiente** — Jupyter Notebook

## Como executar

```bash
git clone https://github.com/thamires-siriustech/estoque-concessionaria-lucas-do-rio-verde.git
cd estoque-concessionaria-lucas-do-rio-verde
pip install -r requirements.txt
jupyter notebook analise_estoque_concessionaria.ipynb
```

Mantenha o notebook e o CSV na mesma pasta. No Jupyter, use **Kernel → Restart & Run All**.

## Estrutura do repositório

```
estoque-concessionaria-lucas-do-rio-verde/
├── analise_estoque_concessionaria.ipynb   # análise completa
├── estoque_lucas.csv                       # dataset anonimizado (184 veículos)
├── requirements.txt
└── README.md
```

## Sobre os dados e privacidade

Os dados são reais, de um relatório de estoque de 03/08/2026, mas foram **anonimizados**: nomes de loja substituídos por Loja 1/2/3 e identificadores sensíveis (placa e RENAVAM) removidos. Não há dado de custo, margem ou cliente — apenas o preço de venda anunciado. O PDF original contém identificadores e não deve ser publicado. 61 veículos estão sem preço ("Consulte") e ficam de fora das análises de valor. O CSV apresenta linhas integralmente repetidas após a anonimização; elas não são removidas automaticamente, pois podem corresponder a unidades distintas. A deduplicação exige validação com a fonte original. Não há quilometragem, então a depreciação é analisada por ano-modelo.

Um detalhe do modelo de negócio é essencial para ler os resultados: a loja opera uma **locadora**. Compra veículos 0km, fatura com eles na locação (rodando por volta de 30 mil km) e depois os transfere para o estoque de venda. Por isso o veículo "ex-locado" chega ao pátio já tendo rendido na primeira vida — a análise trata o capital parado nesse grupo como uma questão de eficiência da revenda, não de prejuízo. A rodagem de ~30 mil km é conhecida pela operação, não está no relatório.

---

**Autora:** Thamires Martins da Silva
Projeto de portfólio em análise de dados — parte 1 de 2 (estoque; a parte 2 trata de equipe de vendas e comissionamento).
