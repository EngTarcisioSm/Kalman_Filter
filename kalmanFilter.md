# Filtro Kalman (Teoria)

## O que é um filtro de Kalman?
- É um processo matemático iterativo que, seguindo um conjunto de iterações (equações), sendo que essas equações recebem entrada de dados consecutivos, calcula-se estimativas  consecultivamente em busca de um valor verdadeiro. 

- O valor real desejado pode ser obtido a partir da média de muitos pontos de entrada, entretanto o filtro de kalman não necessita de várias entradas e rapidamente começa a se aproximar do valor real, ou seja, após cada iteração o valor se aproxima do valor real.

- O filtro de Kalman leva em conta a variação e a incerteza das entradas medidas. O filtro de Kalman torna-se um ótimo filtro quando o sinal lido contêm erros, ruidos e incertezas 

- Ao fazer uma leitura deve-se ter em mente que o valor real não é o lido mais sim ele esta em torno daquele valor lido, ou seja o valor lido possui uma certa incerteza 

- Exemplo 
    ![Grafico_Temperatura](img\001.png)
    - O ciclo de Kalman necessita de uma estimativa inicial (não possuindo valor significativo no resultado final da medição);
    - Em cada estimativa deve-se prever uma certa quantidade de erro/incerteza;
    - Conforme o processo iterativo do filtro ocorre a cada iteração mais proximo se chega-se ao valor real, menor se tornando a imprecisão menor ao ponto de zerar a imprecisão


## Fluxograma

- Existem 3 equações principais no filtro de Kalman 

- Passos:
    - Os passos descritos abaixo são ciclicos, ou seja eles devem ser refeitos a cada nova iteração 
        - Calculo do ganho Comum (Ganho de Kalman)
        - Calculo de Estimativa Atual
        - Calculo do Novo Erro(incerteza) de Estimativa

- Cálculo de Ganho Comun (Ganho de Kalman)
    - Itens necessários para calcular o ganho de Kalman 
        - Erros na estimativa (Erro Anterior)
            - Quando na primeira iteração utilizando o erro original estimado 
            - A cada iteração o Cálculo do Novo Erro (3) é atribuido ao Erro na estimativa
            - Há uma relação entre o erro na estimativa e o erro de dados em que ao analisar aquele com o menor valor terá maior peso sobre o calculo do ganho de kalman

- Estimativa Atual
    - É calculada utilizando 
        - O ganho de Kalman 
        - A Estimativa anterior 
            - Caso seja o primeiro ciclo, utiliza-se a "estimativa original". Em filtros kalman, a "estimativa original" não importa muito pois há uma kconvergencia muito rápida no filtro kalman 
        - O Valor medido (Dados de entrada)
        - Será atribuido um peso tanto a estimativa anterior como ao valor medido (função atribuida ao ganho de kalman). Ambos os valores serão utilizados entretanto com pesos diferentes 
- Calculo de Novo Erro de Estimativa
    - O calculo da nova estimativa de erro é efetuado com os dados 
        - Ganho Comum 
        - Estimativa atual
    - O Calcumo da nova estimativa de erro é utilizado no proximo ciclo 

- A cada no ciclo do filtro a estimativa atual se aproxima mais e mais do valor real

- Diagrama do Filtro de Kalman
    ![Grafico_Temperatura](img\kalman_diagrama.jpg)


## Ganho Comum (Ganho de Kalman)

- O ganho de Kalman é usado para determinar o valor da nova estimativa 
- Calculo do Ganho comum é um calculo entre estimativa de erro  e erro na medição.<br> 
![diagrama 002](img\diagrama002.png)

- Fórmula:<br>
![formulario 001](img\formula001.png)

## Estimativa Atual
- Diagrama da estimativa atual.<br>
![diagrama 003](img\diagrama003.png)

- Fórmula:<br>
![formulario 002](img\formula002.png)


## Onde eu parei 
- https://www.youtube.com/watch?v=fpRb1sjFz_M&list=PLX2gX-ftPVXU3oUFNATxGXY90AULiqnWT&index=3
- Tempo: 01:40