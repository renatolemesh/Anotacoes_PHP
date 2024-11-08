
O PHP tem vários filtros nativos, como de email, e URL
para utilizar, podemos fazer funções:
filter_var($email, FILTER_VALIDATE_EMAIL)

um uso prático:

$email = 'email@email.com';

$url = 'http://true.com' ;

  

function validarEmail(string $email): bool {

    return filter_var($email, FILTER_VALIDATE_EMAIL);

}

function validarUrl(string $url): bool {

    return filter_var($url, FILTER_VALIDATE_URL);

}

var_dump(validarEmail($email));

var_dump(validarUrl($url));