# Como usar o GitHub basico

### Passos

1. Primeiro é necessario instalar o Git, para isso basta abrir o terminal e executar o seguinte comando:

        sudo apt install git

2. Agora clone o repositório onde estão os dados que deseja usando o comando:

        git clone <endereço_HTTP>

    o endereço HTTP pode ser consultado no seu repositório do GitHub indo no botão de clonar repositório e selecionando a opção "use HTTP"

3. Crie os arquivos desejados dentro da pasta que clonou para que depois possa dar o push tranquilamente

4. Agora para subir o arquivo abra um terminal dentro da pasta clonada ou navegue até ela e digite o camando:

        git status

5. Para informar que ira adicionar o arquivo remotamente:

        git remote -v 

6. Feito isso como você estara dentro da pasta execute o comando:

        git add .

    O ponto indica que você que enviar os arquivos da pasta loval, ou seja, ali é local onde indica o caminho do arquivo que deseja dar o push

7. Após execute o comando:

        git commit -m "comentario do comite"

8. Após ter digitado o comentário do commit é hora de mandar para seu repositório os arquivos e para isso bastas executar o comando:

        git push -u origin master

    caso queira mandar o arquivos de forçadamente digite:

        git push -u origin master --force`

9.  Para finalizar infome seu usuario e senha do GitHub para que eja feita a autenticação e seja feliz!