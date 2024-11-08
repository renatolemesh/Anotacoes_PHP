
As validações são ferramentas utilizadas o tempo todo na programação, é possível utilizar os Filtros, porém em alguns casos eles precisam ser adaptados, um exemplo é validar uma URL:

/**

 * validar Url

 *

 * @param string $url url para validação

 * @return bool essa função retorna true caso a validação seja feita, e false caso não atenda os requisitos

 * A função valida se a URL tem menos de 10 caracteres, se contém "." e se contem os http ou https ://

 */

function validarUrl (string $url): bool

{

    if(mb_strlen($url) < 10){

        return false;

    }

  

    if(!str_contains($url, '.')) {

        return false;

    }

  

    if(str_contains($url, 'http://') or str_contains($url, 'https://')){

        return true;

    }

    return false;

}

