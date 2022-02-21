<h1> Instalação do PlatformIo para Linux </h1>
---

## Instalação PlatformIo 
Abrir vscode e tecle "ctrl+shift+x" e digite `platformio` e baixe o PlatformIo IDE

## Instalação de "Linux development tools"
executar os seguintes comandos:

        sudo apt-get update
        sudo apt-get install build-essential tar curl zip unzip
## UInstalação de "vcpkg"
execute os seguintes comandos:

        cd /tmp/
        git clone https://github.com/microsoft/vcpkg
        cd vcpkg/
        ./bootstrap-vcpkg.sh


Remoção e atualização basta seguir a [documentação](https://docs.microsoft.com/en-us/cpp/build/install-vcpkg?view=msvc-160&tabs=linux) oficial.