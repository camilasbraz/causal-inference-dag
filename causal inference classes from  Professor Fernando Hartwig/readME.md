# Causal inference classes from Professor Fernando Hartwig
<!-- (fazer até aula 3 parte 2 hoje(11/05)) -->
### Playlist link: <a href="https://www.youtube.com/watch?v=U7qhODzS1Bs&list=PLQeeqx5FCkGA51xOlwxjj2bJOYsxUOyTE"> Causal inference </a>

## #1: Inferência causal (aula 1, parte 1/4) | Introdução ao modelo de desfechos potenciais

### Modelo de desfechos potencias

Como definir efeitos causais?
- Tabagismo (exposição) e câncer de pulmão (desfecho) --> Tabagismo tem efeito causal sobre o câncer de pulmão

Precisamos de uma situação contrafactual (contrária aos fatos) para verificar se uma exposição tem efeito causal sobre um desfecho.Entretando, é impossível existir esse universo contrafactual, pois seria um universo idêntico ao do desfecho mas com uma única diferença, a exposição não aconteceu.

Temos então desfechos potenciais. O nome potencial vem do fato de que que antes da exposição, qualquer um dos dois desfechos são possíveis (podem acontecer).

Após a ação, temos o desfecho observado, correspondente à ação realizada, e o desfecho contrafactual, correspondente à ação não realizada

#### Modelo
Variável de exposição binária `X`
 - Não-exposto: X = 0
 - Exposto: X = 1

Variável desfecho dicotômica T
- Insucesso: Y = 0
- Sucesso: Y = 1

Y se refere ao desfecho observado, não aos desfechos potenciais
Y(X = 0): desfecho potencial referente à não exposição
Y(X = 1): desfecho potencial referente à exposição

Não conseguimos concluir nada sobre o desfecho da ação que não aconteceu pois precisaríamos do universo contrafactual (corresponde a uma ação que não aconteceu)

