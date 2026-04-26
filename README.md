# Case Técnico - Análise de Dados

## Objetivo
Realizar a limpeza, tratamento e análise de uma base de dados de oportunidades comerciais, identificando padrões relevantes e gerando insights sobre o desempenho do funil de vendas.

---

## Abordagem

O trabalho foi dividido em três etapas principais: tratamento de dados, análise e geração de insights.

---

## 1. Tratamento de Dados

Inicialmente, foi realizada uma análise exploratória da base para identificar inconsistências.

### Principais problemas encontrados:
- Inconsistências em campos textuais (Lead Source, Account Name, Opportunity Name)
- Erros de digitação em estágios
- Dados ausentes em campos financeiros
- Problemas no formato de datas
- Registros com valores negativos ou inconsistentes nos cálculos

### Ações realizadas:
- Padronização textual (remoção de espaços, ajuste de caixa e correção de erros)
- Criação da coluna `Lead_Source_Category` para agrupamento das origens
- Recalculo do campo `Amount` com base na soma dos produtos
- Ajuste do formato de datas para permitir cálculos corretos
- Criação de colunas auxiliares:
  - `month_year`
  - `sales_cycle_days`
  - `pipeline_age_days`

### Tratamento de inconsistências:
- Registros com datas inconsistentes (ex: fechamento antes da criação) foram desconsiderados nos cálculos
- Valores negativos e ciclos iguais a zero foram removidos das análises para garantir consistência

---

## 2. Análise de Dados

Foram desenvolvidas análises para avaliar o desempenho comercial:

- Revenue over time
- Lead source distribution
- Win rate by lead source
- Pipeline distribution by stage
- Mix New Business vs Upsell
- Average ticket
- Top clients
- Pipeline age

---

## 3. Principais Insights

- Receita concentrada em poucos clientes estratégicos
- Diferença de performance entre canais de aquisição
- Pipeline com oportunidades com tempo elevado em aberto
- Possíveis gargalos em estágios intermediários do funil

---

## Entregáveis

- `opps_corrigido.xlsx` → base tratada
- `relatorio_erros.html` → descrição dos problemas identificados
- `analise.html` → análise dos dados e insights
- `apresentacao.pdf` → resumo visual da análise

---

## Observações

Durante o processo, algumas inconsistências foram mantidas na base original, sendo tratadas apenas no contexto analítico, a fim de preservar a integridade dos dados.
