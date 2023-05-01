# APS_AVC

Esse é um projeto da matéria de Algebra Linear e Teoria da Informação do Insper para o curso de Ciência da Computação.

# Projeto: Predição de AVC's

Neste projeto, projetaremos e avaliaremos o classificador linear e o classificador por árvore de decisão no problema de predizer AVCs à partir da base de dados que está disponível no Kaggle. Também, avaliaremos quais foram os fatores de risco identificados por cada um dos classificadores e, após, verificaremos se esses fatores de risco identificados pelos classificadores já foram identificados anteriormente por algum estudo na área. Para isso, vamos usar classificadores para identificar *quais são os fatores de risco para o acidente vascular cerebral (AVC)*. Um AVC (*stroke*) é um dano cerebral causado pela interrupção de seu fluxo sanguíneo. Ter um AVC é um problema sério porque pode levar a sequelas, então é melhor preveni-lo do que tentar lidar com suas consequências.

### [CSV de predição de AVCs](https://github.com/st4pzz/APS_AVC/blob/main/healthcare-dataset-stroke-data.csv)

## Modelo matemático e Explicação

Primeiramente, colocamos os dados em dados teste e de treino, o modelo foi criado por meio de regressão linear, definiu-se a função de perda, a matriz de peso $p$ , que define a relevância de cada uma das características para determinar se uma pessoa teria um AVC ou não, e o valor bias, $b$, também calculamos o gradiente da função de perda. O objetivo do algoritmo é minimizar a função de perda, encontrando os valores de $p$ e $b$ que minimizem a diferença entre as previsões do modelo e os valores reais. Usamos o gradiente descendente para calcular a perda em relação a $p$ e $b$, ajustamosos parâmetros em relação ao gradiente usando a taxa de aprendizagem. O modelo, aprende a melhor combinação de valores para fazer previsões sobre os dados de entrada, utilizando da função de perda que fornece uma medida de como as previsões estão sendo feitas  e dos ajustes ods valores que as melhoram. Deste modo, maximizando a precisão do modelo. Por fim através do peso, $p$, obtido, foi possível concluir que os principais fatores de risco para o AVC estão relacionados a hipertensão e tabagismo. 

## Como rodar o projeto e Funcionalidades

### Clone o repositório do nosso projeto:

```py
https://github.com/st4pzz/APS_AVC
```

### Depois instale os requirements:

```py
pip install -r requirements.txt
```

## Por fim, basta executar o arquivo notebook.ipynb: 

```py
python notebook.ipynb
```

## Resultado final

Nos concluimos que os principais fatores de risco para o AVC estão relacionados a hipertensão e tabagismo. Além disso pesquisamos em diversos sites sendo o principla site pesquisado o do governo, e vimos que a hipertensão e tabagismo são um dos principais riscos para desenvolver um AVC.

### [Referência do gov.br](https://www.gov.br/saude/pt-br/assuntos/saude-de-a-a-z/a/avc)


## Autores

- [@st4pzz](https://github.com/st4pzz)
- [@WeeeverAlex](https://github.com/WeeeverAlex)
