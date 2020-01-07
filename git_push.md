# Como usar o GitHub basico

### Passos

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

- Opção 2 - fornecendo senha:  
   Antes de fazer o push de um repositório execute o comando:

        git config credential.helper store

  Faça todo procedimento normal de PUSH e após verifique o arquivo `~/.git-credentials` que é o arquio que guarda as credenciais, lembrete não é recomendado pois os arquivos guardados não são criptografados.

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

Referências:  
[Alterando arquivo '.gitconfig'](https://fellipe.com/blog/definindo-configuracoes-do-gitconfig-apos-a-instalacao-do-git/)  
[Opção salvando senha](https://stackoverflow.com/questions/35942754/how-to-save-username-and-password-in-git)  
[Documentação credencial store](https://git-scm.com/docs/git-credential-store)
