📊 EDA — Análise de Desempenho Logístico e Satisfação do Cliente
(Parceria Semantix)
🚀 Sobre o Projeto

Este repositório apresenta uma Análise Exploratória de Dados (EDA) aplicada ao desempenho logístico de entregas em um grande e-commerce brasileiro, integrando indicadores operacionais de entrega com avaliações de satisfação dos clientes.

O projeto foi desenvolvido no contexto acadêmico, com apoio e parceria da Semantix, e tem como objetivo demonstrar a aplicação prática de técnicas de tratamento de dados, análise exploratória e visualização, utilizando dados reais para responder a problemas de negócio relevantes, como atrasos logísticos, diferenças regionais e impacto na experiência do cliente.

📌 Problemática

Atrasos na entrega representam um dos principais desafios operacionais do e-commerce. Além de impactarem custos logísticos, esses atrasos afetam diretamente a percepção do cliente, refletida em avaliações e níveis de satisfação.

Neste projeto, buscamos responder questões como:

Onde estão concentrados os atrasos de entrega no Brasil?

Quais regiões apresentam maior percentual e maior tempo médio de atraso?

Como o volume de pedidos influencia a análise de atrasos regionais?

Existe relação entre atraso na entrega e avaliação do cliente?

Qual o impacto do desempenho logístico na satisfação do consumidor?

📁 Estrutura do Repositório
projeto-olist-logistica/
│
├── data/
│   ├── raw/                 # Dados brutos obtidos do Kaggle
│   │   ├── olist_orders_dataset.csv
│   │   ├── olist_customers_dataset.csv
│   │   └── olist_order_reviews_dataset.csv
│   │
│   └── processed/           # Dados tratados e consolidados
│       ├── pedidos_reviews_clientes.csv
│       └── agg_regiao_entrega.csv
│
├── notebooks/
│   ├── 01_etl_spark.ipynb   # Tratamento, integração e preparação dos dados (PySpark)
│   └── 02_eda_pandas.ipynb  # EDA, correlações e visualizações (Pandas)
│
├── dashboard/
│   └── looker_studio_link.txt
│
└── README.md


📊 Fonte dos Dados

Os dados utilizados foram obtidos a partir do dataset público:

Brazilian E-Commerce Public Dataset by Olist
Disponível no Kaggle:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

O dataset contém dados reais anonimizados de um e-commerce brasileiro, incluindo informações sobre pedidos, clientes, entregas, avaliações e localização geográfica.

🛠️ Tecnologias Utilizadas
Ferramenta	Finalidade
🐍 Python	Linguagem principal
⚡ PySpark	Tratamento, integração e agregações de dados
📊 Pandas	Análise exploratória e estatística
📈 Seaborn / Matplotlib	Visualizações e gráficos
📋 Looker Studio	Dashboard interativo
📌 Etapas do Projeto
1️⃣ Tratamento e Preparação dos Dados (PySpark)

Nesta etapa, os dados brutos do Kaggle foram processados utilizando PySpark, garantindo escalabilidade e boas práticas de engenharia de dados.

Principais atividades realizadas:

Leitura dos dados brutos

Padronização e tratamento de colunas de data

Integração das tabelas de pedidos e clientes

Criação de variáveis relacionadas ao tempo de entrega

Cálculo da diferença entre datas estimadas e reais de entrega

Classificação de pedidos entregues no prazo e com atraso

Tratamento da tabela de avaliações (order_reviews), incluindo:

seleção apenas das colunas relevantes (order_id e review_score)

remoção de registros nulos

tratamento de valores inconsistentes e textos inválidos

garantia de uma única avaliação por pedido

Integração das avaliações à base principal de pedidos

Geração de bases finais em formato CSV para análise e visualização

Principais datasets gerados:

pedidos_reviews_clientes.csv — base consolidada por pedido

agg_regiao_entrega.csv — métricas agregadas por região

2️⃣ Análise Exploratória de Dados (EDA — Pandas)

A partir dos dados tratados, foi realizada a análise exploratória com Pandas, focando em:

estatísticas descritivas

distribuição de atrasos

comparação regional de métricas logísticas

análise de volume de pedidos

relação entre atraso de entrega e avaliação do cliente

gráficos de correlação e dispersão para identificar padrões relevantes

Os dados agregados no PySpark foram convertidos para Pandas exclusivamente para fins de visualização.

3️⃣ Dashboard Interativo (Looker Studio)

Com a base final consolidada, foi construído um dashboard no Looker Studio com foco em:

KPIs de desempenho logístico

comparação entre regiões

percentual de pedidos atrasados e no prazo

análise de satisfação do cliente

suporte visual à tomada de decisão

📈 Principais Insights Esperados

Regiões com maior volume de pedidos nem sempre apresentam maior percentual de atraso

Atrasos de entrega tendem a impactar negativamente a avaliação dos clientes

Existe variação significativa no desempenho logístico entre regiões

Métricas agregadas são fundamentais para evitar interpretações enviesadas por volume

🤝 Agradecimentos

Este projeto foi desenvolvido com o apoio da Semantix, reforçando a importância da análise de dados aplicada a problemas reais de negócio e a integração entre desempenho operacional e experiência do cliente.

📜 Licença

Este projeto está sob a licença MIT License. Consulte o arquivo LICENSE para mais detalhes.

👤 Autor

João Victor Sacramento
Analista em formação, com foco em Análise de Dados, Engenharia de Dados e Storytelling com Dados.
