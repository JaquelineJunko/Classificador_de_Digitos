# Classificador_de_Digitos-

A base de imagens MNIST é composta por número de 0 a 9 escritos a mão (<http://yann.lecun.com/exdb/mnist/>). Dessa base podemos elaborar um classificador que seja capaz de analisar e classificar quais são os dígitos representados em cada uma delas. Nesse projeto foi elaborado uma rede neural - multilayer perceptron para distinguir os números 0 e 5 dessa base de imagens.

Quais fatores levaram a escolha desse classificador? Basicamente, os MLP são algoritmos mais robustos, capazes de solucionar uma gama de problemas de classificação. Um dos mais conhecidos sendo a separação das flores setosa, versicolor e virginica da base de imagens IRIS, baseado nas propriedades das flores. Além disso, redes neurais mais complexas, como as Redes Neurais Convolucionais (CNN), foram projetadas especificamente para a análise de dados multidimensionais, como as imagens. A parte de classificação de uma CNN é um MLP, o que nos levou também a escolha. No entanto, como o MLP trabalha com dados na forma unidimensional, foi necessário redimensionar os pixels das imagens para esse estrutura.

O MLP é composto por uma camada de entrada de dimensões (1x784), uma vez que as imagens possuem dimensão de 28 x 28; uma camada oculta com 56 neurônios; e uma camada de saída com a função Softmax. 

Inicialmente, a rede é treinada com 20 épocas para averiguar qual seria a quantidade ideal para treinar o classificador, chegando a conclusão de que **9 épocas** seria o suficiente. Na primeira época, o classificador já obtinha uma acurácia maior que 96%, chegando a valores superiores a 99%. Quanto treinada a rede com 9 épocas, foram obtidas acurácias para treino e teste de **98,94% e 99,15%**, repectivamente. Para o treino da rede foi utilizado o DataLoader, que particionou nosso conjunto de imagens em diferentes batches. Essa foi uma das estratégias para evitar um possivel *overfitting*.

Comparamos o nosso classificador com um outro de baseline, o Dummy Classifier. Esse classificador não possui muita complexidade, e queríamos concluir se ele seria capaz ou não de obter taxas de acurácias tão altas quanto a do nosso modelo. Como resultado, obteve-se uma acurácia de **48,77%**, reafirmando o desempenho de nosso modelo.

Mais ainda, e se comparassemos o MLP com outro classificador também muito utilizado em problemas de classificação e que possui um menor nível de complexidade em relação ao modelo proposto, mas superior ao classificador Dummy? Para isso, foi utilizado o classificador **SVM com o kernel RBF**. Esse classificador foi importado da biblioteca Sklearn e possui custo computacional menor comparado ao MLP. 

O que se conclui foi que o *SVM obtinha resultados infimamente superior ao MLP*, o que nos levou a duas conclusões finais.

Mais detalhes e análise dos resultados podem ser obtidos nos detalhes do projeto. **Não deixe de ler as considerações finais também!**