![Screen Shot 2022-05-11 at 15 22 59](https://user-images.githubusercontent.com/45129483/167919643-7cdc7f09-2b45-4064-b891-69b2eb960bd8.png)

### Efeito causal individual
Contraste entre desfechos potenciais
ECI = Y(X = 1) - Y(X = 0) 
Se ECI < 0 --> relação causal

#### Problema fundamental da inferência causal: só temos um desfecho potencia;, logo, falta dado para inferir. É IMPOSSÍVEL ESTIMAR EFEITOS CAUSAIS COM BASE NOS DADOS

## #2: Inferência causal (aula 1, parte 2/4) | Efeitos causais médios ou agregados


### Heterogeneidade dos efeitos causais individuais

#### O efeito causal é o mesmo para todas as pessoas??
Não, as diferenças entre os indivíduos na presença ou ausência dos modificadores de efeito

#### Tipo de efeito/indivíduo

![Screen Shot 2022-05-11 at 16 56 44](https://user-images.githubusercontent.com/45129483/167935079-c2c12447-0c4c-47bc-89d7-fd76e4450f36.png)



#### Heterogeneidade dos efeitos causais individuais
![Screen Shot 2022-05-11 at 17 00 23](https://user-images.githubusercontent.com/45129483/167935970-56df48f7-ac19-46d0-bead-e359de8bce9f.png)

#### Efeito causal médio
- Média aritmética dos ECIs
- Média do desfecho em populações totalmente expostas ou sem exposição
- Pode ser feito dentro de subgrupos
- É utilizado para controle de confundimento, identificar subgrupos em que a exposição é efetiva e compreender melhor os mecanimos de exposição


## #3 Inferência causal (aula 1, parte 3/4) | Condições necessárias para estimar efeitos causais

Como lidar com o problema fundamental da inferência causal?
Suprir a ausência de informações sobre o desfecho contrafactual por meio de pressupostos (mais plausíveis ou menos plausíveis dependendo da qualidade do estudo feito)

Temos que estimar o ECM e, para isso, precismos de 3 condições no estudo
- Positividade
- Permutabilidade
- Contraste causal bem-definido


### Positividade
- A exposição deve variar entre os indivíduos dentro dos subgrupos de interesse --> precisamos comparar



### Permutabilidade
- Habilidade ou capacidade de trocar
- Ausência de viés sistemático (associaçao entre as variáveis de exposição e desfecho não está sujeita a distorções como confusão, informação e seleção)
- Expostos e não-expostos são comparáveis


Estimamos a associação entre X e Y

Ensaios clínicos randomizados são etimativas de efeitos causais pois, assumindo que é 100% randomizado, a média dos expostos, não expostos e amostra total são iguais (são comparáveis) para qualquer variável. Ou seja, na presença de randomização, associação = causalidade, pois podemos assumir que o desfecho observado em um grupo é igual ao desfecho contrafactual no outro grupo.


![Screen Shot 2022-05-11 at 17 50 18](https://user-images.githubusercontent.com/45129483/167945263-13fcfe40-02a7-4646-91d6-6f70195cdf7e.png)

Em estudos perfeitos, não temos o problema fundamental da inferência causal, mas em estudos reais ele se aplica por falhas, vieses ou tamanho amostral.


### Contraste causal bem-definid
- Ausência de interferência: o efeito da exposição sobre o desfecho em um indíviduo não é influenciado por outros indivíduos na mesma população terem sido ecpstos ou não. Os ECIs dependem de três fatores: se o indivíduo foi exposto ou não, caractarísticas do indivíduo e características contextuais.

- Irrelevância de variações da exposição: a presença de múltiplas variações de cada valor da variável de exposição pode resultar em um efeito causal mal definido, difícil de interpretar (ter muitas exposições, exemplo: sobrepeso-obesidade e mortaldiade. A exposição pode ser obesidade, sobrepeso, peso normal e baixo peso) --> Exposição deve ser definida em detalhes suficientes



## #4 Inferência causal (aula 1, parte 4/4) | Resumo da aula 1

## #5 Inferência causal (aula 2, parte 1/7) | Introdução aos gráficos acíclicos direcionados
DAGs: codificar de forma gráfica os pressupostos da inferência causal

##### TEMPORALIDADE 

Gráfico: representação gráfica das relações causais entre as variáveis
Direcionados: relações de causa e consequência mostradas por setas
Acíclios: não formam ciclos 

![Screen Shot 2022-05-11 at 19 49 25](https://user-images.githubusercontent.com/45129483/167959930-feb75c39-c7a9-4517-a24e-dd720bb22c20.png)

Permite idenficar confundidores, mediadores e outros vieses

Exemplo de uma DAG:

![Screen Shot 2022-05-11 at 19 55 43](https://user-images.githubusercontent.com/45129483/167960574-732bfe64-894e-4eb6-97a1-6076c2db096f.png)

Desenhar ou não desenhar uma seta é uma afirmação entre as relações causais das variáveis

## #6 Inferência causal (aula 2, parte 2/7) | Terminologia e interpretação dos DAGs
Exemplos de dags, interpretações e terminologias:
X é uma causa de Y
![Screen Shot 2022-05-11 at 19 59 41](https://user-images.githubusercontent.com/45129483/167960990-86e6bb72-0057-43b2-b615-b0ebc2d8e69d.png)
![Screen Shot 2022-05-11 at 20 03 07](https://user-images.githubusercontent.com/45129483/167961309-fcd9af68-c114-40e4-b8ac-bafd1a48ed85.png)

### Caminhos causais e caminhos backdoor
Caminho: formas de passar pelas variáveis. Eles podem ser causais ou backdoor, que são caminhos enviesantes (confusão e viéses). 
Os caminhos backdoor podem ser identificados formalmente ![Screen Shot 2022-05-11 at 20 10 10](https://user-images.githubusercontent.com/45129483/167961982-f0f12358-57d5-46cc-9197-33f4027848f1.png)
