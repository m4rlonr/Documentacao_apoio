<h1> Verificando processos em aberto maquina linux </h1>
---

## Verificando e encerrando processos

Há vezes que a maquina apresenta certa lentidão e por isso é legal saber verificar se isso pode estarsendo causado por algum outro programa que esteja sendo executado na maquina

##  Comando para listar os processos:

    sudo systemctl list-unit-files --type service --all

##  Listando serviços usando filtros  
Serviços ativos:

    sudo sudo systemctl list-unit-files --type service --all | egrep enabled

Serviços desativados:

    sudo sudo systemctl list-unit-files --type service --all | egrep disabled

Verificar status do serviço:

    sudo systemctl status <nome_serviço>

Patando o serviço:

    sudo systemctl stop <nome_serviço>

##  Desativando e ativando serviço  
Para ativar usamos o comando:

    sudo systemctl enabled <nome_serviço>

Para desativar usamos o comando:

    sudo systemctl disable <nome_serviço>
