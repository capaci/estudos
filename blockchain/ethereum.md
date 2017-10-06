## Ethereum

### Do Whitepaper

#### Aplicações
Em geral, três categorias de aplicações são construídas sobre a rede Ethereum
Financial applications: aplicações onde os usuários conseguem interagir com contratos, utilizando seu dinheiro para isso. Isso inclui sub-currencies, financial derivatives, hedging contracts, savings wallets, wills, and ultimately even some classes of full-scale employment contracts.
semi-financial applications: aplicações onde o dinheiro até está envolvido, mas há um proposito não monetário a ser realizado; um exemplo é quando um minerador se “auto recompensa” por resolver problemas computacionais ao mineirar um bloco.
Dapps: Aplicações que podem ser descentralizadas e não tem envolvimento financeiro, como por exemplo sistemas de votação e governança (DAOs).

##### Token Systems
Na blockchain há muitos tipos de aplicações diferentes, desde aplicações representando outras moedas, propriedades, ações, até sistemas de tokens. Um sistema de tokens, nada mais é do que um banco de dados com algumas operações:
subtract X units from A and give X units to B, with the proviso that:
(i) A had at least X units before the transaction; and
(ii) the transaction is approved by A.
O trabalho necessário para criar um sistema de tokens desse tipo, é somente programar a lógica das operações em um contrato.

Teoricamente, os tokens na rede Ethereum conseguem fazer uma coisa que na rede Bitcoin não é possível, pagar o fee das transações com o próprio token. Uma maneira de implementar isso, seria manter alguns ethers no contrato. Ao fazer uma transação, o contrato “reembolsa” o valor em ether pago pelo fee da transação e, em troca, coleta uma quantia de token desse endereço que executou a transação. Com isso, o contrato consegue vender tokens através de leilões constantes, mantendo dessa forma, o sistema sustentável.

##### Mercado Financeiro

##### Sistema de Identidade e Reputação
Algo como o Namecoin, onde a pessoa vincula um nome a um IP. Isso também pode ser levado para um sistema de registro de domínios, um exemplo disso é o ENS.


##### Armazenamento de Arquivos
Serviços de armazenamento de arquivos similar ao modelo torrent. Utilizando uma Markle Tree* para guardar o arquivo, poderia se garantir integridade do arquivo.

##### DAOs
([link direto para o paper](https://github.com/ethereum/wiki/wiki/White-Paper#decentralized-autonomous-organizations))

Organizações descentralizadas, pode-se ter comunidades também, onde membros votam para inclusão ou remoção de membros. Pode-se pensar também em corporações. As propostas para serem executadas ou não, precisariam de uma certa porcentagem de votos favoráveis ou contrários, podendo estabelecer também regras de quorum para votação. Além disso, uma idéia muito interessante, é de ter outros contratos que executam funções dessa DAO. Quando houver necessidade de se alterar o código, poderia haver uma proposta para criar um novo contrato e trocar o endereço de execução dessa função para esse novo contrato.
Em uma implementação básica dessa DAO, haveria três transações básicas:
[0,i,K,V] to register a proposal with index i to change the address at storage index K to value V
[1,i] to register a vote in favor of proposal i
[2,i] to finalize proposal i if enough votes have been made

##### OUTRAS


#### GHOST
uncle blocks

#### TAXAS DE TRANSAÇÃO (FEE)

#### TURING COMPLETENESS
A EVM é dita ser turing completa
  - Sofre do problema da parada, não sendo possível dizer quando a execução de uma função de um contrato vai parar ou não

#### CURRENCY AND ISSUANCE

#### MINING CENTRALIZATION

#### SCALABILITY

### SEGURANÇA
#### Ataques:
https://ethereum.stackexchange.com/questions/8551/methodological-security-review-of-a-smart-contract

http://martin.swende.se/blog/Devcon1-and-contract-security.html

#### The DAO Attack
[link](http://hackingdistributed.com/2016/06/18/analysis-of-the-dao-exploit/)
O ataque consistia em uma brecha na chamada da função que transferia ether para um endereço.

Um contrato é considerado um endereço e, quando recebe ether, pode executar uma função definida. O que aconteceu nesse caso, é que essa função executada pelo contrato, chamava a mesma função da DAO que executava a proposta para enviar ether para esse contrato.

Essa função da DAO não marcava uma proposta como executada antes de enviar o ether, então o que acontecia, é que entrava em loop


## File storage
[Storj](https://storj.io/) foi um dos primeiros sistemas de storage utilizando blockchain, ele trabalha através do StorjCoin(SCJX), que é um token ERC20 na blockchain da Ethereum. Este token é utilizado para pagar pelo armazenamento, agindo como um incentivo para os nodos que mantém os arquivos. Antes de fazer o upload de um arquivo, ele é dividido em blocos menores, os blocos são criptografados e só então distribuido entre vários nodos para ser "guardado".

Temos também o [FileCoin](https://filecoin.io), desenvolvido pelos mesmos criadores do [IPFS](https://ipfs.io)(protocolo p2p para armazenamento de arquivos de uma forma permanente e descentralizada). O Filecoin atua como uma "camada de incentivo" em cima da rede do IPFS. O funcionamento difere do Storj (** TODO Estudar melhor essa diferença **)

No Filecoin, os mineradores são pagos para armazenar e recuperar os arquivos, mas também recebem recompensas de mineração pela aplicação do Proof of Work. Outra coisa a ser notada, é que não existe preço pelo armazenamento do arquivo. Ao invés disso, os usuários e mineradores criam ordens de "compra e venda" de espaço, em uma espécie de exchange descentralizada.

## Notas

**\*Merkle Tree**: árvore muito utilizada em redes p2p, onde um nodo guarda a hash dos seus filhos. Isso se torna extremamente útil no compartilhamento de arquivos, onde o arquivo é dividido em blocos e é “guardado” nas folhas da árvore. Quando um usuário vai baixar esse arquivo, ele não precisa baixar o arquivo todo de uma vez, podendo baixar por ramos e, dessa forma, já ir verificando se o ramo que ele está baixando está corrompido, ao invés de baixar o arquivo todo para só então comparar a hash do arquivo recebido com a hash original.

**\*\*EVM**: Ethereum Virtual Machine, utilizada para rodar a rede blockchain e executar os smart contracts.

## Links úteis
[quando usar require() ou assert() no contrato](https://ethereum.stackexchange.com/questions/15166/difference-between-require-and-assert-and-the-difference-between-revert-and-thro)

[Boas práticas na elaboração de smart contracts](https://github.com/ConsenSys/smart-contract-best-practices)
