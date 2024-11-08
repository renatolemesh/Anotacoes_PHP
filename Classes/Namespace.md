Para utilizar classes, normalmente se faz uso de namespace e alias, que é a forma correta de implementar as classes no arquivo

Primeiro, no arquivo da classe, se utiliza o termo :

```php
//arquivo da classe Mensagem
namespace sistema\Nucleo;

class Mensagem
{

}
```

O ideal, é utilizar o caminho da pasta no namespace.
Para utilizar a classe de mensagem, podemos usar o include da pasta:
include './sistema/Nucleo/Mensagem.php'
Mas o ideal é utilizar o use, dessa maneira, não precisamos especificar o caminho ao incluir a classe no código:

```php
use sistema\Nucleo\Mensagem;

echo (new Mensagem())->alerta('texto');
```

Caso tenha duas classes com o mesmo nome e caminhos diferentes, basta usar o alias:

```php
use framework\Nucleo\Mensagem as Msg;

echo (new Msg())->alerta('texto');
```

Desse módo, utilizaremos o alias dela.
