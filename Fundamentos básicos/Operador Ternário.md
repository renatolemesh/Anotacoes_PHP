{variavel} ? {true} : {false}
primeiro a váriavel, se o conteúdo for "true" acontece o que tem após o interrogação, se for falso, o que tem depois dos ":" 

Nesse caso se o $valor existir, ele continua igual, se não existir, vai ficar 0
 ($valor ? $valor : 0)

no caso do if normal, ficaria assim:


if($valor) {
	$valor = $valor
} else {
	$valor = 0
}

nesse caso, é possível reduzir mais ainda, e tirar os parenteses, ficando assim:

$valor ?: 0
