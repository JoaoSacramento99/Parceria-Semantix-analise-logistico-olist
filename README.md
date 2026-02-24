# 📊 Análise de Desempenho Logístico e Satisfação do Cliente — Olist

## 🧠 Introdução do Projeto

Este projeto tem como objetivo analisar o **desempenho logístico de entregas** em um e-commerce brasileiro, avaliando **atrasos, tempo médio de entrega e o impacto na satisfação do cliente**.

A análise foi desenvolvida a partir de **dados reais do Olist**, utilizando **engenharia de dados, análise exploratória e visualização interativa**, com foco em gerar **insights claros e acionáveis** para apoiar a tomada de decisão operacional.

---

## 📊 Coleta de Dados

Os dados utilizados são públicos e foram obtidos a partir do dataset:

**Brazilian E-Commerce Public Dataset by Olist (Kaggle)**  
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

### Arquivos CSV utilizados

**Dados brutos**
- olist_orders_dataset.csv  
- olist_customers_dataset.csv  
- olist_order_reviews_dataset.csv  

**Dados tratados (gerados no projeto)**
- pedidos_reviews_clientes.csv  
- agg_regiao_entrega.csv  

Os dados contêm informações anonimizadas sobre pedidos, clientes, entregas, avaliações e localização geográfica.

---

## 🧱 Modelagem e Tratamento dos Dados

O processamento dos dados foi realizado em duas etapas principais:

### Engenharia de Dados (PySpark)
- Integração das tabelas de pedidos, clientes e avaliações  
- Padronização de campos de data  
- Cálculo do tempo real de entrega  
- Classificação de pedidos entregues no prazo e com atraso  
- Remoção de registros inconsistentes e duplicados  
- Geração de bases consolidadas para análise  

### Análise Exploratória (Pandas)
- Estatísticas descritivas  
- Comparação regional de métricas logísticas  
- Análise de volume de pedidos  
- Relação entre atraso de entrega e avaliação do cliente  

---

## 📈 Visualização dos Resultados

Os resultados finais foram consolidados em um **dashboard interativo desenvolvido no Google Looker Studio**, permitindo a exploração dos dados por período, região e status da entrega.

Dashboard interativo:  
https://lookerstudio.google.com/reporting/637370fb-275d-44bd-a9d9-391636306fd7

---

## 📌 Conclusões

- Regiões com maior volume de pedidos não necessariamente apresentam maior taxa de atraso  
- Atrasos de entrega tendem a impactar negativamente a avaliação dos clientes  
- Existem diferenças significativas no desempenho logístico entre regiões  
- Métricas percentuais devem ser analisadas em conjunto com volume para evitar vieses  
- A análise temporal permite identificar períodos críticos de aumento de atrasos  
