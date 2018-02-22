# Como inferir fórmulas simples de Matemática

> **Eu posso afirmar-lhe categoricamente que se você souber qual é o valor inicial, final e a relação entre esses 2 valores você NÃO PRECISA SABER DA FÓRMULA**

## Como?

Antes de explicar o meu método mental para isso irei deixar aqui um texto que já tinha escrito onde eu explico a inferência da fórmula para achar o lucro entre 2 valores de cryptomoedas.

### Exemplo: Função Lucro

Antes de mostrar essa fórmula irei mostrar como nós podemos deduzir ela.

Imagine que o valor comprado foi 200 e o atual é 220, ou seja, 10% de lucro.


Pegamos a diferença entre o valor inicial e o final, perceba aqui que se o valor final for maior que o inicial, logo tendo lucro, o resultado será um valor negativo:

```

=(200-220) // = -20

```

Com a diferença nós iremos saber qual a proporção desse valor para o valor inicial, fazendo uma simples divisão:

```

=(200-220)/200 // = -20 / 200 = -0.1

```

E como sabemos que o Lucro deveria ser positivo basta multiplicarmos por `-1`

```

=(200-220)/200*-1 // = -20 / 200 = -0.1 * -1 = 0.1

```

Eu só não adicionei mais uma multiplicação por 100, para termos a **porcentagem** real, pois iremos formatar essa coluna de forma parecida com o que fizemos com o Valor Atual, com isso nós criamos a seguinte fórmula:


```

=(inicial-final)/inicial*-1

```

Trocando pelas nossas células ficou assim:

```

=(C9-D9)/C9*-1

```

### Explicação

Agora em cima desse texto que eu já tinha criado irei explicar um pouco mais como é minha metodologia de inferência de fórmulas.

Como nós já fizemos a da Porcentagem irei demontrar a velocidade.

Para calcularmos a velocidade de algo nós precisamos de 2 valores:

- distância percorrida;
- tempo gasto nisso.

Então podemos pegar um valor que qualquer um reconhece como velocidade:

> 100 km/h

Nisso notamos claramente que sua unidade de medida é exatamente o que citei anteriormente.

Então, se um carro alcança 100 km/h, isso diz que ele percorreu 100 kilômetro em 1 hora, correto?

Logo podemos inferir que a conta é:

```

100/1

100km
______
1h

```

Agora olhe que simples!

Se o resultado daquela divisão é a velocidade podemos afirmar que:


```

velocidade = distancia / tempo

```

> Simples né?

Porém precisamos também entender que a distância é baseada em 2 pontos:

- inicial;
- final.

Ou seja, se você possuir os valores de onde o carro começou até onde ele chegou, nós teremos a **VARIAÇÃO** desse espaço.

Como eu ia citar que essa variação era o **delta(Δ)** quis garantir que não estava errado pesquisando o seguinte no Google:

> Matematica delta variação

No primeiro link, da Wikipedia, já temos a seguinte resposta:

> Na matemática e nas ciências aplicadas, é comum o uso da letra maiúscula para representar a diferença entre duas variáveis, como "ΔS", que identifica o resultado da diferença entre a variável "S" em duas situações distintas. 

*fonte: [Δ - Delta](https://pt.wikipedia.org/wiki/%CE%94)*

Sabendo disso imagine comigo 2 valores de início e fim bem simples, iniciou no kilômetro 10 e finalizou no 110. Sem precisar fazer NENHUM cálculo você já sabe que a diferença/variação dessa distância foi `100`, correto?

Então perceba que você já tem todos os dados necessários para inferirmos essa fórmula também:

```

Δd = 110 - 10
Δd = 100


Δd = distFinal - distInicial

```

Você entendeu que apenas por esses dados nós inferimos que o valor a ser subtraído será SEMPRE o final, pois isso nos diz a variação entre os dois pontos.

Só para deixar em JavaScript nós escrevemos:

```

const Δd = (distInicial, distFinal) => distFinal - distInicial

console.log( Δd(10, 110) ) // 100

```

Voltando para nossa velocidade agora temos:


```

velocidade = Δd / tempo

velocidade = 100km / 1h
velocidade = 100km/h

// OU

velocidade = 3600m / 60s
velocidade = 60m/s

```

Logo podemos escrever isso em JS assim:


```

const Δd = (distInicial, distFinal) => distFinal - distInicial

const v = (Δd, tempo) => Δd / tempo

// OU

const v = (distInicial, distFinal, tempo) => Δd(distInicial, distFinal) / tempo

```