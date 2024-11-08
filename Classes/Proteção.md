Os atributos e métodos das classes, possuem três possibilidades:
## Public
É a camada padrão, colocando um atributo como public, é possível mudar o atributo por fora da classe, o que é bem ruim em segurança.

## Protected
É a camada média, não é possível alterar o atributo protected fora da classe, mas caso a classe tenha herança, as herdeiras podem acessar esse atributo.

## Private
É o mais seguro, desse módo, só é possível acessar o atributo dentro da própria classe.