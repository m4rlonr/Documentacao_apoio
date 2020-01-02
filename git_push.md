# Como usar o GitHub basico

## Passos:
1. Primeiro é necessario instalar o Git, para isso basta abrir o terminal e executar o seguinte comando: 
```
sudo apt install git
```
1. Agora clone o repositório onde estão os dados que deseja caso já haja dados usando o comando:
```
git clone <endereço_HTTP>
```
Obs.:recomendo que faça mesmo  que não haja arquivos no repositório pois assim ja ficará sincronizada a pasta e o GitHub

1. Crie os arquivos desejados dentro da pasta que clonou para que depois possa dar o push tranquilamente

1. Agora para subir o arquivo abra um terminal dentro da pasta clonada ou navegue até ela e digite o camando:
```
git status
```

1. Para informar que ira adicionar o arquivo remotamente:
```
git remote -v 
```

1. Feito isso como você estara dentro da pasta execute o comando:
```
git add .
```
Obs.: O ponto "." indica que você que enviar os arquivos da pasta loval, ou seja, ali é local onde indica o caminho do arquivo que deseja dar o push

1. Após execute o comando:
```
git commit -m "<Comentario do comite>"
```

1. Apenas para verificar se os arquivos que deseja dar o push está correto digite 
```
git status
``` 
novamente e verifique se está como desejado e após digite o comando:
```
git push -u origin master
```
Caso queira mandar o arquivos de forçadamente digite:
```
git push -u origin master --force

``` 

1. Para finalizar infome seu usuario e senha do GitHub para que eja feita a autenticação e seja feliz!