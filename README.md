# PrevisaoTempo

O objetivo desse projeto é fazer um estudo sobre um dataset de chuvas na Australia.


As etapas desse projeto serão:

1 - Análise exploratória e tratativa de dados

2 - Treino de modelo

3 -  Validação com métricas



TRATANDO VALORES NULOS

1 Etapa:

Visto que o dataset possui várias colunas com valores nulos, será necessário realizar uma tratativ, porém antes é importante verificar a distribuição dos nulos nas colunas. E também será necessário verificar se não há valor nulo concentrado apenas em uma cidade, e além disso, tratar os valores nulos de colunas quantitativas(int,float) e qualitativas(object) separadas.


2 Etapa:

Separar em colunas qualitativas(object) e quantitativas(float ou int), mas antes de preencher os valores nulos das qualitativas, é importante verificar se temos mais de um valor moda e em seguida, preencher os nulos da colunas quantitativas usando mediana(melhor precisão para o tipo de problema e reduzir impacto dos outliers) e das qualitativas utilizando moda.








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



Gráficos

Analisando o gráfico abaixo, pode-se notar que a maioria dos dias não choveram, o motivo é devido a Australia clima seco e pouco favorável para chuvas.

<img width="597" height="432" alt="image" src="https://github.com/user-attachments/assets/ecc5c3f9-e930-4e7d-bd56-7f547878b34f" />


Outro insight é sobre a relação entre umidade e evaporação em dois diferentes horários. 

Durante dias não que chovem, no horária de 9 da manhã, podemos perceber que quanto menor a umidade, a evaporação tende a aumentar.
<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/324b1c84-25a3-4909-825d-1e8be768c83f" />


Já durante dias que chovem e no horário de 9 da manhã, percebe-se que quanto maior a umidade, maior tende ser a evaporação e os registros diminuem.

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/4bf9265a-6d54-4612-ba5f-2026a76e2ae4" />

Agora analisando os mesmo gráficos, só que 3 da tarde.

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/7510a764-9b35-4cbc-8bc2-91cf943df424" />



Podemos chegar a mesma conclusão de que as condições são semelhantes, ou seja, dias que não chvem,  quanto menor a umidade, a evaporação tende a aumentar.

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/369af0e0-1742-4af7-b3e8-fc0b3bfd6412" />

Porém durante dias que chovem as 3 da tarde, os valores estão bem distribuidos, com o valor de evaporação tendo valores altos tanto na humidade baixa, quanto alto.














