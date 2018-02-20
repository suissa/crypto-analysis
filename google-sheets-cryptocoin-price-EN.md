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

Then I just analyzed which function would be the best for my problem and chose [TEXTJOIN](https://support.google.com/docs/answer/7013992) because I do not need several values like JOIN that accepts an Array of values.

In this way I was able to create a function that searches the value of the currency that has its symbol in column A:

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

#### Tip - Format

Properly format your column if it is not as currency:

![](https://i.imgur.com/IWgC5Wq.png)

<br>

### Function - Profit

Before showing this formula I will show how we can deduce it.

Imagine that the value bought was 200 and the current value is 220, or 10% of profit.



We take the difference between the initial value and the final value, note here that if the final value is greater than the initial value, then having profit, the result will be a negative value:

```

=(200-220) // = -20

```

With the difference we will know the proportion of this value to the initial value, making a simple division:

```

=(200-220)/200 // = -20 / 200 = -0.1

```

And since we know that Profit should be positive, we need to multiply by `-1`:

```

=(200-220)/200*-1 // = -20 / 200 = -0.1 * -1 = 0.1

```

I just did not add one more multiplication per 100, so we have the actual **percentage**, because we will format this column in a similar way to what we did with Current Value, so we created the following formula:


```

=(initial-final)/initial*-1

```

Changing our cells was like this:

```

=(C9-D9)/C9*-1

```


#### Tip - Format

![](https://i.imgur.com/9OhCBIo.png)


<br>
<hr>

## Example - How to use?

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