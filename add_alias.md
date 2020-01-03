# Adicionar alias Linux 

1. Para adicionar alias é necessário que abra o termonal e execute o comando: `sudo nano /home/<user>/.bashrc`
1. Navegue até o final do arquivo aberto e acione seu alias: `alias <name_alias>='<command you want alias to execute>'`
1. Salve o arquivo com o comando: `Ctrl + o` e para sair `Ctrl + x`

1. Exemplo de alias pronto:
```
alias startall='sudo apt update && sudo apt upgrade && sudo apt install -f && sudo apt autoremove && sudo apt autoclean && sudo apt install -f && sudo snap refresh'
```