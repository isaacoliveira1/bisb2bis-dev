# ESPECIFICAÇÕES SISTEMA

Tecnologias utilizadas<br>
Requisitos para hospedagem<br>
Restaurando o banco de dados<br>
Estrutura do projeto<br>
Arquivo de configuração<br>
Instalando o sistema no servidor Apache<br>
- 3.1 Através de arquivo zip
- 3.2 Através de repositório<br>

# Tecnologias utilizadas

PHP 7.3<br>
Symfony MVC Framework v. 4.2<br>
Banco de dados MySQL 5.7+<br>

# Requisitos para hospedagem<br>

Servidor Linux: Ubuntu ou CentOS<br>
PHP 7.3 ou 7.4<br>
Extensões do PHP necessárias<br>
Composer disponível globalmente<br>
Symfony disponível globalmente<br>
Git disponível globalmente<br>
Apache 2<br>
MySQL 5.7+<br>

# Instalando o sistema no servidor Apache<br>
## 3.1 Através de arquivo zip:<br>

Instale o zip com apt install zip<br>
No diretório /var/html/www crie uma pasta para o sistema<br>
Baixe o arquivo .Zip e extraia na pasta criada<br>
Digite o comando unzip -r arquivo.zip<br>

## 3.2 Através de repositório:<br>
Navegue até a pasta criada no diretório do Apache<br>
Rode o comando Git clone https://github.com/Inside-Places/alvara-dourados.git<br>
Após clonar o projeto, na pasta raíz do sistema, crie um arquivo .env é neste arquivo que estará configurado as variáveis de ambiente do sistema.<br>
Na raiz do projeto, rode o comando composer install para instalar todas as dependências.<br>

# Estrutura do projeto

O sistema está baseado no padrão de projeto MVC (Model View Controller) onde:<br>

A pasta Entity é responsável pelos Models, ou entidade de banco de dados<br>
A pasta Controller é responsável por armazenar os controladores e regra de negócio<br>
A pasta templates é onde estão localizadas todas as views.<br>
O arquivo .env é onde fica as variáveis de ambiente para as configurações do projeto, como: conexão com banco de dados, configurações de API’s.<br>

Para mais informações sobre a estrutura do framework Symfony, consulte a documentação oficial. <br>

# Arquivo de configuração

O sistema utiliza o arquivo de configuração .env, localizado na pasta principal do projeto. Neste arquivo existem 3 diretivas importantes:<br>

DATABASE_URL: Informação de conexão do banco de dados<br>
MAILER_URL: Informação de configuração SMTP para disparo dos e-mails de notificação.<br>
APP_ENV: Configuração de ambiente. <br>
dev: para ambiente desenvolvedor com algumas ferramentas para depuração, como profiler e debugger. Utilize essa diretiva para detectar algum erro.<br>
prod: ambiente produção, utilize essa configuração quando o sistema estiver em produção para o sistema processar as requisições de forma mais rápida e ocultar informações de debug do usuário.<br>
