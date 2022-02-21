<h1> Instalando Bando de Dados PostGres</h1>
---
 
## Instalar O PostGres e DBeaver
use o comando:

         sudo apt install postgresql postgresql-contrib

## Configuraçẽos para usar o PostGres e o conectar com o SGBD

- Definir senha:

      sudo passwd postgres
- Logar no usuario PostGres:

      su postgres
   Difite sua senhas
- Execute o comando:

      sudo systemctl enable postgresql
- Execute o comando:

      psql
- Definindo a senha para conectar ao SGBD:

      \password postgres
- Execute o comando:

      \q
   Para sair do Postgres

## Agora Baixe o DBaver do [Site Oficial](https://dbeaver.io/download/)  

- Para Instalar o Dbeaver que deve estar em ".deb" abra o terminal e vá até o local do arquivo e execute o comando:

      sudo dpkg -i <nome_do_arquivo.deb>

- Para verificar se há a nessecidade de baixar mais algum pacote digite o comando:

      sudo apt install -f
- Entre no DBeaver e conecte ele ao seu postGres