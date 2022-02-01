Automate your WordPress development workflow.
# INSTALL 
git clone https://github.com/petrgru/wordpress-docker

cd wordpress-docker

cp env.config .env

nano .env #change what is need password!!!!!!!!

# INSTALL WORDPRESS BY CLI
docker-compose run --rm wpcli wp core install --url=your_domain --title=Your_Blog_Title --admin_user=username --admin_password=password --admin_email=your_email.com

# BACKUP WORDPRESS BY CLI
docker-compose exec -it [db] mysqldump -u [user] -p[password] [database] > [file.sql]

# BACKUP FILE SYSTEM
tar cvfz wordpress.tar.gz build/wordpress

# RESTORE FILE SYSTEM
tar xvfz wordpress.tar.gz -C build/wordpress
