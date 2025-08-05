# Projeto Bootcamp Restart 2025
Projeto criado ao final do Bootcamp Restart - Data Girls 2025 para a Trilha Analista de Dados. O projeto será realizado a partir do dataset 'IBM HR Analytics Attrition & Performance' com o objetivo de se realizar uma Análise de Turnover (Rotatividade) de Funcionários.

As fases de leitura inicial dos dados, limpeza e preparação e análise exploratória (EDA) foram realizadas no arquivo colab, utilizando-se tanto a linguagem Python quanto ferramentas de SQL. Esse primeiro contato com o dataset possibilitou alguns insights: distribuição e rotatividade por setor, perfil individual dos colaboradores desligados, condições de trabalho e satisfação desses colaboradores.

A partir desses insights foi possível determinar alguns passos a se seguir na etapa de visualização dos dados. O primeiro deles foi subdividir o dataset atual em 3 partes: 
- Perfil individual: idade, nível educacional, gênero, estado civil etc.
- Perfil do colaborador: departamento, cargo, se viaja ou não, se faz hora extra ou não, anos de experiência, salário etc.
- Variáveis qualitativas: composta por avaliações realizadas com o colaborador concernentes a satisfação geral.

A seguir irei detalhar o tratamento dos dados para visualização em cada subdivisão:

## Perfil individual
- Primeiramente foi criada uma medida que somava o total de funcionários ao contar a quantidade de códigos únicos. A criação dessa medida irá possibilitar a integração de todos os gráficos para uma análise correlacionada.
- Para o gráfico da informação de nivel_educacional_nome foi necessário classificar as categorias de acordo com a hierarquia estabelecida em nivel_educacional, sendo possível visualizar no gráfico de barras a distribuição mais alto nível até o menor deles.
- Em relação a idade, para traduzir essa variável em uma informação de melhor visualização foram criadas colunas que permitissem classificar essas idades em faixas etárias e hierarquizá-las do mais novo para o mais velho.
- Para o acompanhamento de todas as variáveis é possível a segmentação dos dados entre os que foram desligados da empresa e os que não foram.

## Perfil do colaborador

## Variáveis qualitativas

