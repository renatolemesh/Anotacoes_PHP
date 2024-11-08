
Loop for

```php
For($i = 1; $i <= 10; $i++) {
	echo $i;
}
```

Esse loop vai imprimir do 1 ao 10, sendo a primeira parte a variavel, a segunda a condição, e a terceira o incremento, já a parte de baixo, é o bloco de código

Usando o while:

```php
$i = 1;
while ($i <= 10) {
    echo $i;
    $i++;
}
```

também é possível colocar : e endwhile; invés de {}.

No while, podemos utilizar o do while, que faz a operação do bloco pelo menos uma vez:

```php
$i = 1;
do {
    echo $i;
    $i++;
} while ($i < 11);
```

exemplo de tabuada:

````php
for($i = 1; $i <= 10; $i++){

    for($b = 1; $b <= 10; $b++){

        echo "$i x $b = ".($i * $b).'<br>';

    }

}
```
