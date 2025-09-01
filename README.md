<img width="1435" height="801" alt="image" src="https://github.com/user-attachments/assets/f6cc99a3-966f-465a-94be-75e70b0e660b" />


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
- Para o gráfico da informação de nivel_educacional_nome foi necessário classificar as categorias de acordo com a hierarquia estabelecida em nivel_educacional, sendo possível visualizar no gráfico de barras a distribuição do mais alto nível até o menor deles.
- Em relação a idade, para traduzir essa variável em uma informação de melhor visualização foram criadas colunas que permitissem classificar essas idades em faixas etárias e hierarquizá-las do mais novo para o mais velho.

<img width="1038" height="417" alt="image" src="https://github.com/user-attachments/assets/95b2d37d-fdd7-41fe-827d-c5632684cc6c" />

- Para o acompanhamento de todas as variáveis é possível a segmentação dos dados entre os que foram desligados da empresa e os que não foram, além da taxa de rotatividade.

Desta forma, a primeira página do dashboard irá trazer as seguintes análises:

<img width="1542" height="867" alt="image" src="https://github.com/user-attachments/assets/4d71e2d2-7986-44e5-9030-33be06c560a0" />

Colaboradores que deixaram a empresa:

<img width="1541" height="866" alt="image" src="https://github.com/user-attachments/assets/7cdfae13-6bd1-44b1-83eb-bb39a8701324" />

Colaboradores que permanecem na empresa:

<img width="1543" height="871" alt="image" src="https://github.com/user-attachments/assets/03edfed6-e944-4df8-adb1-1363ca8219b1" />

- O principal volume de colaboradores que deixaram a empresa é composto por pessoas com **estado civil Solteiro(a), com uma taxa de rotatividade de 25,53%, em contraste com os Casados(as) - 12,48% e os Divorciados(as) - 10,09%**.

<img width="518" height="351" alt="image" src="https://github.com/user-attachments/assets/cc9cfb9d-6ce5-41de-9e4e-84fe5a7aaed1" />

- Em relação à área de formação, o perfil individual do colaborador que deixou a empresa é relativamente uniforme com a distribuição geral de todos os colaboradores, sem haver uma área que se destaque visualmente em relação às outras. Não obstante é possível perceber uma **taxa de rotatividade expressiva em Marketing, Técnico e Recursos Humanos**.
- A taxa de **rotatividade do sexo masculino é ligeiramente maior do que no sexo feminino**.
- A faixa etária da base em geral é formada por colaboradores entre 26 e 45 anos, entretanto, quando se observa apenas os colaboradores que deixaram a empresa há um destaque maior para aqueles entre **18 e 35 anos, sendo que a faixa etária de 18 a 25 anos possui uma taxa de rotatividade de 35,77%**.
- Em relação ao nível educacional, os colaboradores que deixaram a empresa estão dividos de forma proporcional em relação a base de dados geral, com destaque para colaboradores com bacharelado ou mestrado.
- De modo geral é possível traçar um perfil de rotatividade formado por **indivíduos mais jovens e solteiros**. Como plano de ação, o setor de recursos humanos poderia **revisar os programas de desenvolvimento de carreira para deixá-los mais claros e com oportunidades de crescimento contínuo, reavaliar benefícios voltados para esse perfil, como flexibilidade de horário, trabalho híbrido e programas de bem-estar (parceria com academias, apoio psicológico, voluntariado corporativo etc).**

## Perfil do colaborador
- Os indicadores que revelam o perfil profissional também estão segmentados entre os que deixaram ou não a empresa e taxa de rotatividade.

Colaboradores que deixaram a empresa:

<img width="1542" height="868" alt="image" src="https://github.com/user-attachments/assets/caf442ed-7e73-4c35-b95a-d3533d03b323" />

Colaboradores que permanecem na empresa:

<img width="1543" height="866" alt="image" src="https://github.com/user-attachments/assets/1ab8766b-3ead-42d1-8e43-ad4c3f3c1553" />

