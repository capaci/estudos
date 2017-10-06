# VueJS

## Algumas notas da documentação

### Diferença entre computed e watch:

### Ciclo de vida da aplicação

### Contextos
Quando criamos uma instância, podemos acessar seus atributos em outros contexto, como por exemplo, fora do escopo do componente, ou então dentro de outros componentes. Isso é possível pois, ao criar o componente, o Vue faz “uma cópia” dos atributos e métodos para o objeto principal.

```javascript
app = new Vue({...});
app.name //acessa atributo name definido dentro de data
app.getName() //acessa método getName do componente
```

Porém, se utilizarmos uma propriedade que não foi definida dentro do componente, essa propriedade não será reativa, ou seja, não irá disparar eventos para atualizar em toda a interface, pois o Vue só transforma as propriedades definidas na criação do componente como reativas.

```javascript
app = new Vue({data: {name: “Rafael”}});
app.name // Rafael
app.age = 23 // cria a propriedade age, porém a propriedade não é reativa
```

## Componentes

### Componentes dinâmicos


## VUEX
Implementação da arquitetura Flux para o Vue. Flux é, a grosso modo, uma arquitetura onde centralizamos o armazenamento de dados na nossa aplicação em um componente global. Esse componente será responsável por alterar o dado e comunicar a todos os componentes que utilizam esse dado da alteração.
Isso é muito útil quando trabalhamos com aplicações que possuem muitos componentes compartilhando o mesmo dado.
Multiple views may depend on the same piece of state.
Actions from different views may need to mutate the same piece of state.

Há algumas vantagens ao se adotar esta abordagem:

    Você tem um local centralizado para adicionar/modificar seus dados;
    Está disponível para todos os componentes;
    Nenhum componente modifica a informação diretamente, garantindo a consistência dos dados;
    Ferramentas adicionais fazem do desenvolvimento uma experiência melhor.



### TRABALHANDO COM O VUEX
