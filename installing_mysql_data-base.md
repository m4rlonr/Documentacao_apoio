# Installing Data-Base 

to perform database installation.

Installing mysql-server
`sudo apt install mysql-server`

Installing securete of data-base
`sudo mysql_secure_installation`
  ->answers the questions
  ->save your password
  
  Change file
  `sudo xed /etc/mysql/mysql.conf.d/mysqld.cnf`
    ->search for `bind-address`
    ->change `bind-address		= 127.0.0.0` for `bind-address		= 0.0.0.0`
    ->restart service `sudo service mysql restart`
 
 Installing SGBD mysql-workbench
`sudo apt install mysql-workbench`

After installing
`sudo mysql -u root`
with mysql open
`SET GLOBAL validate_password_policy=LOW;`
`SET GLOBAL validate_password_special_char_count = 0;`
`SET GLOBAL validate_password_length  = 5;`
`SET GLOBAL validate_password_mixed_case_count = 0;`

To verify change changes
`show global variables like 'validate_password%';`

To finish setup
`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '<12345mR>';`

############################################################################################
Create new user
`create user <name>@'localhost' identified by 'password';`
