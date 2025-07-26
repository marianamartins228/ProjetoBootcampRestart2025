# Análise de Turnover (Rotatividade) de Funcionários

Os dados estão disponibilizados no link abaixo, em que é possível se obter mais informações acerca do dataset e o teor das informações.
https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data

## Leitura & Exploração Inicial

Neste projeto, vamos analisar o conjunto de dados “IBM HR Analytics Attrition & Performance” para entender a rotatividade de colaboradores e seus motivos. O objetivo é descobrir padrões e fatores que influenciam a rotatividade, ajudando a empresa fictícia Data Girls S.A a tomar decisões mais estratégicas na área de Recursos Humanos. Ao final, será criado um dashboard interativo com os principais resultados.
A primeira tecnologia utilizada foi o Python através do Google Colab com o objetivo de fazer a examinação e tratamento inicial dos dados:

<img width="1129" height="519" alt="image" src="https://github.com/user-attachments/assets/c5583cfe-b6c7-439c-a589-a39912dbdf9c" />

<img width="593" height="258" alt="image" src="https://github.com/user-attachments/assets/7ffd03e8-e148-45f4-b581-9f396366b495" />

Inicialmente os dados revelam que é uma base de dados de funcionários e ex funcionários, em que são disponibilizadas informações importantes, tais como: idade, com que frequência viajam a trabalho, a distância do trajeto para a empresa, salário, satisfação com o emprego, se o funcionário faz hora extra, satisfação no relacionamento com colegas de trabalho, quantidade de anos desde a última promoção, etc.
Através da leitura inicial das primeiras linhas da base já é possível perceber que as variáveis categóricas do dataset foram previamente transformadas em valores numéricos, por exemplo, colunas como OverTime, BusinessTravel, MaritalStatus e Gender foram codificadas numericamente. Essa transformação pode facilitar análises quantitativas, mas requer atenção ao interpretar os valores, pois eles não representam uma escala numérica real.
Principais observações que poderão ser relevantes posteriormente:
- A média da idade dos funcionários e ex funcionários é de 36 anos, o que pode revelar se tratar de uma população mais experiente.
- O tempo médio de permanência dos funcionários na empresa é de 7 anos, porém nos próximos passos seria interessante calcular qual a mediana e moda desta coluna. Isso porque podem existir funcionários que permaneceram por muitos anos na empresa, enviesando o resultado médio.
- A descrição e distribuição das variáveis categóricas já nos diz que se trata de uma base em que a maioria dos funcionários ainda trabalham na empresa, são homens casados, viajam raramente e não fazem hora extra. Obviamente, é necessária uma análise bem mais minuciosa para desenhar um perfil, o que será feito posteriormente.

## Limpeza & Preparação dos Dados

O primeiro passo na fase de limpeza e preparação dos dados foi averiguar se existem dados não nulos na base, conforme abaixo. Por se tratar de uma base de dados fictícia, todos os dados estão devidamente preenchidos e tipificados.

<img width="474" height="800" alt="image" src="https://github.com/user-attachments/assets/a15d21e1-553f-431a-9726-49e3e5126822" />

Uma análise do conteúdo das colunas, revelou que algumas delas possuíam valores redundantes que não poderia ser objeto de análise relevante, então efetuei a exclusão dessas colunas. Utilizei o argumento inplace para remover esses dados diretamente no df.

<img width="589" height="44" alt="image" src="https://github.com/user-attachments/assets/dcd9f09b-7aef-4db5-bc0c-ac0899690131" />

Em seguida verifiquei se existiam funcionários com dados duplicados. Como não havia não foi necessária nenhuma ação:

<img width="674" height="82" alt="image" src="https://github.com/user-attachments/assets/ee2cec51-1041-467a-a594-0c629ad004e2" />

Essas observações iniciais nos ajudam a traçar hipóteses para investigação posterior, como a influência de OverTime, JobSatisfaction ou DistanceFromHome sobre a saída de funcionários.

## Análise Exploratória (EDA)

## Visualização Interativa / Dashboard

## Insights e Recomendações
