# Relatório - Capstone
## Introdução do Projeto

  O projeto Capstone, parte da disciplina CCD210 – Fundamentos de Ciência e Visualização de Dados do curso de CDIA na Universidade FEI, tem como objetivo principal aplicar os conceitos de análise de dados, utilizando o framework CRISP-DM (Cross Industry Standard Process for Data Mining) para guiar a estrutura do trabalho. Este processo inclui as fases de compreensão do problema, análise e preparação dos dados, modelagem, avaliação e apresentação dos resultados, permitindo uma abordagem sistemática e eficaz na solução de problemas utilizando-se de dados.
  
  O tema a ser explorado deve ser relacionado com um dos 17 objetivos de desenvolvimento sustentável da ONU, e a questão discutida nesse projeto será o suicídio no Brasil ao longo dos anos, um assunto relevante e que está em alinhamento com a [ODS 3](https://brasil.un.org/pt-br/sdgs/3) (Saúde e Bem-Estar), que busca garantir o acesso à saúde de qualidade e promover o bem-estar para todos, em todas as idades.
    
  Os dados utilizados vêm de uma base pública do [Kaggle](https://www.kaggle.com/), que inclui informações detalhadas como ano, sexo, faixa etária, número de suicídios, entre outros. A análise desse conjunto de dados possibilita uma visão sobre como diferentes fatores influenciam as taxas de suicídio, o que contribui para uma compreensão mais aprofundada da saúde pública. Com isso, espera-se identificar padrões que possam oferecer insights importantes para a formulação de políticas e intervenções mais eficazes.

## Entendimento do Negócio

  O problema central deste projeto é que, apesar das diversas políticas públicas e campanhas de prevenção ao suicídio no Brasil, os números gerais de suicídios entre 1990 e 2015 não apresentaram uma tendência de diminuição significativa. Este cenário deixa claro que as medidas adotadas para combater esse problema podem não ter sido muito eficazes. Isso se torna mais preocupante considerando que o Brasil ocupa atualmente a 8ª posição mundial em termos de índices de suicídio, segundo a Organização Mundial da Saúde ([OMS](https://www.who.int/pt/about)).

  Além do que já foi mencionado, é importante observar que o suicídio não afeta apenas indivíduos, mas tem um impacto significativo na sociedade como um todo. Os efeitos psicológicos nas pessoas próximas aos que cometem suicídio podem fazer com que também considerem a morte como uma forma de aliviar seu sofrimento, o que pode resultar em uma cadeia suicida. A ODS 3 também enfatiza a necessidade de prevenir mortes prematuras causadas por doenças mentais, e o suicídio está diretamente relacionado a essas condições.

  Esse cenário mostra a importância de entender os fatores que contribuem para o crescimento do número de suicídios, como aspectos econômicos, sociais, culturais e de saúde mental. Compreender de forma mais aprofundada as causas de um problema é a chave para encontrar a solução, assim podendo garantir que a prevenção ao suicídio seja tratada de forma mais estratégica e direcionada.

## Compreensão dos Dados

  A base de dados utilizada neste projeto foi retirada do Kaggle, de um dataset chamado "[Suicide Rates Overview 1985 to 2016](https://www.kaggle.com/datasets/russellyates88/suicide-rates-overview-1985-to-2016)". Esse dataset contém informações sobre as taxas de suicídio em diversos países ao longo de vários anos. No entanto, para esse projeto, foi selecionado apenas o subconjunto dos dados referentes ao Brasil e o período de 1990 a 2015. As colunas presentes no dataset incluem informações como o país, ano, sexo, faixa etária, número de suicídios, população correspondente e a taxa de suicídios por 100 mil habitantes. Esses dados brutos, que inicialmente parecem complexos, podem ser rapidamente explorados e enriquecidos para que possamos ter uma visão mais clara sobre o problema, permitindo a criação de colunas derivadas que ajudam na análise mais detalhada.

  Ao olhar para as informações contidas nas colunas do dataset, podemos calcular o total de suicídios em cada ano, além de segmentá-los por sexo e faixa etária. Essa divisão nos daria uma boa visão geral das diferenças nos índices de suicídio entre homens e mulheres e como essas taxas variam conforme as idades. A classificação por faixa etária, em particular, pode revelar padrões interessantes, como um aumento significativo de suicídios entre determinados grupos etários, o que poderia indicar uma necessidade de soluções mais direcionadas a grupos específicos.

  O agrupamento dos dados por ano, também pode ajudar a identificar tendências ao longo do tempo, como o aumento ou diminuição das taxas de suicídio, e analisar a relação desses números com o aumento populacional ao longo dos anos. A capacidade de gerar essas colunas derivadas não só facilita a visualização de padrões, mas também fornece insights que podem ser essenciais para a formulação de estratégias mais eficazes de prevenção ao suicídio.

## Preparação dos Dados

  Na etapa da preparação dos dados, iniciamos abrindo o arquivo no Excel. Primeiramente, filtramos e apagamos mais ou menos 27.500 linhas de dados, mantendo apenas os dados relacionados ao Brasil. Em seguida, excluímos linhas fora do período de 1990 a 2015, mantendo somente os dados registrados dentro dessa faixa de tempo.

  Em seguida, identificamos que uma das colunas tinha uma grande quantidade de dados faltantes, e como a quantidade de dados faltantes era muito alta e não tinha uma maneira adequada de preenchê-los, removemos essa coluna da base de dados. Além disso, também excluímos outras colunas que não seriam úteis para a análise, como a coluna "country-year", que era redundante, pois já temos as colunas "country" e "year" separadas, e considerando que só será feita a análise do Brasil, também podemos eliminar a coluna "country". Dessa forma, simplificamos a base de dados, deixando apenas as informações importantes para a análise.

  Após a limpeza dos dados, foram feitas mudanças na coluna "sexo" para facilitar sua utilização em modelos e análises quantitativas. Utilizamos o método de label encoding, que converte valores categóricos em valores numéricos. Nesse processo, colocamos o valor 0 à categoria "masculino" e o valor 1 à categoria "feminino".

  Com base nos dados originais, criamos uma tabela derivada que mostra uma visão geral dos dados de suicídios no Brasil entre 1990 e 2015 e outra que mostra a quantidade total de suicídios por faixa etária ao longo de todos esses anos.
  
![image](https://github.com/user-attachments/assets/b5e323c1-8bcc-4480-823c-a5bdcfff8e3c) ![image](https://github.com/user-attachments/assets/8d7021f4-3ff0-4da4-adcf-114c82487e2b)

## Modelagem

  Na etapa de modelagem, começamos utilizando das nossas tabelas derivadas para fazer uma regressão linear, representando a tendência de crescimento no número de suicídios entre os anos de 1990 e 2015.
  
![image](https://github.com/user-attachments/assets/2c065c0c-9d5b-4019-a516-3eedfdb69ce5)

  Após a regressão linear, vamos para a construção de gráficos utilizando Python, com base nas mesmas tabelas derivadas. Criamos esses gráficos para complementar a análise visual e facilitar a interpretação dos dados.
  
* GRÁFICO 1

![image](https://github.com/user-attachments/assets/246f48c8-9bd1-48c7-833e-a4123b5c5eef)

* GRÁFICO 2

![image](https://github.com/user-attachments/assets/e074506d-e81e-429b-a205-226cbe079293)

* GRÁFICO 3

![image](https://github.com/user-attachments/assets/933d66f7-7cf4-4925-90fe-2d70d024b528)

## Avaliação

  Analisando os resultados obtidos no processo de modelagem, começando pelo gráfico 1, que apresenta o número total de suicídios por faixa etária no Brasil entre os anos de 1990 e 2015, podemos ver claramente a predominância dos suicídios na faixa etária de 35 a 54 anos, seguida pelas faixas de 25 a 34 anos e 15 a 24 anos. Esse padrão indica que a maior parte dos suicídios está concentrada nas pessoas em idade produtiva, o que pode estar relacionado com estresse no trabalho, instabilidade econômica e problemas de saúde mental, que são mais comuns nessa fase da vida. A análise também sugere que as medidas e campanhas contra suicídio no Brasil podem ser mais eficazes se forem direcionadas especificamente à classe trabalhadora, sendo uma possível forma de alcançar esse público, a promoção de campanhas no ambiente de trabalho.
  
  No gráfico 2 comparamos o número de suicídios por gênero, essa comparação mostrou uma disparidade enorme, com os homens cometendo suicídios em números muito maiores do que as mulheres. Esses dados apontam para uma série de fatores complexos, sendo um deles a dificuldade que os homens têm de expressar suas emoções ou buscar ajuda profissional. Em muitas culturas, ainda é forte a ideia de que "homem não chora" ou que pedir ajuda para um psicólogo, é sinal de fraqueza, mas é certo que com o aumento da conscientização sobre saúde mental essas ideias vão diminuindo gradualmente. Outra possível análise é que o mercado de trabalho, muitas vezes, pode ser um ambiente cruel, e sabendo que a participação dos homens no mercado de trabalho é superior à das mulheres, é um fator a se considerar, embora a diferença tenha diminuído ao longo dos anos.

  No gráfico 3, que representa a taxa de suicídios a cada 100.000 habitantes, é possível observar que a taxa variou ao longo dos anos, seguindo uma tendência geral de subir. Essa tendência de crescimento é semelhante à dos outros gráficos, que também demonstram o comportamento dos suicídios ao longo do tempo, com um aumento constante na maioria dos casos. A análise dessa taxa por 100.000 habitantes ajuda principalmente em comparações, é mais uma forma de visualizar os mesmos dados.

## Conclusão

  Neste projeto aplicamos alguns conceitos de analise de dados utilizando o framework CRISP-DM com o tema "suicídio no Brasil entre 1990 e 2015". Temos como objetivo final deixar claro o valor da análise de dados como uma ferramenta fundamental para entender e abordar questões complexas, como o suicídio, e como ela pode auxiliar na criação de soluções mais assertivas e baseadas em evidências.

  







  
