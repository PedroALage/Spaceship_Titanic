# Spaceship Titanic
Repositório criado para **[competição do Kaggle sobre Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic)**

O histórico dos resultados obtidos é mostrado abaixo e pode ser encontrado no Kaggle:
<img src="https://github.com/PedroALage/Spaceship_Titanic/blob/main/pkgImages/grafEvolucao.png"/>

## [Etapa 0: Tantando base](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte0_TratandoDados.ipynb)
- Na etapa 0 **foi realizada apenas um tratamento simples** na base.
  - Foi visualizado um resumo da base utilizando o ydata-profiling, biblioteca capaz de gerar com poucas linhas toda a descrição do nosso dataset.
  - Foi removida as colunas com **elevada cardinalidade** e as **colunas de texto**.
  - Os **valores vazios** foram tratados utilizando a relação identificada entre as colunas, onde não se encontrou relação, foi utilizado a média e a moda das variáveis.

## [Etapa 1: Análise inicial](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte1_AnaliseSimples.ipynb)
- Na etapa 1 **foi aplicado os modelos de classificação**.
  - Foram utilizados 3 algoritmos: **Árvore de Classificação**, **KNN** e **Regressão Logística** e foi avaliado esses modelos utilizando a **acurácia** e a **matriz de confusão**.
  - O score retornado pelo Kaggle foi: **78,20 %**

## [Etapa 2: Tratando textos](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte2_TratandoColunas.ipynb)
- Na etapa 2 o foco principal foi tratar as colunas de texto para utilizar todas as variáveis no modelo.
  - Foi utilizado o **OneHotEncoder** para tratar as colunas de texto.
  - As colunas lógicas também foram tratadas nessa etapa, de modo a tornar os dados mais homogêneos.
  - Foi utilizado os mesmos modelos anteriores.
  - O score retornado pelo Kaggle foi: 78,95 %
 
## [Etapa 3: Tratando os dados](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte3_EngRecursos.ipynb)
- Na etapa 3 o objetivo foi de entender melhor os dados para encontrar uma forma mais eficaz de tratar os dados e tentar melhorar o resultado obtido anteriormente.
  - Foi realizado o **ajuste na escala** dos dados para as colunas RoomService, FoodCourt, ShoppingMall, Spa, VRDeck.
  - As colunas foram analisadas de modo a encontrar alguma relação que ajudasse na previsão, a análise resultou em uma nova coluna apontando passageiros jovens em sono criogênico.
  - Foi analisado a **correlação entre todas as variáveis** para selecionar aquelas que mais faziam sentido com o modelo.
  - A remoção de colunas ocasionou em perde de acurácia, então não foi utilizada.
  - A inserção da nova coluna não apresentou ganhos ao modelo.
  - Foi utilizado os mesmos modelos anteriores.
  - O score retornado pelo Kaggle foi: 78,95 %
 
## [Etapa 4: Selecionando novos algoritmos](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte4_NovosModelos.ipynb)
- Na etapa 4 o objetivo foi de manter os dados e **utilizar novos algoritmos de previsão** e comparar os resultados.
  - Foram utilizados os algoritmos: **Regressão Logística** (mantido pois obteve melhor resultado nas etapas anteriores), **RandomForest** e **MLPClassifier (Redes Neurais)**.
  - O score retornado pelo Kaggle foi: 79,33 %

## [Etapa 5: Recuperando informações](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte5_RevisandoBase.ipynb)
- Na etapa 5 o objetivo foi de **recuperar a informação relacionada ao lado da cabine** e verificar como afetaria o modelo.
  - O PassengerId permitia encontrar quais passageiros estavam na mesma, tornando possível preencher alguns valores de cabines vazias.
      - Os outros valores foram preenchidos com a moda.
  - Foi utilizado a função **lambda** para converter os textos em valores.
  - Foram utilizados os algoritmos da etapa 4.
  - O score retornado pelo Kaggle foi: 79,72 %

## [Etapa 6: Determinando melhores parametros](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte6_MelhorParametros.ipynb)
- Na etapa 6 o objetivo foi de utilizar o **GridSearch** para determinar os melhores parâmetros para os modelos utilizados na etapa anterior.
  - O RandomForest foi oque obteve melhor acurácia, mas o resultado do Kaggle mostrou que o MLPClassifier teve uma maior taxa de acertos.
  - O score retornado pelo Kaggle foi: 79,98 %
