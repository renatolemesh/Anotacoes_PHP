
Essa função serve pra transformar textos em urls amigaveis, por exemplo:

"Um milhão"

converte pra um-milhao

function slug(string $text, string $divisor ='-'): string

{

  

  // substitui caracteres diferentes de letras pelo divisor

  $text = preg_replace('~[^\pL\d]+~u', $divisor, $text);

  

  // conversão para caracteres americanos

  $text = iconv('utf-8', 'us-ascii//TRANSLIT', $text);

  

  // remove caracteres especiais

  $text = preg_replace('~[^-\w]+~', '', $text);

  

  // corta os espaços antes e depois

  $text = trim($text, $divisor);

  

  // remove os divisores duplicados

  $text = preg_replace('~-+~', $divisor, $text);

  

  // Conversão pra minusculas

  $text = strtolower($text);

  

  if (empty($text)) {

    return 'n-a';

  }

  

  return $text;

}