- Para essas informações foram criadas medidas que revelam uma síntese de indicadores importantes como **aumento salarial, distância de casa, quantidade de empresas anteriores, quantidade de treinamentos no último ano, salário mensal médio e anos de empresa**. Na comparação entre os que deixaram ou não a empresa destaca-se: **(1) aqueles que deixaram a empresa tem uma distância média de 2 milhas maior a percorrer do que os colaboradores que permanecem, (2) os colaboradores que saíram ganhavam em média 2 mil a menos, (3) os colaboradores que permanecem possuem em média dois anos a mais de empresa.**
- Com base nesses números recomenda-se novamente examinar o plano de cargos e salários para **validar se não há uma defasagem de salários em relação aos valores praticados pelo mercado, além de analisar se existem programas de ajuda de custo para transporte e se eles são compatíveis com a realidade da empresa**. Em relação ao tempo de empresa, o setor de recursos humanos poderia **avaliar a criação de programação de retenção de talentos com benefícios ou bônus específicos para quem atinge marcos de permanência**.
- Distribuição por cargos e departamento: observa-se que a **taxa de rotatividade é substancialmente menor em cargos de gestão e diretoria, concentrando-se em cargos de atividade operacionais, com destaque para o setor de vendas e recursos humanos**.
- A análise da área de vendas revela uma **disparidade significativa entre os cargos de representante e executivo**, tanto em termos de rotatividade quanto de remuneração e tempo de empresa. Enquanto os **representantes apresentam uma taxa de rotatividade de 39,76%, os executivos registram apenas 17,4%**. Além disso, há um **gap salarial expressivo de 4,2 mil a favor dos executivos, que também possuem, em média, quatro anos a mais de permanência na organização**. Esses dados indicam a necessidade de ações estratégicas como a implementação de planos de carreira estruturados e personalizados para essa área, **programas de mentoria e capacitação, políticas salariais mais competitivas e modelo de comissionamento mais compatível com a função.**
- Outro destaque se faz necessário para cargos na área de **recursos humanos em si**, onde existe uma **rotatividade de 23,08%**. A rotatividade no RH pode estar ligada à **sobrecarga de trabalho, pressão por resultados e poucas oportunidades de crescimento.** Para avaliar e reduzir esse índice, recomenda-se buscar um **equilíbrio das demandas, investir em desenvolvimento e reconhecimento dos profissionais e revisar o plano de carreira específico da área.**
- No setor de Pesquisa e Desenvolvimento, que concentra mais da metade do total de colaboradores, destaca-se o cargo de **Técnico de Laboratório, cuja rotatividade é 7,84% maior do que a do cargo de Cientista Pesquisador, apesar de ambos apresentarem indicadores compatíveis.** Esse dado sugere que fatores além de salário, tempo de empresa e treinamento podem estar influenciando essa diferença.
- 
Cientista Pesquisador:

<img width="252" height="361" alt="image" src="https://github.com/user-attachments/assets/d21c3f3d-801d-4c17-aa4a-65e8cc4e5761" />

Técnico de Laboratório:

<img width="252" height="353" alt="image" src="https://github.com/user-attachments/assets/6820d9aa-253f-4af8-9e94-36e0366b2585" />

- Viagem a trabalho: é possível perceber uma relação entre rotatividade e viagens a trabalho. Isso porque quem **viaja raramente possui 14,96% de rotatividade, quem viaja com frequência tem 24,91% e quem não viaja possui apenas 8% de rotatividade**. Entre as ações recomendadas cita-se avaliar e **implementar melhorias nas condições de trabalho durante as viagens, como suporte logístico e tempo de descanso adequado.** Também seria recomendável promover **benefícios específicos para colaboradores que viajam, como incentivos, reconhecimentos ou compensações extras.**
- Hora extra: este indicador revela um ponto crítico de atenção. Na base geral, 70% dos colaboradores não precisam realizar horas extras. No entanto, entre os que precisam, observa-se uma **taxa de rotatividade alarmante de 30,53%, significativamente superior à taxa de 10,44% entre os que não fazem hora extra**. Para mitigar esse impacto, é essencial **revisar a distribuição de carga horária, implementar políticas de compensação mais justas e promover ações de escuta ativa com os times mais sobrecarregados.**

## Variáveis qualitativas
- Para as variáveis qualitativas não se faz necessária a criação de medidas, apenas a hierarquização das categorias.

<img width="1542" height="870" alt="image" src="https://github.com/user-attachments/assets/77d707cd-f932-4839-be17-d1eb457ddf0f" />

- Como era esperado, a rotatividade é mais elevada entre colaboradores que demonstram baixa satisfação com o trabalho, pouco envolvimento e dificuldades em manter o equilíbrio entre vida pessoal e profissional. Após a implementação das medidas já mencionadas, é fundamental que o setor de Recursos Humanos reavalie esses indicadores periodicamente para monitorar sinais de melhoria e ajustar estratégias conforme necessário. Além disso, **recomenda-se que esse tipo de análise seja desvinculado do código individual do colaborador** — como ocorre nesta base de dados — para garantir a confidencialidade. A coleta de dados deve ser feita com foco no setor ou cargo, **promovendo um ambiente de confiança e incentivando respostas mais sinceras**. Para reforçar essa segurança, pode-se adotar pesquisas anônimas e comunicar claramente aos colaboradores que suas opiniões serão tratadas com sigilo e respeito.


