Os atributos, são as "váriaveis" dentro das funções
Por exemplo:


```php
class Mensagem
{
	public $texto;
}

$msg = new Mensagem();
echo $msg->texto
```
Para chamar o atributo, utilizamos a classe, e a flecha "->" para chamar o atributo, sem o cifrão "$"

No caso de um atributo publico, é possível trocar o valor pra $msg->texto = 'mudando a string';

Já, no caso de chamar ele dentro da classe, precisamos usar o identificador $this

```php
public function renderizar(): string

    {

        return $this->texto = $this->filtrar('<h1>mensagem de teste');

    }
```

Nesse caso, chamados o atributo texto com o $this->atributo



