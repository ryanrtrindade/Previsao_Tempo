# PrevisaoTempo

O objetivo desse projeto é criar um algoritmo capaz de atuar na previsão de chuvas


As etapas desse projeto serão:

1 - Análise exploratória e tratativa de dados

2 - Treino de modelo

3 -  Validação com métricas



TRATANDO VALORES NULOS

1 Etapa:

Visto que o dataset possui várias colunas com valores nulos, será necessário realizar uma tratativ, porém antes é importante verificar a distribuição dos nulos nas colunas. E também será necessário verificar se não há valor nulo concentrado apenas em uma cidade, e além disso, tratar os valores nulos de colunas quantitativas(int,float) e qualitativas(object) separadas.


2 Etapa:

Separar em colunas qualitativas(object) e quantitativas(float ou int), mas antes de preencher os valores nulos das qualitativas, é importante verificar se temos mais de um valor moda e em seguida, preencher os nulos da colunas quantitativas usando mediana(melhor precisão para o tipo de problema e reduzir impacto dos outliers) e das qualitativas utilizando moda.

Outro pequeno detalhe será remover a coluna RainTomorrow, pois o foco é a coluna RainToday para essa análise.








ANALISANDO OUTLIERS

É de suma importância fazer uma análise dos outliers no projeto e verificar se não há algum valor extremamente elevado ou abaixo do normal, e se houve, também investigar se não houve algum tipo de erro de digitação ou se as condições climática fugiram do padrão.


A principio não será necessário remover estes outliers de cara nesse projeto pois irei criar o modelo utilizando random forest, porém eu irei explorar os outliers de cada coluna e verificar em quantos porcentos do total de linhas eles correspondem para validar minha decisão.


As seguintes porcentagens de outliers em cada coluna:

Rainfall = 19,89%

Evaporation = 25,76%

WindGustSpeed = 3,79%

Humidity9am = 0,97%

Humidity3pm = 0%

Pressure9am = 1,89%

Pressure3pm = 1,73%

Cloud9am = 0% 

Cloud3pm = 3,41%

Temp9am = 0,21%

Temp3pm = 0, 67%







CONSTRUÇÃO DE GRÁFICOS

A construção dos gráficos terá 2 objetivos:

1) Gerar insights sobre o gráfico

2) Fazer comparativo com os valores do modelo de previsão(Esse é o principal motivo)





