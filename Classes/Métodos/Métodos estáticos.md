As funções ou métodos estaticos, são funções que podem ser chamados sem instanciar a classe, são muito utilizados
Um exemplo prático, é ter um arquivo com essas funções, por exemplo de limpar um número, e chamar ela em algum lugar.

Para declarar uma função estática, declaramos dentro da classe:

public static function validarNumero(){}

Para usar essa função, utilizamos o use do namespace da classe e chamamos a classe junto a " :: " e chamamos a função, dessa forma:

```php
include_once './Sistema/Nucleo/Helpers.php';

use Sistema\Nucleo\Helpers;

echo Helpers::limparNumero('gg456h76-12');
```

Já, se precisamos chamar a função dentro da clase, trocamos o $this, pelo self::
```php
$cpf = self::limparNumero($cpf);
```


