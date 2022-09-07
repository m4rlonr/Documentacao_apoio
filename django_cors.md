# Como Configurar e instalar cors headers no DJango

1.  Para iniciar necessário estar dentro do ambiente virtual com o terminal aberto e instalar com o seguinte comando:

        pip install django-cors-headers

    Feita instalação é necessário alterar o arquivo `settings.py`

1.  Em `INSTALLED_APPS` adicionar a seguinte linha de comando:

        ...,
        'django.contrib.staticfiles',
        'corsheaders',
        'rest_framework',
        ...,

1.  Abaixo do `INSTALLED_APPS` adicionar a linha de código a seguir:

        CORS_ORIGIN_ALLOW_ALL = True

1.  Para finaliza é necessário adicionar os Hosts permitidos em `ALLOWED_HOSTS`, em ambiente de desenvolvimento altere da seguinte forma:

        ALLOWED_HOSTS = ['*']

1.  Os passos são esse caso haja problemas procure solução e ajusde na documentação
