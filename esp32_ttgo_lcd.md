<h1> Configuração e teste de ESP32 TTGO Oled </h1>
---

# Introdução
Para realizar a instalação será necessário executar alguns passo como instalação de programas, configuração de bibliotecas e de dispositivo.
Os passos de dados contidos aqui são baseados em experiencia pessoal com o desenvolvimento.

# Instalação de dependencias
Levando em consideração que o usuário que está lendo o presente documento já tenha instalado a IDE e todas as dependências necessárias para o desenvolvimento com o ESP32, neste documento será abordado apenas o uso da biblioteca `TFT_eSPI`.
## Instalação de pacotes do Python

A primeira configuração é realizada ainda em dados do sistema no caso `Linux mint` via terminal.

Comando 1

    sudo apt install python-is-python3

Comando 2

    sudo apt-get install python3-serial

## Instalação de biblioteca TFT_eSPI

O ESP32 no qual esse documento é baseado é o TTGO e a placa que o indentifica é `ttgo-lora32-v1`.
A IDE usada é PlatformIo e para fazer a instalação basta ir em "Libraries" e digitar pelo nome da biblioteca como dito no tema desse passo.

## Modificação de arquivos da Biblioteca
Para o funcionamento correto do código base funcionar é necessário alterar dados do código fonte da biblioteca e o caminho no PlatformIo é o seguinte:

    `Projeto>.pio>libdeps>TFT_eSPI>User_Setup_Select.h`
Já com o arquivo aberto na linha 22 onde está a seguinte linha de código

    #include <User_Setup.h>           // Default setup is root library folder
é necessário comenta-la, ou seja, adicionar "//" no inicio da linha.
Já na linha 53 onde está o seguinte trecho de código:

    //#include <User_Setups/Setup25_TTGO_T_Display.h>    // Setup file for ESP32 and TTGO T-Display ST7789V SPI bus TFT
Será necessário descomentar a linha, ou seja, retirar o "//" do inicio da linha.

Feito todos esses passos basta abrir um exemplo da biblioteca e o compilar para dentro da placa, podem haver casos onde será necessário dar permissão ao usuário para compilar o código para dentro do ESP32 mas o erro pode ser resolvido com o seguinte comando:

    sudo chmod 666 /dev/ttyUSB0

Comando esse que deve ser executado no terminal linux.