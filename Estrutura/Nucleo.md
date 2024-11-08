No nucleo do sistema, é comum ter um arquivo de métodos estáticos, que serão utilizados pelo sistema.

Por exemplo, pode haver uma pasta:
sistema/Nucleo/Helpers.php

Nesse arquivo helpers, usamos o namespace, e declaramos sua classe
Podemos colocar funções de validação, de conversão, e as que são mais utilizadas


 Com isso, precisamos declarar funções estáticas, e podemos usar essas funções chamando o use do namespace, por exemplo:

```php

include_once './Sistema/Nucleo/Helpers.php';

use Sistema\Nucleo\Helpers; 

echo Helpers::limparNumero('gg456h76-12');
```

