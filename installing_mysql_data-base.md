# Installing Data-Base 

to perform database installation.

Installing mysql-server
`sudo apt install mysql-server`

Installing securete of data-base
`sudo mysql_secure_installation`
  ->answers the questions
  
  Change file
  `sudo xed /etc/mysql/mysql.conf.d/mysqld.cnf`
    ->search for `bind-address`
    ->change `bind-address		= 127.0.0.0` for `bind-address		= 0.0.0.0`
 
 Installing SGBD mysql-workbench
`sudo apt install mysql-workbench`
