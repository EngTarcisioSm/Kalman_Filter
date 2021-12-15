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


https://www.youtube.com/watch?v=tk3OJjKTDnQ&list=PLX2gX-ftPVXU3oUFNATxGXY90AULiqnWT&index=2

PAREI EM 02:15