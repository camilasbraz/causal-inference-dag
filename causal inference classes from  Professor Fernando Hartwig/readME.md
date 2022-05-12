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
Os caminhos backdoor podem ser identificados formalmente

![Screen Shot 2022-05-11 at 20 10 10](https://user-images.githubusercontent.com/45129483/167961982-f0f12358-57d5-46cc-9197-33f4027848f1.png)

## #7 Inferência causal (aula 2, parte 3/7) | Gráficos acíclicos direcionados: d-separação e d-conexão

#### d-separação e d-conexão
Duas variáveis estão d-separadas se não há caminhos abertos entre elas. Do contraário, diz-se que estão d-conectadas.

##### REGRA 1: A presença de uma variável de colisão automaticamente bloqueia o caminho

![Screen Shot 2022-05-11 at 21 39 31](https://user-images.githubusercontent.com/45129483/167969450-89b6be9c-6f05-4acc-a9c5-4cf4044564f1.png)
![Screen Shot 2022-05-11 at 21 40 43](https://user-images.githubusercontent.com/45129483/167969526-f9853e21-b6b1-48e1-ab91-43936aee09dd.png)

Não é porque duas veriáveis tem efeito casusal sobre uma terceira variável não significa que exista uma relação entre elas


##### REGRA 2: Ajustar uma variável de colisão abre o caminho para suas variáveis pai
(caixa --> ajustar)

![Screen Shot 2022-05-11 at 21 44 14](https://user-images.githubusercontent.com/45129483/167969837-c93e2c69-df00-407f-8d28-dfa11ee5e403.png)

#### REGRA 2b: Ajustar uma variável para um descendente de collider também abre o caminho

![Screen Shot 2022-05-11 at 21 45 08](https://user-images.githubusercontent.com/45129483/167969929-6e5b2dd6-db9a-4e8f-a32a-1fd6cc7819cb.png)


Problema de ajustar um collider:

Exemplo com estratificação: só pegamos imóveis baratos
![Screen Shot 2022-05-11 at 21 47 37](https://user-images.githubusercontent.com/45129483/167970107-4d471809-0962-4b87-824d-eed62152c090.png)

#### REGRA 3: Ajustar para pelo menos uma variável não collider bloqueia o caminho entre as variáveis pai

![Screen Shot 2022-05-11 at 21 50 29](https://user-images.githubusercontent.com/45129483/167970333-2d3944ca-8da1-4a16-b31d-b6af150c5cfa.png)

Juntando as 3 regras: condicionar, ajustar ou controlar uma variável inverte seu papel com relação à d-conexão e d-separação

#### REGRA DA COMPATIBILIDADE: Se duas variáveis estão d-separadas, elas não têm associação estatística.

![Screen Shot 2022-05-11 at 21 54 07](https://user-images.githubusercontent.com/45129483/167970641-b2f9448d-5989-44d6-afc2-3369591283fc.png)

#### REGRA DA FIDELIDADE: Se existe um ou mais caminhos abertos entre duas variáveis, em geral, estas variáveis apresentarão associação estatística
(Fidelidade perfeita(existe associação estatística) x fidelidade imperfeita(pode existir associação estatística))
![Screen Shot 2022-05-11 at 21 56 23](https://user-images.githubusercontent.com/45129483/167970820-23a0a46f-0a9b-4332-993c-a2923a622f41.png)

## #8 Inferência causal (aula 2, parte 4/7) | Utilizando DAGs para identificação e ajuste para vieses

#### Critério backdoor para reduzir viés
1) Excluir todas as setas que saem de X
 - Desse modo, qualquer associação entre X e Y deve-se a viés
2) Identificar todos os caminhos abertos de X até
 - Se houverem, os caminhos abertos de X até y são backdoor
3) Bloquear todos os caminhos identificados no passo 2
 - Cuidados:
  - Não abrir caminhos backdoor ao ajustar coliders
  - Não ajustar para descendentes de X
4) Avaliar a associação entre X e Y ajustando para um conjunto de variáveus que, com base no DAG, bloqueiam todos os caminhos backdoor
 - Espera-se que não exista associação, a menos que exista um caminho causal entre X e Y

Lembrar de não ajustar para mediadores

## #9 Inferência causal (aula 2, parte 5/7) | Definição de confundimento utlizando DAGs

#### Gráfico M

![Screen Shot 2022-05-11 at 22 27 05](https://user-images.githubusercontent.com/45129483/167973631-01636722-c69c-49ab-a49c-6e15b8bacf68.png)

U é um confudidor??

![Screen Shot 2022-05-11 at 22 28 02](https://user-images.githubusercontent.com/45129483/167973719-5aa9488a-e06a-42b1-a0c3-dccd127b1323.png)

Exemplo: 
![Screen Shot 2022-05-11 at 22 34 52](https://user-images.githubusercontent.com/45129483/167974328-8c6cbdfa-6c05-4a8e-bcbf-7cb483059c7d.png)


![Screen Shot 2022-05-11 at 22 52 09](https://user-images.githubusercontent.com/45129483/167976146-6261a35d-d67d-4c0c-9e02-2af795527c22.png)


##### Definição estrutural de confundimento: Leva em consideração o DAG, biés devido a causas comuns entre X e Y
##### Definição de confundidor: ao ser ajustado, fechamos o caminho backdoor


![Screen Shot 2022-05-11 at 22 57 53](https://user-images.githubusercontent.com/45129483/167976745-d5bc40d9-948c-4589-8b26-5e603d487931.png)


1) Sim, confundidor
2) Não, não confundidor
3) Não, confundidor
4) Sim,  não confundidor


## #10 Inferência causal (aula 2, parte 6/7) | Representando viés de seleção e viés de informação nos DAGs

#### Viés de seleção
Distorção da associação causada pelo processo de seleção dos indivíduos para a análise

- No processo de amostragem (viés de sobrevivência)
- Após a amostragem (critérios de exclusão, recusa, perdas. por acompanhamento, análises estratificadas)



![Screen Shot 2022-05-11 at 23 13 42](https://user-images.githubusercontent.com/45129483/167978381-f593cfab-9208-4797-a4a9-a1674afa4539.png)

Dependendo do padrão de perdas, a validade/qualidade do estudo pode ser perdida



![Screen Shot 2022-05-11 at 23 17 34](https://user-images.githubusercontent.com/45129483/167978796-05303544-67b7-4d02-af23-e5a346d4bc8a.png)


#### Viés de Informação
Refere-se à mensuração de variáveis

![Screen Shot 2022-05-11 at 23 24 19](https://user-images.githubusercontent.com/45129483/167979559-c55365b4-6f9e-4b5b-96a1-d81a6e810ff9.png)





![Screen Shot 2022-05-11 at 23 29 34](https://user-images.githubusercontent.com/45129483/167980040-b2e65c7f-4507-4f5d-b6a6-219122e6521e.png)


Associação espúria: relação estatística entre duas variáveis sem sem ser de causa e efeito

Proxy: variáveis mensuráveis relacionadas a um conceito


## #11 Inferência causal (aula 2, parte 7/7) | Resumo da aula 2









