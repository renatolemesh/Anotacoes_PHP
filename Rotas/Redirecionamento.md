Para criar redirecionamentos, é comum utilizarmos uma função de redirecionamento no Helpers, e na configuração da rota, colocamos um try catch, pois quando não encontra a rota, ele lança a Exception NotFound, e a partir disso, chamamos a função de redirecionar

```php
try {
    SimpleRouter::setDefaultNamespace('Sistema\Controller');
    SimpleRouter::get('/estrutura/sobre', 'SiteController@sobre');
    SimpleRouter::start();
} catch (\Pecee\SimpleRouter\Exceptions\NotFoundHttpException $ex) {
    if(Helpers::localhost()){
        echo $ex;
    }
    Helpers::redirecionar('/estrutura/404');
}
```

```php
public static function redirecionar(string $url): void
    {
        header('HTTP/1.1 302 Found');
        $local = ($url ? self::url($url) : self::url());
        header("Location: $local ");
        exit();
    }
```

Essa função, tem um header padrão do http, e procura a url, com base na função de url que traz a base do site, no caso http://127.0.0.1 e retorna o local, no caso /estrutura
