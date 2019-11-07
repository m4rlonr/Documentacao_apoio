#Intalling postgresql and Dbeaver SGBD
 
 # to start installing
 
 ## 1. Installing postgresql
 ```
 sudo apt install postgresql postgresql-contrib
 ```
 
 ## 2. setting up postgres
    -Define password              => `sudo passwd postgres`
    -login user postgres          => `su postgres`  ** type your password
    -run the command              => `sudo systemctl enable postgresql`
    -run the command              => `psql`
    -Set password to connect SGBD => `\password postgres`
    -run the command              => `\q` for exit  
 
 ## 3.now download dbeaver from the official site
    -to install go to the folder where the downloaded file is and run the commands
    -installing         => `sudo dpkg -i <NameFile>`
    -check dependencies => `sudo apt install -f`
    
 ## 4. go to dbeaver and connect to postgres
 
 # ready be happy
