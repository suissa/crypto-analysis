# Truffle


Built-in smart contract compilation, linking, deployment and binary management.
Automated contract testing with Mocha and Chai.
Configurable build pipeline with support for custom build processes.
Scriptable deployment & migrations framework.
Network management for deploying to many public & private networks.
Interactive console for direct contract communication.
Instant rebuilding of assets during development.
External script runner that executes scripts within a Truffle environment.


Truffle é um ambiente de desenvolvimento, estrutura de testes e pipeline de ativos(assets) para Ethereum, com o objetivo de tornar a vida do desenvolvedor Ethereum mais fácil. Com ele você obtém:

- compilação de contrato inteligente, ligação, implantação e gerenciamento binário incorporados.
- teste contratado automatizado com Mocha e Chai.
- treinamento de compilação configurável com suporte para processos de compilação personalizados.
- estrutura de implantação e migração Scriptable.
- gerenciamento de rede para implantação em muitas redes públicas e privadas.
- console interativo para comunicação direta de contrato.
- reconstrução instantânea de ativos durante o desenvolvimento.
- corredor de script externo que executa scripts dentro de um ambiente Truffle.


## Instalação

Tão fácil quando instalar um pacote global com NPM hehehehe:

```
$ npm install -g truffle
```

## Como usar

For a default set of contracts and tests, run the following within an empty project directory:

Para um conjunto padrão de contratos e testes, execute o seguinte comando  dentro de um diretório vazio:

```
$ truffle init
```
A partir daí, você pode executar `truffle compile`, `truffle migrate` e `truffle test` para compilar seus contratos, implantar(deploy) esses contratos na rede e executar os testes unitários associados.

Certifique-se de estar conectado a um cliente ethereum antes de executar esses comandos. Se você for novo, instale o [testrpc](https://github.com/trufflesuite/ganache-cli) para executar um servidor local RPC. Depois disso, simplesmente execute o testrpc em uma nova guia.

