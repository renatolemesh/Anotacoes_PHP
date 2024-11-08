O arquivo composer json, permite dar autoload de classes e constantes, sem a necessidade de ficar dando inclue, primeiro configuramos o json:

{

    "name": "cursophp8/estrutura",

    "description": "Curso de php8",

    "type": "project",

    "autoload": {

        "psr-4": {

            "Sistema\\": "Sistema/"

        },

        "files":[

            "sistema/configuracao.php"

        ]

    },

    "authors": [

        {

            "name": "Renato Lemes"

        }

    ],

    "minimum-stability": "dev",

    "require": {}

}

Dentro da pasta autoload, configuramos a pasta inicial do projeto, e em baixo, arquivos onde contem constantes que utilizaremos no projeto.

Já no arquivo index, podemos só chamar ele:

require 'vendor/autoload.php';



