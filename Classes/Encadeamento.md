Algo muito utilizados nos métodos, é o encadeamento, por exemplo, uma função chamando outra função:

```php

class Classe {
    public function executar_isto() {
        //faz algo importante
        return $this;
    }
    public function executar_aquilo() {
        //faz algo mais importante
        return $this;
    }
}
$objeto = new Classe();
$objeto->executar_isto()->executar_aquilo();

```

Um exemplo prático, seria colocar uma classe CSS em um elemento:

```php
class Mensagem

{

    private $texto;

    private $css;

    /**

     * sucesso

     *

     * @param  mixed $mensagem string da mensagem

     * @return Mensagem faz encadeamento e retorna o objeto

     * Essa função é utilizada para definir uma classe css, e filtrar o texto, e para encadear com a função de renderizar

     */

    public function sucesso(string $mensagem): Mensagem

    {

        $this->css ='alert alert-success';

        $this->texto = $this->filtrar($mensagem);

        return $this;

    }

    /**

     * renderizar

     * @return string utilizamos uma string, que pode estar com tags

     * Essa função, filtra a mensagem para não entrar na estrutura html, e rendereiza o texto limpo com a tag se tiver

     */

    public function renderizar(): string

    {

        return "<div class='{$this->css}'>".$this->texto."</div>";

    }

  

    private function filtrar(string $mensagem): string

    {

        return filter_var($mensagem, FILTER_SANITIZE_SPECIAL_CHARS);

    }

}

$msg = new Mensagem();

  

echo $msg->sucesso('Mensagem de sucesso')

         ->renderizar();

echo '<hr>';

var_dump($msg);
```