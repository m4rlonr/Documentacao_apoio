# Verificando processos em aberto maquina linux

### Verificando e encerrando processos

Há vezes que a maquina apresenta certa lentidão e por isso é legal saber verificar se isso pode estarsendo causado por algum outro programa que esteja sendo executado na maquina

1.  Comando para listar os processos:

        sudo systemctl list-unit-files --type service --all

1.  Listando serviços usando filtros  
    Serviços ativos:

        sudo sudo systemctl list-unit-files --type service --all | egrep enabled

    Serviços desativados:

        sudo sudo systemctl list-unit-files --type service --all | egrep disabled

    Verificar status do serviço:

        sudo systemctl status <nome_serviço>

    Patando o serviço:

        sudo systemctl stop <nome_serviço>

1.  Desativando e ativando serviço  
    Para ativar usamos o comando:

        sudo systemctl enabled <nome_serviço>

    Para desativar usamos o comando:

        sudo systemctl disable <nome_serviço>
