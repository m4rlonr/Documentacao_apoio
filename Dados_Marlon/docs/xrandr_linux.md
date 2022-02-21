<h1> Configurando resolução de segunda tela linux</h1>
---

## Script para forçar a resolução de um monitor no Linux

1. Abra o terminal e digite o comando:

        cvt <Sua_Resolução> 60  

1. Você recebera uma resolução como essa:

    ><Sua_Resolução> 51.40 Hz (CVT) hsync: 3.91 kHz; pclk: 7.00 MHz  
    Modeline "<Sua_Resolução>_60.00"    7.00  1440 1480 1616 1792  60 63 73 76 -hsync +vsync

1. Agora para o proximo comando copie tudo após o "Modeline" e execute o comando:

        xrandr --newmode <tudo_depois_do_modeline>

    Exemplo:

        xrandr --newmode "<Sua_Resolução>_60.00"  106.50  1440 1528 1672 1904  900 903 909 934 -hsync +vsync

1. Execute o addmode e na porta desejada podendo ser a VGA, HDMI ou DP:

        xrandr --addmode <porta> <Sua_Resolução>_60.00

1. O ultimo comando para instalar a configuração de saida de video:

        xrandr --output <porta> --mode <Sua_Resolução>_60.00
---

## Exemplo de script pronto

        #/bin/bash
        cvt 1440 900 60
        xrandr --newmode "1440x900_60.00"  106.50  1440 1528 1672 1904  900 903 909 934 -hsync +vsync
        xrandr --addmode DP-1 1440x900_60.00
        xrandr --output DP-1 --mode 1440x900_60.00

Observação:  para que quando você reinicie seu computador e tenha que refazer todos esse passo crie um arquivo e coloque o nome do mesmo com extensão ".sh" e vá nas configurações de inicialização automatica do linux e adicione esse arquivo para que sempre que seu computador inicie o script rode e sua resolução seja ajustado.
