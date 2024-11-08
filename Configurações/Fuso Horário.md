para definir fuso horário utilizamos a função:
date_default_timezone_set(timezoneId)

existe uma lista, porém a de são paulo, é 'America/Sao_Paulo'

desse modo, para desenvolver uma aplicação no Brasil, é recomendável utilizar:

date_default_timezone_set('America/Sao_Paulo');


