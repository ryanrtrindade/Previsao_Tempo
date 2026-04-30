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
