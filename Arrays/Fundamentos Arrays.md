Para declarar um array, utilizamos duas sintaxes:

$meses = array();

ou a mais comum:
$meses = [];

Os arrays são compostos dos indíces que são chaves de acesso, podem ser inteiros, ou strings, o recomendado é usar um, ou outro, por exemplo:

$coresFrutas = [
	'laranja => 'laranja',
	'limao' => 'verde
];

se eu dar echo $coresFrutas['limao']
isso me retorna 'verde'

O padrão é começar do 0, e depois ir crescendo, pode se utilizar a ordem que quiser, mas o recomendado é deixar no padrão.
para percorrer um array, utilizamos principalmente o foreach, um exemplo bem prático são com datas:


foreach ($meses as $chave => $valor) {

    echo $chave.$valor.'<br>';

}

  

/**

 * dataAtual

 *

 * @return string retorna uma string com a data formatada como 'terça, 05 de novembro de 2024'

 * Essa função trabalha com arrays e seus indices, por tráz dos panos, utiliza o dia no formato w (week), e usa como indíce do array dos dias da semana, retornando o dia da semana, já em mês, precisa ter um -1, pois o primeiro mês é janeiro, e retorna o int 1, então precisamos pular um indíce.

 */

function dataAtual(): string

{

    $diaMes = date('d');

    $diaSemana = date('w');

    $mes = date('n') - 1;

    $ano = date('Y');

  

    $nomesDiasDaSemana = ['domingo', 'segunda', 'terça', 'quarta', 'quinta', 'sexta', 'sábado'];

  

    $nomesDosMeses = ['janeiro', 'fevereiro', 'março', 'abril', 'maio', 'junho', 'julho', 'agosto', 'setembro', 'outubro', 'novembro','dezembro'];

  

    return $dataFormatada = $nomesDiasDaSemana[$diaSemana].', '.$diaMes.' de '.$nomesDosMeses[$mes].' de '.$ano;

}

  

echo dataAtual();