Para documentar funções, podemos utilizar o PHPDocs, essa extensão, serve pra documentar em comentários, os atributos, e a serventia dessa função.

primeiros abrimos a seção de comentários, colocamos o nome da função, e depois os atributos, e no final, o que ela faz:

/**

 * Calcula o IMC

 * @param float $altura altura em metros

 * @param int $peso peso em kilos

 * Essa função calcula a multiplicação das alturas, e faz o peso, dividido pelo resultado, e retorna o valor do IMC.

 */

  

function calcularIMC(float $altura, int $peso) {

    $divisor = ($altura * $altura);

    $IMC = ($peso / $divisor);

    return $IMC;

}

desse modo, temos documentado o que a função faz, facilitando a leitura do código.


