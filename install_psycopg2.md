# Instalação do psycopg2
A instalação do psycopg3 depende de outras packages e por esse motivo quando tentamos fazer a instalação do mesmo acaba havendo varios logs de problemas de instalação.

Para resolver isso antes de instala-lo é necessário executar os seguintes programas de instalação:

    sudo apt install libpq-dev python3-dev build-essential
  essas são as dependencias do psycopg2 e após as tela instalado é possível instalar o psycopg2 sem mais problemas com o comando:


    pip install psycopg2
