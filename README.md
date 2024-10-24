# Cálculo de Engajamento

## Visão Geral

Este documento descreve a lógica utilizada para calcular diferentes tipos de engajamento com base em métricas específicas. As métricas avaliadas incluem:

- **Engajamento de Abertura**
- **Engajamento de Click-Through**
- **Engajamento de Click-to-Open**
- **Engajamento de Resposta**

Cada métrica é calculada comparando taxas específicas com limiares predefinidos, resultando em uma pontuação de engajamento que reflete o desempenho relativo.

## Métricas de Engajamento

### 1. Engajamento de Abertura

**Definição:** Mede o percentual de destinatários que abriram a mensagem enviada.

**Limiar e Pontuação:**

| Taxa de Abertura (%) | Pontuação de Engajamento |
|----------------------|--------------------------|
| ≥ 25                 | 5                        |
| ≥ 20 e < 25          | 4                        |
| ≥ 15 e < 20          | 3                        |
| ≥ 10 e < 15          | 2                        |
| < 10                 | 1                        |

### 2. Engajamento de Click-Through

**Definição:** Mede o percentual de destinatários que clicaram em pelo menos um link presente na mensagem.

**Limiar e Pontuação:**

| Taxa de Click-Through (%) | Pontuação de Engajamento |
|---------------------------|--------------------------|
| ≥ 5                       | 5                        |
| ≥ 3 e < 5                 | 4                        |
| ≥ 2 e < 3                 | 3                        |
| ≥ 1 e < 2                 | 2                        |
| < 1                       | 1                        |

### 3. Engajamento de Click-to-Open

**Definição:** Mede o percentual de destinatários que clicaram em um link após abrir a mensagem.

**Limiar e Pontuação:**

| Taxa de Click-to-Open (%) | Pontuação de Engajamento |
|---------------------------|--------------------------|
| ≥ 50                      | 5                        |
| ≥ 40 e < 50               | 4                        |
| ≥ 30 e < 40               | 3                        |
| ≥ 20 e < 30               | 2                        |
| < 20                      | 1                        |

### 4. Engajamento de Resposta

**Definição:** Mede o percentual de destinatários que responderam à mensagem.

**Limiar e Pontuação:**

| Taxa de Resposta (%) | Pontuação de Engajamento |
|----------------------|--------------------------|
| ≥ 5                  | 5                        |
| ≥ 3 e < 5            | 4                        |
| ≥ 2 e < 3            | 3                        |
| ≥ 1 e < 2            | 2                        |
| < 1                  | 1                        |

## Processo de Cálculo

Para cada tipo de engajamento:

1. **Recebimento da Taxa:** A taxa específica (por exemplo, taxa de abertura) é calculada com base nos dados fornecidos.
2. **Comparação com Limiar:** A taxa é comparada com os limiares predefinidos na tabela correspondente.
3. **Atribuição de Pontuação:** A pontuação de engajamento é atribuída com base na faixa em que a taxa se enquadra.
4. **Pontuação Padrão:** Se a taxa não atingir nenhum dos limiares superiores, a pontuação mais baixa é atribuída.

## Exemplo de Cálculo

Considere os seguintes dados de uma campanha de email marketing:

- **Emails Enviados:** 2.028
- **Emails Abertos:** 1.131
- **Cliques:** 35

### Cálculo das Taxas

1. **Taxa de Abertura (`openRate`):**

   $$
   \text{openRate} = \left( \frac{1.131}{2.028} \right) \times 100 \approx 55,80\%
   $$

2. **Taxa de Click-Through (`clickThroughRate`):**

   $$
   \text{clickThroughRate} = \left( \frac{35}{2.028} \right) \times 100 \approx 1,73\%
   $$

3. **Taxa de Click-to-Open (`clickToOpenRate`):**

   $$
   \text{clickToOpenRate} = \left( \frac{35}{1.131} \right) \times 100 \approx 3,09\%
   $$

4. **Taxa de Resposta (`replyRate`):**

   $$
   \text{replyRate} = 0,00\%
   $$

### Determinação das Pontuações

1. **Engajamento de Abertura:**
   - **Taxa:** 55,80%
   - **Faixa:** ≥ 25%
   - **Pontuação:** 5

2. **Engajamento de Click-Through:**
   - **Taxa:** 1,73%
   - **Faixa:** ≥ 1% e < 2%
   - **Pontuação:** 2

3. **Engajamento de Click-to-Open:**
   - **Taxa:** 3,09%
   - **Faixa:** ≥ 2% e < 3%
   - **Pontuação:** 3

4. **Engajamento de Resposta:**
   - **Taxa:** 0,00%
   - **Faixa:** < 1%
   - **Pontuação:** 1

### Resumo das Pontuações

| Métrica                      | Taxa Calculada | Pontuação de Engajamento |
|------------------------------|-----------------|--------------------------|
| Engajamento de Abertura      | 55,80%          | 5                        |
| Engajamento de Click-Through | 1,73%           | 2                        |
| Engajamento de Click-to-Open | 3,09%           | 3                        |
| Engajamento de Resposta      | 0,00%           | 1                        |

## Considerações Finais

- **Interpretação das Pontuações:** Pontuações mais altas indicam melhor desempenho em cada categoria de engajamento.
- **Ações Estratégicas:** Com base nas pontuações, estratégias podem ser desenvolvidas para melhorar áreas com desempenho inferior.
- **Ajuste de Limiar:** Os limiares e pontuações podem ser ajustados conforme as necessidades específicas de cada campanha ou negócio.
