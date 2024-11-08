
Para configurar rotas só com packages, sem frameworks, precisamos definir o htaccess para permitir roteamento:

Options -Indexes

RewriteEngine on
RewriteCond %{SCRIPT_FILENAME} !-f
RewriteCond %{SCRIPT_FILENAME} !-d
RewriteCond %{SCRIPT_FILENAME} !-l
RewriteRule ^(.*)$ index.php/$1

#isso é a configuração para variavel que recebe os posts.


