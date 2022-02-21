<h1> Como usar o GitHub basico</h1>

## Passos

1.  Primeiro é necessario instalar o Git, para isso basta abrir o terminal e executar o seguinte comando:

        sudo apt install git

1.  Com git instalado agora precisa definir usuario e email(opcional)

- Opção 1 - Sem fornecer senha:  
   Definindo Usuario:

        git config --global user.name "nome_usuario_github"

  Definindo Email:

        git config --global user.email "email_github"

  Verificar se foi devidamento definido basta exercutarmos os comandos:

        git config user.name
        git config user.email

1.  Agora clone o repositório onde estão os dados que deseja usando o comando:

        git clone <endereço_HTTP>

    o endereço HTTP pode ser consultado no seu repositório do GitHub indo no botão de clonar repositório e selecionando a opção "use HTTP"

2.  Crie os arquivos desejados dentro da pasta que clonou para que depois possa dar o push tranquilamente

3.  Agora para subir o arquivo abra um terminal dentro da pasta clonada ou navegue até ela e digite o camando:

        git status

4.  Para informar que ira adicionar o arquivo remotamente:

        git remote -v

5.  Feito isso como você estara dentro da pasta execute o comando:

        git add .

    O ponto indica que você que enviar os arquivos da pasta loval, ou seja, ali é local onde indica o caminho do arquivo que deseja dar o push

6.  Após execute o comando:

        git commit -m "comentario do comite"

7.  Após ter digitado o comentário do commit é hora de mandar para seu repositório os arquivos e para isso bastas executar o comando:

        git push -u origin master

    caso queira mandar o arquivos de forçadamente digite:

        git push -u origin master --force`

8.  Comando úteis para usar caso necessario  
    Verificar se o diretório local esta sincronizado com dirretório do Gitub usamos o comando:

        git pull origin master

    Para remover um arquivo de diretório localmente e sincronizar usamos o comando:

        git rm -r <nome__arquivo>

    Apos é necessario fazer o mesmo processo de push para que o arquivo seja remoovido também no repositório do GitHub

9.  Para finalizar infome seu usuario e senha do GitHub para que eja feita a autenticação e seja feliz!

## Criando acesso SSH no GitHub

Para criar o acesso é necessario verificar esta instalado o `openssh-client`, ele lhe dira se esta instalado e logo após verificar se ja foram criadas chave ssh com o comando `ls -al ~/.ssh` e caso haja bastas executar o comando `cat ~/.ssh/id_rsa.pub`, copiar e colar no GitHub e depois testar a conexão, que será feito nos próximos passos!

Caso não tenha nenhuma chava é necessário criar com o seguintes passo:

1.  Abra o terminal e digite o comando

        ssh-keygen -t rsa -b 4096 -C "seu_email@example.com"

    Troque o local indicado pelo email da sua conta do GitHub e **nos próximos dois passos caso queira deixar em branco só aperte enter**

1.  Agora vamos adicionar a agenda com o comando

            eval "$(ssh-agent -s)"

    Pronto o que deveria ser feito no terminal está pronto agora devemos ir ao GitHub e executar os seguintes passos:

1.  executar o comando `cat ~/.ssh/id_rsa.pub` para vermos a chave e copiala para colar no GitHub.
1.  No canto superior direito de qualquer página, clique na foto do seu perfil e clique:

        Configurações -> SSH and GPG keys -> New SSH key ou Add SSH key

    De um titulo e abaixo cole sua chave que você copiou com o comando `cat ~/.ssh/id_rsa.pub`

1.  Confirme sua senha do GitHub e agora teste a conexão com o terminal com um simples comando:

        ssh -T git@github.com

    Esse comando lhe repondera com uma mensagem dizendo que foi um sucesso a autenticação.

## Usando SSH em seu repositório

Caso você não tenha os repositórios em sua maquina e deseja acionar em sua maquina bastas ir no seu repositório do GitHub e clicar em clonar e escolher a opção SSH e o comando para clonar deverá ficar paracido com o seguinte comando:

        git@github.com:<usuario>/<diretório>

Seguindo esses passos você poderá usar tranquilamente o ssh sem problomas!

Se já esta com o repositório em sua maquina e usou o HTTP é necessario remover o vinculo com o HTTP usando o comando:

        git remote rm origin

e então adicionar o vinculo com o SSH usando o comando:

        git remote add origin git@github.com:<usuario>/<repositório>

Assim o vinculo será feito com o SSH e você podera usar tranquilamente o ssh em um diretório ja existente em sua maquina.

Referências:  
[Alterando arquivo '.gitconfig'](https://fellipe.com/blog/definindo-configuracoes-do-gitconfig-apos-a-instalacao-do-git/)  
[Opção salvando senha](https://stackoverflow.com/questions/35942754/how-to-save-username-and-password-in-git)  
[Documentação credencial store](https://git-scm.com/docs/git-credential-store)
[Criar nova chave ssh e adicionando a agenta](https://help.github.com/pt/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)  
[Quando a primeira conexão foi feita com http](https://stackoverflow.com/questions/33880832/github-ssh-key-claiming-it-is-not-used)  
[Adicionando chave ao GitHub](https://help.github.com/pt/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
