
Para definirmos uma data no PHP, utilizamos a função nativa date()
Ela é um int, com o total de segundos a partir de uma data especifica unix, é necessário muito cuidado nas conversões

Um padrão é:

$data = date('d/m/Y H:i:s');
desse modo retorna a data e horario atual, assim:
25/12/2024 23:59:59

para converter uma string em tempo, para fins de calculo de tempo, utilizamos o strtotime($data) 
isso retorna o tempo em segundos dessa data, então fazemos um:
strtotime(date(Y-m-d H:i:s)) ou date('c') que é o formato padrão

então, a diferença entre a subtração dessas datas, é a diferença em segundos, exemplo:

[function contarTempoPreciso (string $data){

    $agora = strtotime(date('Y-m-d H:i:s'));

    $tempo = strtotime($data);

    $diferença = $agora - $tempo;

  

    $segundos = $diferença;

    $minutos = round($diferença / 60);

    $horas = round($diferença / 3600);

    $dias = round($diferença / 86400);

    $semanas = round($diferença / 604800);

    $meses = round($diferença / 2419200);

    $anos = round($diferença / 29030400);

  

    return("$anos anos, $meses meses, $semanas semanas, $dias dias, $horas horas, $minutos minutos, e $segundos segundos");

}]
