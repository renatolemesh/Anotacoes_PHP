O método __toString permite que uma classe seja convertida pra uma string, desse módo será possível dar echo no objeto chamando essa função, ela também substitui a necessidade de encadeamento ao dar echo

```php
public function __toString()
    {
        return $this->renderizar();
    }

public function renderizar(): string
    {
        return "<div class='{$this->css}'>".$this->texto."</div>";
    }

echo $msg->sucesso('Mensagem de sucesso');
```

Desse modo não tem a necessidade de por o ->renderizar após a mensagem de sucesso.