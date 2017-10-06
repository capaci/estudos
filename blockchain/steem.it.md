## Steem

[Whitepaper](https://steem.io/SteemWhitePaper.pdf)

### Algoritmo de consenso
Nas redes comuns de blockchain, o consenso é atingido por alo

### Problemas comuns do blockchain

#### Fee
Nas redes mais comuns de blockchain, existe uma taxa para cada transação que é executada na rede. Isso é totalmente normal, visto que é um processo que é utilizado para evitar spam na rede, ou seja, alguém fazendo milhares de pequenas transações somente para ocupar a rede (acho que podemos equiparar isso a um ataque [dos - denial of service](https://en.wikipedia.org/wiki/Denial-of-service_attack)). Dessa forma, o atacante não vai ficar spamando a rede, já que ele vai perder muito dinheiro com isso.

O problema que de todo esse processo, é que isso se torna inviável transações com valores pequenos. Vamos tomar por base as transações de Bitcoin hoje (06/out/2017). Atualmente, o fee das transações, se convertermos para dólares gira em torno de US$12. Isso é totalmente aceitaval para grandes transações do mercado financeiro, visto que os bancos cobram taxas percentuais altissímas sobre o valor a ser transacionado. Porém, isso é totalmente inviável para transações de valores pequenos. Um exemplo é que eu vi em um grupo de facebook um vendedor de pipoca que aceitava bitcoin na compra de um saquinho. Um saquinho de pipoca custa R$5, porém para transferir o valor para ele, o cliente gastaria mais US$12 na transação. Inviável.

E quando falamos que é inviável para pequenas transações, não estamos falando apenas desse tipo de transação que eu citei, do vendedor de pipoca. Se quisermos realmente utilizar a blockchain para construir nossas aplicações, como vamos fazer nosso usuário gastar esse pequeno fee para cada transação que ele fizer? Imagina uma troca de senha, um "curtir", um comentário. Se o nosso usuário tiver que pagar por isso, ele não vai pagar...
Outro contra é que o fee vai se ajustando ao longo do tempo, então cada vez que o usuário vai executar uma determinada transação, ele paga uma taxa diferente. Isso deixa a experiência do nosso usuário horrível.

O Steem tenta resolver esse problema, como... eu ainda vou descobrir.
