# Rede-Neural-Completa

<p align="justify">
💻 Como trabalho proposto no mestrado em Inteligência Computacional, este é um código que implementa, passo a passo, o treinamento e utilização de uma Rede Neural Perceptron Múltiplas camdas utilizando código Python na plataforma "Google Colab". A base dedados utilizada foi disponibilizada para esta disciplina e é referente a um Banco de dados de mamografia e é composto  por 5 variáveis de entrada: Avaliação BI-RADS, idade, forma, margem e densidade. Uma saída (label): classe 0 (normal) ou classe 1 (anormal).
  
O Notebook do Google Colab pode ser acessado neste link: https://colab.research.google.com/drive/1GLDHoyAds4tr2RLbR5kgthgn7EbJfXQd?usp=sharing
</p>

# Metodologia
<p align="justify">
-> Para este trabalho foi exigido dos alunos a implementação do algoritmo de validação cruzada, ou seja, testar a rede em uma abse de dados diferente da usada no treinamento para verificar se o erro de validação cresce enquanto o erro de treinamento continua decrescento, o que foi implementado com sucesso no código.
  
 A base de dados seguiu a divisão mostrada na imagem 1 abaixo:

  * Imagem 1 - Divisão do banco de dados
<p align="center">
  <img src="https://user-images.githubusercontent.com/67600860/174449875-ecfaba55-0b2b-4ee3-ab15-c47151beca12.png" />
</p>

<p align="justify">
-> Par fins de teste, o código tem os seguintes requisitos:
  <ol>
  <li>Edição do número de neurônios na camada escondida</li>
  <li>Edição do número de épocas</li>
  <li>Escolha da função de ativação da camada oculta</li>
  </ol>
</p>

<p align="justify">
-> Para a avaliação de uma rede neural para problemas de classificação de padrões, geralmente se utilizam algumas principais métricas, sendo elas: matriz de confusão, acurácia, precisão, sensibilidade e F_score. 
A matriz de confusão é uma ferramenta gráfica importante pois permite analisar rapidamente o desempenho do sistema, os valores que compõem a matriz advém da comparação entre o conjunto de teste e a predição do sistema, que computa todos os acertos e erros. Ela nos mostra a frequência de cada um dos tipos abaixo:

<ul>
  <li>VP significa verdadeiro positivo, no caso de diagnóstico de câncer de mama indicaria que a amostra foi classificada corretamente com tendo câncer</li>
  <li>VN significa verdadeiro negativo, no caso de diagnóstico de câncer de mama indicaria que a amostra foi classificada corretamente como não tendo câncer</li>
  <li>FP significa falso positivo, no caso de diagnóstico de câncer de mama indicaria que a amostra foi classificada erroneamente como tendo câncer, quando na verdade não o tinha</li>
  <li>FN significa falso negativo, no caso de diagnóstico de câncer de mama indicaria que a amostra foi classificada não tendo câncer, quando na verdade teria</li>
</ul>

A métrica acurácia é definida como: (VP + VN)/(VP + VN + FP + FN)     

> A acurácia é uma das métricas mais utilizadas, já que divide o total de acertos pelo total de valores presentes na base de dados, e diz quanto o modelo acertou das classificações possíveis, então sua interpretação é a mais intuitiva.

A métrica precisão é definida por: VP/(VP + FP)     

> Esta métrica responde a seguinte pergunta: Qual a proporção de identificações positivas foi realmente correta? No caso de diagnóstico de faltas, a métrica indica quantos casos previstos como determinada falha, realmente eram daquela falha.

A métrica sensibilidade (recall) é definida por: VP/(VP + FN)     

> Esta métrica responde a seguinte pergunta: qual proporção de positivos foi identificada corretamente? Ou seja, com ela pode-se saber quão bom o modelo é em prever positivos (a classe que se quer prever), e no caso de diagnóstico de faltas, se uma amostra pertence a determinado tipo de falha.

A métrica F_score é definida por: (2*VP)/(2*VP + FP + FN)        

> Esta métrica representa um balanço entre a precisão e a sensibilidade.

</p>


# Resultados
<p align="justify">
Os resultados apresentados pelo algoritmo são satisfatórios, como podemos ver nos gráficos e imagens a seguir.
</p>

* Imagem  - Evolução do Erro de treinamento

<p align="center">
  <img src="https://user-images.githubusercontent.com/67600860/174449674-3f01abf2-ad55-4faa-8943-fed043ce7470.png" />
</p>

* Imagem  - Evolução do Erro de validação

<p align="center">
  <img src="https://user-images.githubusercontent.com/67600860/174449725-39f0abfa-8dc3-4211-bb97-6ed2a0b4e900.png" />
</p>

* Imagem  - Matriz de Confusão

<p align="justify">
Além da matriz de confusão mostrada abaixo, o modelo obteve as seguintes métricas: 
  <ol>
  <li>Precisão de 0.78</li>
  <li>Sensibilidade de 0.76</li>
  <li>F_score de 0.77</li>
  <li>Acurácia de 0.8</li>
  </ol>
 </p>
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/67600860/174449761-5bea4c75-ca5f-4c41-bd9f-e37c1ae85062.png" />
</p>
