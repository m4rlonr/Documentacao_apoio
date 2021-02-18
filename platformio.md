# Instalação do PlatformIo para Linux

### Passos
1. Abrir vscode e tecle "ctrl+shift+x" e digite `platformio` e baixe o PlatformIo IDE
2. Instalar " Linux development tools", executar os seguintes comandos:

        sudo apt-get update
        sudo apt-get install build-essential tar curl zip unzip
1. Para instalar o "vcpkg" execute os seguintes comandos:

        cd /tmp/
        git clone https://github.com/microsoft/vcpkg
        cd vcpkg/
        ./bootstrap-vcpkg.sh


Remoção e atualização basta seguir a [documentação](https://docs.microsoft.com/en-us/cpp/build/install-vcpkg?view=msvc-160&tabs=linux) oficial.