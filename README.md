# Relatório - Capstone
## Introdução do Projeto

  O projeto Capstone, parte da disciplina CCD210 – Fundamentos de Ciência e Visualização de Dados do curso de CDIA na Universidade FEI, tem como objetivo principal aplicar os conceitos de análise de dados, utilizando o framework CRISP-DM (Cross Industry Standard Process for Data Mining) para guiar a estrutura do trabalho. Este processo inclui as fases de compreensão do problema, análise e preparação dos dados, modelagem, avaliação e apresentação dos resultados, permitindo uma abordagem sistemática e eficaz na solução de problemas utilizando-se de dados.
  
  O tema a ser explorado deve ser relacionado com um dos 17 Objetivos de desenvolvimento sustentável da onu, e a questão discutida nesse projeto será o suicídio no Brasil ao longo dos anos, um assunto relevante e que está em alinhamento com a [ODS 3](https://brasil.un.org/pt-br/sdgs/3) (Saúde e Bem-Estar), que busca garantir o acesso à saúde de qualidade e promover o bem-estar para todos, em todas as idades.
    
  Os dados utilizados vêm de uma base pública do [Kaggle](https://www.kaggle.com/), que inclui informações detalhadas como ano, sexo, faixa etária, número de suicídios, entre outros. A análise desse conjunto de dados possibilita uma visão sobre como diferentes fatores influenciam as taxas de suicídio, o que contribui para uma compreensão mais aprofundada da saúde pública. Com isso, espera-se identificar padrões que possam oferecer insights importantes para a formulação de políticas e intervenções mais eficazes.

## Entendimento do Negócio

  O problema central deste projeto é que, apesar das diversas políticas públicas e campanhas de prevenção ao suicídio no Brasil, os números gerais de suicídios entre 1990 e 2015 não apresentaram uma tendência de diminuição significativa. Este cenário deixa claro que as medidas adotadas para combater esse problema podem não ter sido muito eficazes. Isso se torna mais preocupante considerando que o Brasil ocupa atualmente a 8ª posição mundial em termos de índices de suicídio, segundo a Organização Mundial da Saúde ([OMS](https://www.who.int/pt/about)).

  Além do que já foi mencionado, é importante observar que o suicídio não afeta apenas indivíduos, mas tem um impacto significativo na sociedade como um todo. Os efeitos psicológicos nas pessoas próximas aos que cometem suicídio podem fazer com que também considerem a morte como uma forma de aliviar seu sofrimento, o que pode resultar em uma cadeia suicida. A ODS 3 também enfatiza a necessidade de prevenir mortes prematuras causadas por doenças mentais, e o suicídio está diretamente relacionado a essas condições.

  Esse cenário mostra a importância de entender os fatores que contribuem para o crescimento do número de suicídios, como aspectos econômicos, sociais, culturais e de saúde mental. Compreender de forma mais aprofundada as causas de um problema é a chave para encontrar a solução, assim podendo garantir que a prevenção ao suicídio seja tratada de forma mais estratégica e direcionada.

## Compreensão dos Dados

  A base de dados utilizada neste projeto foi retirada do Kaggle, especificamente do conjunto de dados "[Suicide Rates Overview 1985 to 2016](https://www.kaggle.com/datasets/russellyates88/suicide-rates-overview-1985-to-2016)". Este conjunto de dados contém informações sobre as taxas de suicídio em diversos países ao longo de vários anos. No entanto, para este projeto, foi selecionado apenas o subconjunto de dados referente ao Brasil e o período de 1990 a 2015. As colunas presentes no conjunto de dados incluem detalhes como o país, ano, sexo, faixa etária, número de suicídios, população correspondente e a taxa de suicídios por 100 mil habitantes. Esses dados brutos, que inicialmente parecem complexos, podem ser rapidamente explorados e enriquecidos para que possamos ter uma visão mais clara sobre o problema, permitindo a criação de colunas derivadas que ajudam na análise mais detalhada.

  Ao olhar para as informações contidas nas colunas do dataset, podemos calcular o total de suicídios em cada ano, além de segmentá-los por sexo e faixa etária. Essa divisão nos daria uma boa visão geral das diferenças nos índices de suicídio entre homens e mulheres e como essas taxas variam conforme as idades. A classificação por faixa etária, em particular, pode revelar padrões interessantes, como um aumento significativo de suicídios entre determinados grupos etários, o que poderia indicar uma necessidade de soluções mais direcionadas a grupos específicos.

  O agrupamento dos dados por ano, também pode ajudar a identificar tendências ao longo do tempo, como o aumento ou diminuição das taxas de suicídio, e analisar a relação desses números com o aumento populacional ao longo dos anos. A capacidade de gerar essas colunas derivadas não só facilita a visualização de padrões, mas também fornece insights que podem ser essenciais para a formulação de estratégias mais eficazes de prevenção ao suicídio.

  