## Síntese dos principais resultados, ações e considerações
### Perfil Individual

- Faixa etária com maior rotatividade: 18 a 25 anos (35,77%) e 26 a 35 anos.
- Estado civil: Solteiros têm maior rotatividade (25,53%) comparado a casados (12,48%) e divorciados (10,09%).
- Gênero: Homens apresentam ligeiramente mais rotatividade.
- Nível educacional: Rotatividade proporcional, com destaque para bacharelado e mestrado.
- Área de formação: Marketing, Técnico e RH têm taxas mais altas.

Medidas recomendadas: 
- Reavaliar benefícios voltados para jovens e solteiros (flexibilidade, bem-estar, trabalho híbrido).
- Criar programas de desenvolvimento de carreira com trilhas claras de crescimento.

### Perfil do Colaborador

- Cargos operacionais (representantes, técnicos) têm maior rotatividade que cargos de gestão.
- Setores mais críticos: Vendas e Recursos Humanos.
- Distância da casa: Colaboradores que saem percorrem, em média, 2 milhas a mais.
- Salário: Colaboradores desligados ganham cerca de 2.000 a menos.
- Tempo de empresa: Permanentes têm, em média, dois anos a mais.
- Viagens a trabalho: Quem viaja com frequência tem rotatividade de 24,91%, contra 8% de quem não viaja.
- Hora extra: 30,53% de rotatividade entre quem faz hora extra, contra 10,44% entre quem não faz.

Medidas recomendadas: 

- Revisar plano de cargos e salários, especialmente em áreas operacionais.
- Implementar ajuda de custo para transporte.
- Criar programas de retenção com bônus por tempo de casa.
- Estruturar planos de carreira e mentoria para representantes de vendas.
- Reequilibrar demandas e investir em reconhecimento no setor de RH.

### Variáveis Qualitativas
- Baixa satisfação, envolvimento e equilíbrio estão diretamente ligados à rotatividade.
- Avaliações qualitativas indicam que colaboradores com notas baixas em satisfação geral, ambiente e relacionamentos tendem a sair mais.

Medidas recomendadas: 
- Realizar pesquisas anônimas para garantir sinceridade nas respostas.
- Monitorar periodicamente os indicadores de satisfação e ajustar ações conforme os resultados.
- Desvincular análises do código do colaborador para preservar anonimato.

Ponto sugerido para melhoria da análise:
- Falta de segmentação temporal: Não há análise por tempo (ano/mês), o que dificulta identificar tendências.

## Automação com Power Automate

Este projeto inclui uma automação criada com Power Automate que envia alertas por e-mail quando a taxa de rotatividade ultrapassa 20%.

### O que a automação faz:
- Executa diariamente
- Consulta o dataset do Power BI
- Verifica se a taxa de rotatividade ultrapassa 20%
- Envia um e-mail de alerta e link para o dashboard

### Fluxo utilizado:
- Gatilho: Recorrência diária
- Ação: Executar consulta DAX no Power BI
- Condição: Verifica se taxa de rotatividade > 20%
- Resultado: Envio de e-mail automático

### Arquivo e informações do fluxo:

[automacao_tx_rotatividade_20250810181552.zip](https://github.com/user-attachments/files/21706820/automacao_tx_rotatividade_20250810181552.zip)

<img width="1108" height="439" alt="image" src="https://github.com/user-attachments/assets/d16699bb-8c48-4318-b335-ece8953c68ec" />

<img width="1111" height="711" alt="image" src="https://github.com/user-attachments/assets/6cb529f7-1626-4e58-8672-eb445118f908" />

<img width="1385" height="827" alt="image" src="https://github.com/user-attachments/assets/d8f195a0-a14d-48a6-a985-11f11316c0f9" />


## Encerramento

Este projeto foi desenvolvido com o objetivo de aplicar conhecimentos práticos em análise de dados e visualização com Power BI. A solução proposta oferece uma abordagem eficiente para monitorar a taxa de rotatividade nas empresas, permitindo decisões mais ágeis e estratégicas. Estou aberta a críticas construtivas e sugestões que possam aprimorar ainda mais este estudo — toda contribuição é bem-vinda! Muito obrigada!




