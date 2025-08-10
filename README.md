
<img width="1387" height="777" alt="afgsegs" src="https://github.com/user-attachments/assets/543ec4eb-b824-4d8c-a0c4-8d9c12192f58" />

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

<img width="1038" height="417" alt="image" src="https://github.com/user-attachments/assets/95b2d37d-fdd7-41fe-827d-c5632684cc6c" />

- Para o acompanhamento de todas as variáveis é possível a segmentação dos dados entre os que foram desligados da empresa e os que não foram, além da taxa de rotatividade.

Desta forma, a primeira página do dashboard irá trazer as seguintes variáveis:

<img width="1309" height="731" alt="image" src="https://github.com/user-attachments/assets/5662cefa-9d23-4c2b-95be-ab3178b01553" />

Colaboradores que deixaram a empresa:

<img width="1310" height="738" alt="image" src="https://github.com/user-attachments/assets/1fc78e78-0915-44ba-8102-7f9fb74610a5" />

Colaboradores que permanecem na empresa:

<img width="1311" height="740" alt="image" src="https://github.com/user-attachments/assets/f0751bef-a7fa-4a89-b47a-9f95c39033b2" />

Principais resultados e sugestões de planos de ação:
- O principal volume de colaboradores que deixaram a empresa é composto por pessoas com estado civil Solteiro(a), com uma taxa de rotatividade de 25,53%, em contraste com os Casados(as) - 12,48% e os Divorciados(as) - 10,09%.

<img width="440" height="302" alt="image" src="https://github.com/user-attachments/assets/17a163e2-4273-40e4-97f0-d776ce8384c4" />

- Em relação à área de formação, o perfil individual do colaborador que deixou a empresa é relativamente uniforme com a distribuição geral de todos os colaboradores, sem haver uma área que se destaque visualmente em relação às outras. Não obstante é possível perceber uma taxa de rotatividade expressiva em Marketing, Técnico e Recursos Humanos.
- A taxa de rotatividade do sexo masculino é ligeiramente maior do que no sexo feminino.
- A faixa etária da base em geral é formada por colaboradores entre 26 e 45 anos, entretanto, quando se observa apenas os colaboradores que deixaram a empresa há um destaque maior para aqueles entre 18 e 35 anos, sendo que a faixa etária de 18 a 25 anos possui uma taxa de rotatividade de 35,77%.
- Em relação ao nível educacional, os colaboradores que deixaram a empresa estão dividos de forma proporcional em relação a base de dados geral, com destaque para colaboradores com bacharelado ou mestrado.
- De modo geral é possível traçar um perfil de rotatividade formado por indivíduos mais jovens e solteiros. Como plano de ação, o setor de recursos humanos poderia revisar os programas de desenvolvimento de carreira para deixá-los mais claros e com oportunidades de crescimento contínuo, reavaliar benefícios voltados para esse perfil, como flexibilidade de horário, trabalho híbrido e programas de bem-estar (parceria com academias, apoio psicológico, voluntariado corporativo).

## Perfil do colaborador
- Os indicadores que revelam o perfil profissional estão segmentados entre os que deixaram ou não a empresa e taxa de rotatividade.
Colaboradores que deixaram a empresa:

<img width="1312" height="730" alt="image" src="https://github.com/user-attachments/assets/6bd8675e-eb3d-4995-a872-80ebd7395bda" />

Colaboradores que permanecem na empresa:

<img width="1312" height="739" alt="image" src="https://github.com/user-attachments/assets/8aee8ec5-ac82-4f49-b1a4-549614656e7c" />

- Para essas informações foram criadas medidas que revelam uma síntese de indicadores importantes como aumento salarial, distância de casa, quantidade de empresas anteriores, quantidade de treinamentos no último ano e salário mensal médio.

<img width="216" height="295" alt="image" src="https://github.com/user-attachments/assets/7f3b1522-46ee-4922-8caf-27e2586e4328" />


## Variáveis qualitativas

