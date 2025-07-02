# MVP: Análise Exploratória e Pré-processamento de Dados de Qualidade do Ar e Saúde

## 📌 Descrição do Projeto

Este projeto faz parte do desenvolvimento de um MVP (Produto Mínimo Viável) com foco em análise exploratória e pré-processamento de dados, investigando a relação entre **qualidade do ar** e **indicadores de saúde pública**, especialmente internações hospitalares por doenças respiratórias.

O conjunto de dados utilizado — *Air Quality Health Dataset* — foi extraído do Kaggle e contém registros ambientais e hospitalares de diversas cidades ao redor do mundo. As variáveis incluem níveis de poluentes como PM2.5, PM10, CO, NO2, SO2, O3, além de indicadores como densidade populacional e número de internações.

O objetivo principal do projeto é entender padrões ocultos e relações entre os dados, validar hipóteses baseadas em evidências e preparar os dados para futuros modelos de regressão supervisionada capazes de prever hospitalizações com base em fatores ambientais.

---

## 🎯 Objetivos

- Realizar uma **Análise Exploratória de Dados (EDA)** para identificar padrões, outliers e correlações relevantes entre variáveis ambientais e indicadores de saúde.
- Validar hipóteses iniciais relacionadas ao impacto da poluição do ar nas internações hospitalares.
- Executar um **pré-processamento robusto** dos dados, incluindo transformações, codificações, normalização e engenharia de variáveis.
- Preparar o dataset para a **fase de modelagem preditiva** com dados limpos, organizados e otimizados.

---

## 🔍 Hipóteses Investigadas

1. Existe uma correlação positiva forte entre o índice de qualidade do ar (AQI) e o número de internações hospitalares.
2. Poluentes particulados (PM2.5 e PM10) possuem o maior impacto sobre doenças respiratórias.
3. Há variações significativas no impacto da poluição entre diferentes cidades.

---

## 🧪 Metodologia

O trabalho foi conduzido em etapas bem definidas:

- **Exploração Inicial dos Dados**: análise de tipos, valores nulos, estatísticas descritivas e distribuição das variáveis.
- **Visualizações Gráficas**: histogramas, boxplots e matriz de correlação para investigar relações entre os poluentes e as internações.
- **Pré-processamento**: conversão de tipos, codificação de variáveis categóricas, divisão treino/teste e normalizações.
- **Transformações Avançadas**:
  - Criação de variáveis de *lag* para análises temporais.
  - Seleção de variáveis mais relevantes com `SelectKBest`.
  - Redução de dimensionalidade com PCA.
- **Validação das Hipóteses** com base em análises quantitativas e visuais.

---

## 📁 Estrutura dos Dados

O dataset contém **88.489 registros** e as seguintes colunas principais:

- `city`: cidade de origem dos dados  
- `date`: data da observação  
- `aqi`, `pm2_5`, `pm10`, `co`, `no2`, `so2`, `o3`: níveis de poluentes atmosféricos  
- `temperature`, `humidity`, `population_density`: condições ambientais e demográficas  
- `hospital_admissions`: número de internações registradas  

---

## ✅ Principais Conclusões

- A variável `PM2.5` apresentou uma correlação moderada (~0.39) com as internações, enquanto `PM10` teve impacto menor.
- Não houve correlação significativa entre o AQI e as internações, refutando a primeira hipótese.
- As visualizações demonstraram diferenças claras nos níveis de poluição entre as cidades, validando a terceira hipótese.
- O processo de pré-processamento deixou os dados prontos para a aplicação de modelos de regressão.

---

## 📂 Repositório

- **Notebook com análise completa**: `air_quality.ipynb`
- **Base de dados original**: [`air_quality_health_dataset.csv`](https://github.com/LDONoronha/MVP_analise_exploratoria_de_dados/blob/main/air_quality_health_dataset.csv)
- **Scripts auxiliares e imagens**: organizados em subpastas do repositório.

---

## 🚀 Próximos Passos

Com os dados devidamente explorados e preparados, os próximos passos incluem:

- Aplicação de modelos de regressão supervisionada para prever internações.
- Avaliação do desempenho dos modelos utilizando métricas como MAE, RMSE e R².
- Exploração de variáveis temporais e séries temporais para modelagem mais robusta.

---

## 👨‍🎓 Autor

**Lucas de Oliveira Noronha**  
Aluno de Ciência de Dados  
[LinkedIn](www.linkedin.com/in/lucas-noronha-82ba74237) | [Email](noronharm2@gmail.com)

---
