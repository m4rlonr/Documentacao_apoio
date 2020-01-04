# Instalando Banco de dados Mysql

### Para instalar o Banco de dados Mysql no Linux

1. Execute o seguinte comando pois ele instalara o mysql- serve, mysql-client e o SGBD WorkBench.

        sudo apt install mysql-server mysql-client mysql-workbench

2. Após concluida toda a instalação execute os comandos:

        sudo mysql -u root -p

    comando usado para abrir via terminal o msql como root, no próximo comando é importanto te no local "Sua_Senha" você a informe antes de executar o comando para que o banco registre sua senha.

        ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '<Sua_Senha>'; flush privileges;

3. Agoras bastas sair do console do msql e o resetar usando os comasndos:

        exit
    e logo apoś

       sudo service mysql restart

### Pronto agora é correr para o abraço e usar o seu Banco de Dados


##### Bonus
1. Para criar um novo usuario entre novamente no console do Mysql e execute o seguinte comando trocando o "nome" e "password" pela que você desejar

        create user <nome>@'localhost' identified by 'password';