# Case Técnico — Análise de Dados (Operations)

## 🎯 Objetivo

Realizar a limpeza, tratamento e análise de uma base de dados de oportunidades comerciais, com o objetivo de gerar insights sobre receita, pipeline e eficiência do funil de vendas.

---

## 🧠 Abordagem

O trabalho foi dividido em três etapas principais:

1. Auditoria e limpeza dos dados
2. Análise exploratória
3. Geração de insights e recomendações

A base original foi analisada com apoio de ferramentas de IA, com validação manual das correções para garantir consistência.

---

## 🧹 1. Tratamento de Dados

### Principais problemas encontrados:

* Inconsistências em campos categóricos (Lead Source, Stage, Lead Office)
* Erros de digitação e variações de escrita
* Divergência entre `Amount` e `Total_Product_Amount`
* Duplicações causadas pela granularidade por produto
* Registros fora do escopo de análise
* Datas inconsistentes (ex: fechamento antes da criação)
* Valores negativos em métricas de tempo

---

### Ações realizadas:

* Padronização de textos (remoção de espaços, correção de grafia)
* Criação da coluna `Lead_Source_Category` para normalização
* Recalculo do `Amount` com base em `Total_Product_Amount`
* Uso de `Opportunity_ID` como chave única para evitar duplicidade
* Criação de colunas auxiliares:

  * `month_year`
  * `sales_cycle_days`
  * `pipeline_age_days`
* Exclusão de registros fora do escopo definido no case
* Tratamento de inconsistências de datas e valores

---

## 📊 2. Análise de Dados

As principais análises realizadas foram:

* Receita Closed Won ao longo do tempo (MoM)
* Participação por Lead Source
* Win rate por Lead Source
* Pipeline aberto por Stage
* Mix entre New Business e Upsell
* Ticket médio por Type
* Top 10 oportunidades abertas
* Top 10 clientes Closed Won
* Ciclo de vendas médio por Lead Office
* Distribuição da idade do pipeline (histograma)

---

## 💡 3. Principais Insights

* Concentração de receita em poucos clientes (risco de dependência)
* Customer Success como principal canal de geração de receita
* Pipeline com concentração em estágios intermediários
* Existência de oportunidades com mais de 180 dias em aberto
* Diferença relevante no ciclo de vendas entre regiões

---

## ⚙️ Recomendações

* Padronização automática de campos no CRM
* Validação obrigatória de datas e valores
* Definição de campos obrigatórios para oportunidades
* Monitoramento contínuo da qualidade dos dados
* Uso de dashboards para acompanhamento do pipeline

---

## 📦 Entregáveis

* `opps_corrigido.xlsx` → base tratada
* `relatorio_erros.html` → auditoria dos dados
* `analise.html` → análises e visualizações
* `apresentacao.pdf` → resumo executivo
* `/imagens` → gráficos utilizados na análise

---

## 🤖 Uso de IA

A IA foi utilizada para:

* Identificação de padrões de erro na base
* Apoio na estruturação das análises
* Sugestão de fórmulas e organização do processo

Todas as saídas foram validadas manualmente para garantir precisão.

---

## 📌 Observações

Algumas inconsistências foram tratadas apenas no contexto analítico, respeitando a estrutura original da base.

---

## 🚀 Conclusão

A qualidade dos dados impacta diretamente a confiabilidade das análises.
Após o tratamento, foi possível gerar insights relevantes sobre o pipeline comercial e identificar oportunidades de melhoria no processo de vendas.
