# Análise de Turnover (Rotatividade) de Funcionários
Os dados estão disponibilizados no link abaixo, em que é possível se obter mais informações acerca do dataset e o teor das informações.
https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data

## Leitura & Exploração Inicial
Neste projeto, vamos analisar o conjunto de dados “IBM HR Analytics Attrition & Performance” para entender os motivos que levam os funcionários a saírem da empresa. O objetivo é descobrir padrões e fatores que influenciam a rotatividade, ajudando a empresa fictícia Data Girls S.A a tomar decisões mais estratégicas na área de Recursos Humanos. Ao final, será criado um dashboard interativo com os principais resultados.
A primeira tecnologia utilizada foi o Python através do Google Colab com o objetivo de fazer a examinação inicial dos dados:

<img width="1583" height="700" alt="image" src="https://github.com/user-attachments/assets/f68d6c9a-112f-4c69-9561-f15c930ee4f2" />

Inicialmente os dados revelam que é uma base de dados de funcionários e ex funcionários, em que são disponibilizadas informações importantes, tais como: idade, com que frequência viajam a trabalho, a distância do trajeto para a empresa, salário, satisfação com o emprego, se o funcionário faz hora extra, satisfação com relacionamento com colegas de trabalho, quantidade de anos desde a última promoção, etc.

## Limpeza & Preparação dos Dados
O primeiro passo na fase de limpeza e preparação dos dados foi averiguar se existem dados não nulos na base, conforme abaixo. Por se tratar de uma base de dados fictícia, todos os dados estão devidamente preenchidos e tipificados.
<img width="474" height="800" alt="image" src="https://github.com/user-attachments/assets/a15d21e1-553f-431a-9726-49e3e5126822" />
Uma análise do conteúdo das colunas, revelou que algumas delas possuíam valores redundantes que não poderia ser objeto de análise relevante, então efetuei a exclusão dessas colunas. Utilizei o argumento inplace para remover esses dados diretamente no df.
<img width="589" height="44" alt="image" src="https://github.com/user-attachments/assets/dcd9f09b-7aef-4db5-bc0c-ac0899690131" />
Em seguida verifiquei se existiam funcionários com dados duplicados:
<img width="674" height="82" alt="image" src="https://github.com/user-attachments/assets/ee2cec51-1041-467a-a594-0c629ad004e2" />

## Análise Exploratória (EDA)

## Visualização Interativa / Dashboard

## Insights e Recomendações
