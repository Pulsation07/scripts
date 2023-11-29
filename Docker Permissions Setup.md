# Docker Permissions Setup
Enter directory with docker-compose file.

`$ docker compose up -d`

Transfer all of /wp-content/ to wp-app/wp-content

Adjust local file permissions

`$ sudo chown -R $USER:$USER /wp-app/`

Adjust wp-config.php database credentials

Navigate to http://localhost:8080 and login

Import database and change site/home URLs to https://localhost:8000

SSH into container and update permissions
```
$ chown -R www-data:www-data /var/www
$ find /var/www -type d -exec chmod 0755 {} \;
$ find /var/www -type f -exec chmod 644 {} \;
```
