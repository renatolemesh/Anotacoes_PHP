O simple router é um package que permite roteamento, pra iniciar é bem simples, usamos require 'rotas.php'; no arquivo index.php
e criamos um arquivo de rotas;

```php

require 'vendor/autoload.php';
use Pecee\SimpleRouter\SimpleRouter;

SimpleRouter::setDefaultNamespace('Sistema\Controller');

SimpleRouter::get('/estrutura/blog', 'SiteController@index');

SimpleRouter::get('/estrutura/sobre', 'SiteController@sobre');

SimpleRouter::start();
```

Desse módo, definimos um namespace padrão, e fazemos as rotas, como o get, utilizando a classe SimpleRouter
Ao lado vem a rota, e o Controlador

