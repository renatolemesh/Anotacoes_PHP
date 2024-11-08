É comum ter ambiente de produção e de desenvolvimento, uma função muito usada para isso é verificar a url, caso a url seja localhost, está no ambiente dev, se for outra, de prod, uma função que verifica isso é essa:

define('URL_PRODUCAO', 'https://www.dominio.com');

define('URL_DESENVOLVIMENTO', 'localhost');

/**

 * localhost

 *Função localhost

 * @return bool Retorna true caso o input do servidor seja do localhost

 */

function localhost(): bool

{

    $servidor = $_SERVER['SERVER_NAME'];

    if($servidor == 'localhost') {

        return true;

    }

    return false;

}

Também é comum utilizar urls para o ambiente, então pra diferenciar, usamos essa função:

/**

 * gerar url

 *

 * @param string $url caminho final da url

 * @return string retorna o caminho completo da url

 * Essa função serve para verificar o ambiente de dev ou prod, e concatenar com a url informada

 */

function url(string $url): string

{

    $servidor = $_SERVER['SERVER_NAME'];

    $ambiente = ($servidor == 'localhost' ? URL_DESENVOLVIMENTO : URL_PRODUCAO);

    if(str_starts_with($url, '/')) {

        return $ambiente.$url;

    }

    return $ambiente.'/'.$url;

}