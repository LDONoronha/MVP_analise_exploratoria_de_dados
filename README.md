# MVP: Análise Exploratória e Pré-processamento de Dados de Qualidade do Ar e Saúde

## Aluno
Lucas de Oliveira Noronha

## Dataset
Air Quality Health Dataset (Disponível no Kaggle)

## Link para os Dados
[air_quality_health_dataset.csv](https://github.com/LDONoronha/MVP_analise_exploratoria_de_dados/blob/main/air_quality_health_dataset.csv)

## Definição do Problema
Este projeto investiga a relação entre a poluição do ar e a saúde pública, focando em como níveis de poluentes específicos impactam internações hospitalares por doenças respiratórias em diferentes cidades.

## Hipóteses
1.  Correlação positiva forte entre AQI e métricas de saúde.
2.  Material particulado (PM2.5 e PM10) terá o impacto mais significativo em internações respiratórias.
3.  Diferença notável no impacto da poluição entre as cidades.

## Tipo de Problema
Problema de Regressão Supervisionada.

## Análise Exploratória de Dados (EDA)
A análise exploratória revelou:
*   O dataset possui 88489 instâncias sem valores nulos.
*   As colunas `city`, `date` e `population_density` são categóricas (`date` foi convertida para datetime).
*   Estatísticas descritivas mostraram a distribuição das variáveis numéricas.
*   Histogramas visualizam a distribuição de `aqi`, `pm2_5`, `pm10`, e `hospital_admissions`.
*   Um gráfico de contagem por cidade evidenciou um desbalanceamento na quantidade de registros por cidade.
*   Boxplots por cidade demonstraram a variabilidade dos poluentes entre as cidades.
*   A matriz de correlação mostrou uma correlação positiva moderada entre PM2.5 e hospital_admissions (~0.39), enquanto outras correlações foram fracas.

## Pré-processamento de Dados
As seguintes etapas de pré-processamento foram realizadas:
*   Conversão da coluna `date` para o tipo datetime.
*   Aplicação de One-Hot Encoding na coluna `city`.
*   Remoção da coluna `date` e `population_density` para a modelagem.
*   Separação dos dados em conjuntos de treino (80%) e teste (20%).
*   Realização de Normalização (Min-Max Scaling) e Padronização (Standardization) nos dados numéricos, separadamente para treino e teste.

## Outras Transformações e Etapas Exploradas
*   **Engenharia de Características:** Demonstração da criação de uma Lag Feature para `pm2_5`.
*   **Seleção de Características:** Utilização de `SelectKBest` para identificar as 5 features mais relevantes (`pm2_5`, `o3`, `temperature`, `city_Beijing`, `city_Mexico City`).
*   **Redução de Dimensionalidade:** Aplicação de PCA nas features de poluentes, onde 2 componentes explicaram aproximadamente 40.25% da variância.

## Conclusão e Validação das Hipóteses
*   **Hipótese 1:** Não validada pela análise de correlação linear (correlação AQI e internações próxima de zero).
*   **Hipótese 2:** Parcialmente validada. PM2.5 mostrou uma correlação positiva moderada com internações, enquanto PM10 não.
*   **Hipótese 3:** Validada pelas visualizações, que mostram diferenças significativas nos níveis de poluição entre as cidades.

Este notebook conclui as etapas de análise exploratória e pré-processamento, deixando os dados preparados para a fase de modelagem preditiva.
