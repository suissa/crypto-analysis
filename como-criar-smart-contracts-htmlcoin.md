Como criar um simples token na rede de smart contracts da HTMLCOIN

1 - Abra o Solidity Compiler da Ethereum em https://ethereum.github.io/browser-solidity/ ou pelo botão existente na aba de Smart Contract na carteira HTML.

2 - Feche e delete qualquer coisa que talvez venha aberto no Solidity

3 - Crie um novo arquivo com o nome do seu token Ex: zequinhacoin.sol

4 - Entre no link https://ethereum.org/token#the-code 

5 - Copie tudo em "THE CODE" a apartir de "pragma solidity ^0.4.18;" e cole no Solidity, no mesmo arquivo "zequinhacoin.sol" que vocÍ criou

6 - Na nona linha "uint8 public decimals = 18;", troque o 18 por 8

6.2 - Na quinta linha "contract", troque "TokenERC20" pelo nome do seu token Ex: ZequinhaCoin

6.3 - FaÁa o mesmo na linha "function TokenERC20"

7 - Entre em https://github.com/ConsenSys/Tokens/blob/master/contracts/eip20/EIP20Interface.sol e copie tudo a partir de "pragma solidity ^0.4.18;"

8 - Crie um novo arquivo no Solidity chamado de "Interface.sol" e cole o que vocÍ copiou acima

9 - Feito isso, aperte o bot„o "Start to compile"

10 - Agora abra a carteira HTML e aguarde sincronizar

11 - Abra a opÁ„o "Smart Contract" e logo depois "Create"

12 - Ter· dois campos para preencher, "Bytecode" e "Interface (ABI)"

13 - Volte ao Solidity e em baixo do bot„o "Start to compile", selecione seu Token Ex: ZequinhaToken

14 - Clique em "Details"

15 - La nos detelhes vai ter o "BYTECODE", vocÍ vai copiar todo cÛdigo em "object" como na imagem https://imgur.com/wUQigVa

16 - Cole tudo em "Bytecode" na carteira HTML e se der certo vai ficar assim https://imgur.com/wXX7KEp

17 - Se ficar vermelho, vocÍ copiou e colou errado, se vire

18 - Agora l· no Solidity novamente, abaixo de "BYTECODE", em "ABI" copie tudo apertando no bot„ozinho https://imgur.com/vWMAUne

19 - Cole tudo no segundo campo "Interface (ABI)" na carteira HTML 

20 - Se vocÍ fez tudo certo atÈ aqui, na parte "Constructor" vai aparecer mais opÁıes https://imgur.com/Mszqkaa

21 - Em "uint256 initialSupply" vocÍ coloca quantos tokens quer criar Ex: 100000 ZEQUINHAS

22 - Em "string tokenName" vocÍ coloca o nome do seu token Ex: ZequinhaCoin

23 - Em "string tokenSymbol" vocÍ coloca o simbolo do token Ex: ZEQUINHA/ZEQ/ZQT

24 -  Vai ficar assim https://imgur.com/T4tLlvG

25 - Logo abaixo em "Gas Limit" pode deixar 2500000 caso vocÍ n„o entenda o suficiente o que È o GAS (nem eu sei, ent„o deixa quietinho)

26 - Defina o "Gas Price" para qualquer valor acima de 40 satoshi de HTML. Lembrando, sempre que for enviar os tokens para outro endereÁo, vocÍ deve colocar um valor equivalente ou superior ao Gas Price do seu token, se n„o a transaÁ„o n„o ser· efetivada

27 - Em "Sender Address" defina a wallet que vai armazenar os tokens 

28 - Vai ficar assim https://imgur.com/gt8Iwkr

29 - Clique em "Create Token", coloque a senha da carteira caso esteja criptografada e dÍ um "OK" 

30 - Pronto, seu contrato foi criado e enviado para a rede HTML https://imgur.com/pjKYghr

31 - VocÍ tem que ter saldo na carteira para criar o token, quanto maior o "Gas Price", maior ser· o quanto vocÍ vai pagar

32 - Quando vou poder usar meu token? VocÍ vai poder usar os tokens quando a rede te retornar parte dos HTML's (em forma de mineraÁ„o) usados para pagar o contrato https://imgur.com/I7Thb72 (Contract send = Contrato Pago) (Minerado = Contrato Confirmado)

================================================================================================================================================================

COMO ADICIONAR E USAR OS TOKENS

1 - Logo no inicio da carteira clique em "Add Token" https://imgur.com/kniAnzF

2 - Em "Contract Address" vocÍ sÛ vai precisar colocar o endereÁo do contrato que vocÍ gerou e a carteira onde vocÍ colocou os tokens https://imgur.com/EEnPz1a -https://imgur.com/fmfjEhe

3 - O preenchimento È feito autom·ticamente https://imgur.com/qONa9gA

4 - Clique em "Confirm"

5 - E pronto, seus tokens est„o visiveis e usuais https://imgur.com/I5ZB7mB

6 - Para enviar È sÛ clicar em "Send" e preencher https://imgur.com/09XKcko

7 - Lembre-se sempre de colocar o "Gas Price" certo (igual ou superior) https://imgur.com/cWds3R1

8 - Coloque sua senha caso a carteira esteja criptografada e confirme o envio dos seus tokens https://imgur.com/4tZodev

9 - Pra receber È sÛ dar seu endereÁo nÈ


Tutorial by TheOdyssey - 26/02/2018
Telegram: @thodyssey
DOE HTML PORQUE N√O FOI F¡CIL DE FAZER, ENOIS: Ho6xP2Nf7rCmZV5CHeBMdn9rFVCSoGoH4W

