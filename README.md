<img width="1387" height="777" alt="afgsegs" src="https://github.com/user-attachments/assets/543ec4eb-b824-4d8c-a0c4-8d9c12192f58" />

# Projeto Bootcamp Restart 2025
Projeto criado ao final do Bootcamp Restart - Data Girls 2025 para a Trilha Analista de Dados. O projeto será realizado a partir do dataset 'IBM HR Analytics Attrition & Performance' com o objetivo de se realizar uma Análise de Turnover (Rotatividade) de Funcionários.

As fases de leitura inicial dos dados, limpeza e preparação e análise exploratória (EDA) foram realizadas no arquivo colab, utilizando-se tanto a linguagem Python quanto ferramentas de SQL. Esse primeiro contato com o dataset possibilitou alguns insights: distribuição e rotatividade por setor, perfil individual dos colaboradores desligados, condições de trabalho e satisfação desses colaboradores.

A partir desses insights foi possível determinar alguns passos a se seguir na etapa de visualização dos dados. O primeiro deles foi subdividir o dataset atual em 3 partes: 
- Perfil individual: idade, nível educacional, gênero, estado civil etc.
- Perfil do colaborador: departamento, cargo, se viaja ou não, se faz hora extra ou não, anos de experiência, salário etc.
- Variáveis qualitativas: composta por avaliações realizadas com o colaborador concernentes a satisfação geral.

A seguir irei detalhar o tratamento dos dados para visualização em cada subdivisão. Essa subdivisão também irá contemplar uma análise e sugestões de planos de ações.

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

<img width="1312" height="736" alt="image" src="https://github.com/user-attachments/assets/032aa4f0-19a0-4678-9616-1bd5436bf351" />

Colaboradores que permanecem na empresa:

<img width="1311" height="739" alt="image" src="https://github.com/user-attachments/assets/419f9f33-8d7f-4e47-ac11-f17b3fb8b9f9" />

- Para essas informações foram criadas medidas que revelam uma síntese de indicadores importantes como aumento salarial, distância de casa, quantidade de empresas anteriores, quantidade de treinamentos no último ano, salário mensal médio e anos de empresa. Na comparação entre os que deixaram ou não a empresa destaca-se: (1) aqueles que deixaram a empresa tem uma distância média de 2 milhas maior a percorrer do que os colaboradores que permanecem, (2) os colaboradores que saíram ganhavam em média 2 mil a menos, (3) os colaboradores que permanecem possuem em média dois anos a mais de empresa.
- Com base nesses números recomenda-se novamente examinar o plano de cargos e salários para validar se não há uma defasagem de salários em relação aos valores praticados pelo mercado, além de analisar se existem programas de ajuda de custo para transporte e se eles são compatíveis com a realidade da empresa. Em relação ao tempo de empresa, o setor de recursos humanos poderia avaliar a criação de programação de retenção de talentos com benefícios ou bônus específicos para quem atinge marcos de permanência.
- Distribuição por cargos e departamento: observa-se que a taxa de rotatividade é substancialmente menor em cargos de gestão e diretoria, concentrando-se em cargos de atividade operacionais, com destaque para o setor de vendas e recursos humanos.
- A análise da área de vendas revela uma disparidade significativa entre os cargos de representante e executivo, tanto em termos de rotatividade quanto de remuneração e tempo de empresa. Enquanto os representantes apresentam uma taxa de rotatividade de 39,76%, os executivos registram apenas 17,4%. Além disso, há um gap salarial expressivo de 4,2 mil a favor dos executivos, que também possuem, em média, quatro anos a mais de permanência na organização. Esses dados indicam a necessidade de ações estratégicas como a implementação de planos de carreira estruturados e personalizados para essa área, programas de mentoria e capacitação, políticas salariais mais competitivas e modelo de comissionamento mais compatível com a função.
- Outro destaque se faz necessário para cargos na área de recursos humanos em si, onde existe uma rotatividade de 23,08%. A rotatividade no RH pode estar ligada à sobrecarga de trabalho, pressão por resultados e poucas oportunidades de crescimento. Para avaliar e reduzir esse índice, recomenda-se buscar um equilíbrio das demandas, investir em desenvolvimento e reconhecimento dos profissionais e revisar o plano de carreira específico da área.
- No setor de Pesquisa e Desenvolvimento, que concentra mais da metade do total de colaboradores, destaca-se o cargo de Técnico de Laboratório, cuja rotatividade é 7,84% maior do que a do cargo de Cientista Pesquisador, apesar de ambos apresentarem indicadores compatíveis. Esse dado sugere que fatores além de salário, tempo de empresa e treinamento podem estar influenciando essa diferença.
Cientista Pesquisador:
<img width="212" height="310" alt="image" src="https://github.com/user-attachments/assets/5e7cb029-f83e-4102-abed-f1a2973b06c2" />
Técnico de Laboratório:
<img width="209" height="307" alt="image" src="https://github.com/user-attachments/assets/55a5b7ed-f901-4d38-872a-8428284628b5" />
- Viagem a trabalho: é possível perceber uma relação entre rotatividade e viagens a trabalho. Isso porque quem viaja raramente possui 14,96% de rotatividade, quem viaja com frequência tem 24,91% e quem não viaja possui apenas 8% de rotatividade. Entre as ações recomendadas cita-se avaliar e implementar melhorias nas condições de trabalho durante as viagens, como suporte logístico e tempo de descanso adequado. Também seria recomendável promover benefícios específicos para colaboradores que viajam, como incentivos, reconhecimentos ou compensações extras.
- Hora extra: este indicador revela um ponto crítico de atenção. Na base geral, 70% dos colaboradores não precisam realizar horas extras. No entanto, entre os que precisam, observa-se uma taxa de rotatividade alarmante de 30,53%, significativamente superior à taxa de 10,44% entre os que não fazem hora extra. Para mitigar esse impacto, é essencial revisar a distribuição de carga horária, implementar políticas de compensação mais justas e promover ações de escuta ativa com os times mais sobrecarregados.

## Variáveis qualitativas
- Para as variáveis qualitativas não se faz necessária a criação de medidas, apenas a hierarquização das categorias.

<img width="1314" height="737" alt="image" src="https://github.com/user-attachments/assets/c1149b6b-f39f-4a33-bd83-c444a7151cdf" />

- Como era esperado, a rotatividade é mais elevada entre colaboradores que demonstram baixa satisfação com o trabalho, pouco envolvimento e dificuldades em manter o equilíbrio entre vida pessoal e profissional. Após a implementação das medidas já mencionadas, é fundamental que o setor de Recursos Humanos reavalie esses indicadores periodicamente para monitorar sinais de melhoria e ajustar estratégias conforme necessário. Além disso, recomenda-se que esse tipo de análise seja desvinculado do código individual do colaborador — como ocorre nesta base de dados — para garantir a confidencialidade. A coleta de dados deve ser feita com foco no setor ou cargo, promovendo um ambiente de confiança e incentivando respostas mais sinceras. Para reforçar essa segurança, pode-se adotar pesquisas anônimas e comunicar claramente aos colaboradores que suas opiniões serão tratadas com sigilo e respeito.







