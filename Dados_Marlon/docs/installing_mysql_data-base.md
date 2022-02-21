<h1> Instalando Banco de dados Mysql</h1>
---

## Instalando ferramentas

Execute o seguinte comando pois ele instalara o mysql- serve, mysql-client e o SGBD WorkBench.

        sudo apt install mysql-server mysql-client mysql-workbench

## Definindo senha para usuário mysql
Após concluida toda a instalação execute os comandos:

        sudo mysql -u root -p

comando usado para abrir via terminal o msql como root, no próximo comando é importanto te no local "Sua_Senha" você a informe antes de executar o comando para que o banco registre sua senha.

        ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '<Sua_Senha>'; flush privileges;

## Preparo pra iniciar o serviço do mysql
Agoras bastas sair do console do msql e o resetar usando os comasndos:

        exit
e logo após

       sudo service mysql restart

##### Bonus
1. Para criar um novo usuario entre novamente no console do Mysql e execute o seguinte comando trocando o "nome" e "password" pela que você desejar

        create user <nome>@'localhost' identified by 'password';