# Installing Data-Base 

## To perform database installation.

## 1. Installing mysql-server
```
sudo apt install mysql-server
```

## 2. Installing mysql-client
```
sudo apt install mysql-client
```

## 3. Intalling mysql-workbench
```
sudo apt install mysql-workbench
```

## 5. after installation run the following commands on the terminal
```
sudo mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '<YourPassword>'; flush privileges;
```

## 6. right after execute the command
```
exit
sudo service mysql restart
```

# Go to the workbench press to access the database, enter your password and be happy!

## Create new user
```
create user <name>@'localhost' identified by 'password';
```
