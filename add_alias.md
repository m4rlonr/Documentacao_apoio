# Add alias 

1.To add an alias, you need to open the terminal and follow these steps.
`sudo nano /home/<user>/.bashrc`

In the file that was opened at the end we can see that there are already some aliases, just below them you can add your own aliases

1.Add an alias to the file
`alias <name_alias>='<command you want alias to execute>'`

*example*
`alias startall='sudo apt update && sudo apt upgrade && sudo apt install -f && sudo apt autoremove && sudo apt autoclean && sudo apt install -f'`

1.save the file
