# tidy linux screen resolution

## script to force a monitor screen resolution

# 1. type the following command
```
cvt <YourResolution> 60  
```
# 2. an answer like that
```
1440x60 51.40 Hz (CVT) hsync: 3.91 kHz; pclk: 7.00 MHz
Modeline "1440x60_60.00"    7.00  1440 1480 1616 1792  60 63 73 76 -hsync +vsync
```
# 3. type the following command with and copy the end of the previous command response
```
xrandr --newmode <PreviousCommandResponse>
```
example:
```
xrandr --newmode "1440x900_60.00"  106.50  1440 1528 1672 1904  900 903 909 934 -hsync +vsync
```
# 4. after you type this command by adding the resolution to the port you want
```
xrandr --addmode <door> <YourResolution>_60.00
```
# 4. ending now making the screen output video at the desired resolution
```
xrandr --output <Door> --mode <YourResolution>_60.00
```

#################################################################################################
## full script example
```
#/bin/bash
cvt 1440 900 60
xrandr --newmode "1440x900_60.00"  106.50  1440 1528 1672 1904  900 903 909 934 -hsync +vsync
xrandr --addmode DP-1 1440x900_60.00
xrandr --output DP-1 --mode 1440x900_60.00
```

# save the script to the desired location with ".sh" format and add it to the startup applications so that when the system goes up it will come to the desired resolution
