As expressões regulares (regex) são formas de substituir strings, procurar caracteres especificos, e é muito usada a todo momento, para verificar, tem o site regexphplive

alguns exemplos:

$numero_limpo = preg_replace('/[^0-9]/', '', $numero);
a expressão regular '/[^0-9]/' procura tudo que não é númerico entre 0 e 9
essa expressão procura números repetidos: '/(\d)\1{10}/'

```php
$cpf = '-123.45,6789m10';

  

/**

 * limparNumero

 *

 * @param  mixed $numero numero com caracteres diferentes de numeros

 * @return string retorna o número limpo

 * Essa função filtra só os valores númericos

 */

function limparNumero(string $numero): string

{

    $numero_limpo = preg_replace('/[^0-9]/', '', $numero);

    return $numero_limpo;

}

  

echo limparNumero($cpf);

  

/**

 * validarCpf

 *

 * @param  mixed $cpf cpf em string

 * @return bool

 * Essa função converte o cpf em somente numeros, e caso tenha menos de 11 caracteres, ou seja numero repetido, retorna false

 */

function validarCpf(string $cpf): bool

{

    $cpf = limparNumero($cpf);

    if (mb_strlen($cpf) != 11 or preg_match('/(\d)\1{10}/', $cpf)) {

        return false;

    }

    return true;

}
```