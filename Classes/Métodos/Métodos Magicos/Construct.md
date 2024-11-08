Esse método é um dos mais usados nas classes, serve pra realizar uma ação assim que a classe é criada, por exemplo:

```php
class Controlador
{
    function __construct(string $texto)
    {
        echo $texto;
    }
}

$controlador = new Controlador('texto');

#dessa maneira, é exibido o 'texto' na tela.
```

