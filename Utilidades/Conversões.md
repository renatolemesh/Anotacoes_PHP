Podemos utilizar funções para converter coisas, por exemplo, um numero de celular, com parenteses ou traços, podemos utilizar só o numeral com o regex.


function validarNumeroCelular(string $numero_celular): mixed

{

    $numeroLimpo = preg_replace('/\D/', '', $numero_celular);

    (strlen($numeroLimpo) < 12) ? $booleano = false : $booleano = true;

    return [$numeroLimpo, $booleano];

}