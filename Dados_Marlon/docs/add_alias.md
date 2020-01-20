# Adicionar alias Linux 

Para adicionar alias é necessário que abra o termonal e execute o comando: 

    sudo nano /home/<user>/.bashrc

Navegue até o final do arquivo aberto e acione seu alias: 

    alias <nome_do_alias>='<comando que você deseja realizar com alias>'

Salve o arquivo com o comando: `Ctrl + o` e para sair `Ctrl + x`

Exemplo de alias pronto:

    alias startall='sudo apt update && sudo apt upgrade && sudo apt install -f && sudo apt autoremove && sudo apt autoclean && sudo apt install -f && sudo snap refresh'
