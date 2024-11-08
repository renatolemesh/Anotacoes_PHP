Para tratamento de exceções, utilizamos o try/catch, a estrutura é bem parecida com if/else:

```php
try{

    $msg->renderizar();

} catch (Exception $e) {

    echo $e->getMessage();

} finally {

    echo 'sempre aparece';

}
```
Desse modo, primeiro é tentado renderizar, caso de algum erro, é armazenado na var $e, e coletado somente a mensagem com a função getMessage(), já o finally, é opcional, é algo que sempre aparece.

