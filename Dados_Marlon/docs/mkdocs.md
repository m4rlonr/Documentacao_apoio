# Usando MkDocs 

### Fazendo seu site com MkDocs

Referencias:
- [Download pip e definir python como padrão.](https://stackoverflow.com/questions/54633657/how-to-install-pip-for-python-3-7-on-ubuntu-18)
- [Download MkDocs, custumização e criação do site .](https://www.mkdocs.org/#mkdocs)

1. Intalando e configurando python e instalndo pip:  
   Para conseguir fazer seu site precisamos do Python e do pip e para isso basta executarmos o comando:

        sudo apt install python3.7
    Adicione o python3.7 como o padrão, com o terminal aberto digite:

        sudo nano ~/.bashrc
    No final do arquivo cole o seguinte código:

        alias python='python3.7'
    Então agora para instalar o pip execute o comando;

        python3.7 -m pip install pip
2. Iniciando ambiente virtual, instalando mkdocs:  
   Com o python e o pip instalado vamos fazer o site com nossos MarkDown do GitHub, para isso é necessario abrir o terminal e navegar até o diretório que clonou do GitHut [(Veja como fazer)](https://github.com/M4rlon-R0drigues/documentacao_diversa/blob/master/git_push.md), já estando dentro do diretório execute o comando:

        pipenv shell
    Esse comando criará um ambiente virtual e dentro dele vamos instalar o MkDocs com o comando:

        pip install mkdocs
    Terminada instalação do MkDocs vamos iniciar um projeto usando o comando:

        mkdocs new <nome_do_projeto>
    Nesse momento o MkDocs criou um diretório e precisamo acessar esse diretório usando o comando:

        cd <nome_do_projeto>/
    Dentro dessa pasta haverá uma pasta com o nome "docs" e um arquivo com nome "mkdocs.yml", a pasta docs é a pasta onde deve ficar todos os seus arquivos de MarkDown, que se tornaram as paginas do seu site, então cole todos seus arquivos dentro da pasta docs.

   Explicações breves:
   - Dentro da pasta "docs" exite também um arquivo chamado 'index.md' esse arquivo será a página inicial do site então o configure como quiser para que tenha uma aparecia legal.

   - O arquivo "mkdocs.yml" é o arquivo de configuração do MkDocs, nele ficara todo código de configuração do seu site, no final deixarei um exemplo pronto de código de configuração pronto.

3. Iniciando servido mkdocs:  
   Com todos os seus arquivos MarkDowns colados na pasta "docs" e com o arquivo "mkdocs.yml" configurado podemos subir o servidor para ver se esta tudo como desejado com o comando:

        mkdocs serve
    Para fechar o servidor bastas ir até o termianl e apertar as teclas: **Ctrl + C**
4. Construindo seu site:  
   Após encerrar o servido para construir seu site digite o comando:

        mkdocs build
    Após a contrução do seu site agora falta o deploy para ele subir hehe
5. Fazendo o Deploy:  
   O Deploy é feito com um comando simples e ele é o responsável de deixar seu site publico, para isso basta usar o comando:

        mkdocs gh-deploy
    Informe seu usuario do GitHub e sua senha e logo após o termino so processo você recebero o link do seu site e pronto só compartilhar com seus amigos!

---
Modelo pronto das configurações do arquivo "mkdocs.yml"

+ Antes é necessário que com o terminal aberto ja dentro do ambiente virtual você instale o tema 'material' com o comando:

        pipenv install mkdocs-material
+ Agora vá até a pasta do seu projeto e abra com editor de texto de seu gosto e cole as configurações abaixo:

        site_name: <nome do_seu_site>
        theme:
        name: 'material'
        palette:
            primary: 'teal'
            accent: 'blue'
        font:
            text: 'Ubuntu'
            code: 'Ubuntu Mono'
        logo:
            icon: 'nome_icone'
        language: 'pt'
        extra:
        search:
            language: 'en, pt'
        feature:
            tabs: true
    [Veja aqui nome dos icones.](https://material.io/resources/icons/?style=baseline)

### Tudo pronto agora é compartilhar seu site com seus amigos e ser feliz!