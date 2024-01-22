# Spaceship Titanic
Repositório criado para **[competição do Kaggle sobre Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic)**

O histórico dos resultados obtidos é mostrado abaixo e pode ser encontrado no Kaggle:
<img src="https://github.com/PedroALage/Spaceship_Titanic/blob/main/pkgImages/grafEvolucao.png"/>

## [Etapa 0: Tantando base](https://github.com/PedroALage/Spaceship_Titanic/blob/main/Parte0_TratandoDados.ipynb)
- Nessa etapa foi realizada apenas o tratamento básico na base.
  - Foi visualizado um resumo da base utilizando o ydata-profiling, biblioteca capaz de gerar com poucas linhas toda a descrição do nosso dataset.
  - Foi removida as colunas com elevada cardinalidade e as colunas de texto.
  - Os valores vazios foram tratados utilizando a relação identificada entre as colunas, os que não se encontrou relação foi utilizado a média e a moda das variáveis.
