# 🧮 Calculadora de Créditos

Descubra quantos créditos cada chamada de API consome e quantas chamadas seu cliente consegue fazer por mês, já com a sua margem de lucro embutida.

**👉 [Abrir a calculadora](https://bittencourtthulio.github.io/calculo-creditos-revenda-tokens/)**

## Como funciona

Você vende **créditos**. A cada chamada de API, a calculadora converte o custo em dólar no preço final e em créditos consumidos.

```
preço cobrado        = (custo US$ × cotação + valor mínimo) × (1 + margem)
créditos por chamada = preço cobrado ÷ valor do crédito
chamadas por mês     = créditos do cliente ÷ créditos por chamada
```

### Configuração

| Campo | Padrão | O que faz |
| --- | --- | --- |
| Margem de lucro | 300% | Lucro sobre o custo (300% = cobra 4× o custo) |
| Valor mínimo por chamada | R$ 0,01 | Somado ao custo antes da margem, então nenhuma chamada sai de graça |
| Valor de 1 crédito | R$ 1,00 | Preço que o cliente paga por crédito |
| Cotação do dólar | R$ 5,50 | Converte o custo em US$ para R$ |

### Simulador

Informe o **custo da chamada (US$)** e os **créditos mensais do cliente**. O resultado mostra:

- quantas chamadas cabem no mês;
- preço cobrado por chamada (US$ e R$);
- créditos consumidos e lucro por chamada;
- receita, custo e lucro mensais se o cliente usar tudo.

### Exemplo

Chamada de **US$ 0,02**, com os valores padrão:

- custo em reais: R$ 0,11, mais R$ 0,01 de mínimo = R$ 0,12
- preço cobrado: R$ 0,12 × 4 = **R$ 0,48** → 0,48 crédito
- cliente com 1.000 créditos → **2.083 chamadas por mês**

## Rodar local

É um único arquivo, sem dependências. Abra o `index.html` no navegador.

## Licença

MIT
