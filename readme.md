# Tweet Validator

Twitter Tweet Validator

### Recommended software
- Ubuntu 16.04
- PHP 7.2
- MySQL
- composer
- nodejs and npm

### First Installation
1. Clone repository
2. copy `.env.example` to `.env`
3. Create a new MySQL database and add detail to .env file
4. Make sure that bootstrap/cache and storage directories are writable
5. Run `npm run fresh` 
6. Run `npm run dev` or Run `npm run prod`
7. *[optional]* Create Apache virtual host based on `/server_config/apache-virtualhost.conf`

### Virtual Host
- For example domain `tweetvalidator.dev` follow below steps:
```
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/tweetvalidator.dev.conf
sudo nano /etc/apache2/sites-available/tweetvalidator.dev.conf
```
- Add below code in `tweetvalidator.dev.conf`
```
<VirtualHost *:80>
    ServerAdmin admin@tweetvalidator.com
    ServerName tweetvalidator.dev
    ServerAlias www.tweetvalidator.dev
    DocumentRoot /var/www/html/tweetvalidator/public
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
- Run command to enable site `sudo a2ensite tweetvalidator.dev.conf`
- Run command to disable default sites `sudo a2dissite 000-default.conf`

- Add host in hosts file `sudo nano /etc/hosts`

```
127.0.1.1   tweetvalidator.dev
127.0.1.1   www.tweetvalidator.dev
```

### Authors
- codesapient | codesapient@gmail.com | @codesapient
- rajr.royal | rajr.royal@gmail.com | @rajr.royal

**CodeSapient** 2019
