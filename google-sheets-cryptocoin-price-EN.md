Today I had to create a spreadsheet to manage my cryptocoins portfolio.

Later this month I will create a Dashboard Web to show this information more easily and beautifully, as well as providing various reports. But while it's not ready I've created a spreadsheet to advance the service and by doing so I've discovered a very useful * Add-on * for anyone who wants to manage their profits on top of those digital assets.

![Final spreadsheet](https://i.imgur.com/i3h7hgR.png)

<br>
<hr>

## Add-on - CRYPTOFINANCE

[This *add-on*](https://chrome.google.com/webstore/detail/cryptofinance/bhjnahcnhemcnnenhgbmmdapapblnlcn) is the simplest way to provide the current value of any cryptocoin on the market, only needing to use the function/formula:

```
=CRYPTOFINANCE("ADA/BTC")
```

<br>


## Function - TEXTJOIN

While I was creating the lines of each coin, I asked myself:


> Is there an automatic way to create the `"COIN/BTC"` String? I already have the symbol for each one in the first column.


![](https://i.imgur.com/67qO1UY.png)

So I searched Google and found the following link:


- [https://support.google.com/docs/table/25273?visit_id=1-636544947571461454-1779998409&hl=en&rd=2](https://support.google.com/docs/table/25273?visit_id=1-636544947571461454-1779998409&hl=en&rd=2)

And I just searched for: `join`. Because I knew it should be something like that.

![](https://i.imgur.com/7sZA8hJ.png)

Depois apenas analisei qual função seria a melhor para o meu problema e escolhi a [TEXTJOIN](https://support.google.com/docs/answer/7013992) pois eu não precisarei de vários valores como na JOIN que aceita um *Array* de valores.

Dessa forma consegui criar uma função que busca o valor da moeda que possui seu símbolo na coluna A:

```

=CRYPTOFINANCE(TEXTJOIN("/", TRUE, A3, "BTC"))

```

Para você poder reusar essa mesma fórmula nas outras linhas da planilha basta fazer a mesma ação que faria no Excel, basta clickar e segurar no canto inferior direito da célula e arrastar parar baixo até a linha final desejada, pois assim o valor de `A3` irá mudar **apenas** o número da linha e não a coluna.

![](https://i.imgur.com/EfiEeGx.png)
![](https://i.imgur.com/8arlcAt.png)


> Agora sim você consegue reusar ela sempre que quiser!


<br>
<hr>

## Bonus

### Function - Valor Atual

Nessa função nós precisamos fixar qual é a célula que possui o preço atual do Bitcoin, que é a `H2`, para que possamos multiplicar pelo resultado da Quantidade vezes o Preço Atual.

- Quantidade: B{3};
- Preço Atual: D{3};
- Preço Atual Bitcoin: H2;

Para fixar a célula do Preço Atual Bitcoin iremos utilizar o `$`, deixando assim: `$H$2`.

Dessa maneira nós fixamos que sempre será a coluna `H` e sempre a célula: `2`:


```

=(B3*D3)*$H$2

```

#### Dica - Format

Formate corretamente sua coluna caso ela não esteja como moeda:

![](https://i.imgur.com/IWgC5Wq.png)

<br>

### Function - Profit

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


#### Dica - Format

![](https://i.imgur.com/9OhCBIo.png)


<br>
<hr>

## Exemple - How to use?

Você pode utilizar meu [exemplo rodando](https://docs.google.com/spreadsheets/d/1s-WnUpyG2jv_rFXOslO7lcClkpa8x1QE26kkHJwa8j4/edit?usp=sharing) criando uma cópia dele.


![Criando uma cópia da planilha](https://i.imgur.com/JYI0Iv0.png)

<br>

Depois basta RENOMEAR ela para o que você desejar e seguir os passos das imagens abaixo:

![Planilha copiada](https://i.imgur.com/vzY6OxT.png)

<br>

Adicionar o *Add-on* na sua planilha:

![Click em Get Add-on](https://i.imgur.com/iDXTiKW.png)

<br>

Procurar o *Add-on* e adicioná-lo:

![Procure por cryptofinance](https://i.imgur.com/19oAruP.png)

<br>

Depois basta esperar carregar os dados:

![Carregando os dados](https://i.imgur.com/dTNfEBf.png)


**Caso sua planilha não saia desse carregamento logo você deverá fazer um REFRESH(Ctrl+R) na página.**

<br>

> **Por hoje é só, espero que esse meu exemplo sirva para alguém, assim como essas explicações ehhehehhe.**


<br>

![Bye Bye](https://vignette.wikia.nocookie.net/yandere-simulator-fanon/images/6/63/7e79d0db2452984041abc0a553cbc495_okay-i-see-bye-now-g-topsy-okay-bye-memes_800-444.jpeg/revision/latest/scale-to-width-down/640?cb=20170405092917)

*Image from: http://yandere-simulator-fanon.wikia.com/wiki/File:7e79d0db2452984041abc0a553cbc495_okay-i-see-bye-now-g-topsy-okay-bye-memes_800-444.jpeg*


*ps: todas as outras imagens são printscreen meus.*