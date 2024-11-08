Os métodos são as funções dentro das classes, por exemplo, uma filtro:

```php
class Mensagem
{
    private $texto;
    /**
     * renderizar
     * @return string utilizamos uma string, que pode estár com tags
     * Essa função, filtra a mensagem para não entrar na estrutura html, e rendereiza o texto limpo com a tag se tiver

     */
    public function renderizar(): string
    {
        return $this->texto = $this->filtrar('<h1>mensagem de teste');

    }
    private function filtrar(string $mensagem): string
    {
        return filter_var($mensagem, FILTER_SANITIZE_SPECIAL_CHARS);
    }
}
```

É muito comum filtrar textos, devido a poderem ter tags html, e influenciarem na visualização, então usamos filtros como o FILTER_SANITIZE_SPECIAL_CHARS.