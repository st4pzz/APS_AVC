# APS_AVC

Esse é um projeto da matéria de Algebra Linear e Teoria da Informação do Insper para o curso de Ciência da Computação.

# Projeto: Predição de AVC's

Neste projeto, projetaremos e avaliaremos o classificador linear e o classificador por árvore de decisão no problema de predizer AVCs à partir da base de dados que está disponível no Kaggle. Também, avaliaremos quais foram os fatores de risco identificados por cada um dos classificadores e, após, verificaremos se esses fatores de risco identificados pelos classificadores já foram identificados anteriormente por algum estudo na área. Para isso, vamos usar classificadores para identificar *quais são os fatores de risco para o acidente vascular cerebral (AVC)*. Um AVC (*stroke*) é um dano cerebral causado pela interrupção de seu fluxo sanguíneo. Ter um AVC é um problema sério porque pode levar a sequelas, então é melhor preveni-lo do que tentar lidar com suas consequências.

## Descrição do Projeto

Temos à nossa disposição um conjunto de dados para [predição de AVCs](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset). O que faremos é:

1. Treinar um classificador para predizer se houve ou não houve AVCs
2. Verificar a acurácia do classificador
3. Identificar quais são os fatores que mais provavelmente estão ligados a ter AVCs

## Explicação:

### Aproximação Linear

Usaremos a aproximação linear para prever outros resultados a partir das informações atuais, para isso criaremos uma linha que considere os pontos do DataFrame ou da matriz original. Realizamos um processo de *aprendizagem*, alterando a matriz de pesos ( $W^T$ ) e bias ( $b$ ), que modificam a matriz de características ( $X$ ) e nos fornecem uma matriz de valores de estimativa ( $Y^{est}$ ) . Criamos uma matriz de pesos $W^T$ e bias $b$ com valores que não são importantes, ou seja, podem ser aleatórios ou 1, pois serão corrigidos durante o processo. Em seguida, particionamos nossas matrizes originais (arrays de $X$ features e $Y$ results) em $X_{test}$ , $Y_{test}$ , $X_{train}$ e $Y_{train}$ . Treinamos nosso modelo usando arrays $train$ e testamos sua eficácia usando arrays $test$. Criamos nossa função de erro na qual estimamos a matriz $Y$ com o resultado $Y^{est}$ e retornamos o quadrado médio da diferença entre as duas matrizes (o erro). 

$$Y^{est} = W^TX + b$$

$$Erro = Média((Y-Y^{est})^2)$$

Esta função é passada para gradiente utilizando a biblioteca `autograd`, retornando o vetor gradiente da função de erro, este vetor com a derivada do erro em relação a cada parâmetro da função, sendo assim uma tupla com os novos valores de $W_{err}^T$ e $b_{err}$. Deste modo, multiplicamos $W_{err}^T$ e $b_{err}$ por $\alpha$ , que é nossa taxa de aprendizado. Pegamos esse o erro e o subtraímos dos valores originais de $W^T$ e $b$, tendo:

$$W^T = W^T - \alpha W_{err}^T$$

$$b = b - \alpha b_{err}$$

Temos assim, $W_{err}^T$ e $b_{err}$ que se assemelham à equação mais próxima da linha dos pontos originais, verificaremos a eficácia do modelo por comparação. Primeiro, calculamos $Y^{est}$ para $X^{test}$. Agora usamos a função de precisão para calcular a precisão do modelo.


### Hipótese Nula

A hipótese nula é a acurácia de um modelo que sempre categoriza algo como o resultado mais frequente. Nesse caso, temo a quantidade de vezes que o resultado mais frequente ocorreu ($r$) dividida pelo número total de resultados ($N$).

$$H_{0} = \frac{r}{N}$$

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


### [CSV de predição de AVCs](https://github.com/st4pzz/APS_AVC/blob/main/healthcare-dataset-stroke-data.csv)

## Autores

- [@st4pzz](https://github.com/st4pzz)
- [@WeeeverAlex](https://github.com/WeeeverAlex)
