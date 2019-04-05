apt-get update
apt-get -y upgrade

# install java
add-apt-repository ppa:webupd8team/java


# nginx 
wget -c -O- http://nginx.org/keys/nginx_signing.key | sudo apt-key add -
echo "deb http://nginx.org/packages/ubuntu/ trusty nginx" | sudo tee -a /etc/apt/sources.list.d/nginx.list > /dev/null

# artifactory
https://jfrog.bintray.com/artifactory-debs/

wget -c -O- "https://bintray.com/user/downloadSubjectPublicKey?username=jfrog" | sudo apt-key add -
echo "deb https://bintray.com/artifact/download/jfrog/artifactory-debs trusty main" | sudo tee -a /etc/apt/sources.list.d/artifactory-oss.list

apt-get update
# install java
apt-get -y install oracle-java8-installer
# install MySQL
apt-get -y install mysql-server-5.7
# set root password here...
# install nginx
apt-get -y install nginx

# http only:
```
    server {
        listen 80 default_server;
        listen [::]:80 default_server;
        server_name artifactory.exampleserver.xyz;
        root /usr/share/nginx/artifactory;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-Proto $scheme;
        location / {
          proxy_pass http://localhost:8081;
        }
} 

server {
    listen 80;
    server_name repo.nikl.me;
    root /usr/share/nginx/artifactory;
    rewrite ^/$ /artifactory/webapp/ redirect;
    rewrite ^/artifactory/?(/webapp)?$ /artifactory/webapp/ redirect;
    location / {
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass http://localhost:8081;
    }
}

```
service nginx restart


# artifactory 
apt-get -y install jfrog-artifactory-oss

# change time to let artifactory start in: !!! (900)
/opt/jfrog/artifactory/bin/artifactory.default

# same for /var/opt ? Also reset the home path...


# configure mySQL
/opt/jfrog/artifactory/bin/configure.mysql.sh


service artifactory start
service artifactory status
service artifactory stop/check







~.
cd /
add-apt-repository ppa:webupd8team/java
apt-get update
apt-get install oracle-java8-installer
dpkg -i jfrog-artifactory-oss-6.5.2.deb
service artifactory start
top
apt-get -y install mysql-server-5.6
apt-get -y install mysql-server-5.7
apt-get -y install nginx
service nginx status
mkdir /etc/nginx/sites-available
ls
rm jfrog-artifactory-oss-6.5.2.deb
cd etc/nginx/
ls
cd sites-available/
ls
touch artifactory.conf
nano artifactory.conf
service nginx restart
ls
rm default
service nginx restart
ln -sf /etc/nginx/sites-available/artifactory.conf /etc/nginx/sites-enabled/artifactory.conf
service nginx restart
cd /opt/jfrog/artifactory/misc/db/createdb/
ls
cd /opt/jfrog/artifactory/bin/
ls
./configure.mysql.sh
service artifactory start
cd .ssh
ls
shutdown -r 0
ufw
ufw -help
ufw list
ufw -list
ufw status
iptables -help
ls
nano .ssh/authorized_keys
service ssh restart
ls
dig 8.8.8.8
ping 8.8.8.8
ping google.com
ping localhost
apt-get install software-properties-common
add-apt-repository ppa:certbot/certbot
apt-get update
apt-get install python-certbot-nginx
certbot --nginx
exit
ls
cd ..
ls
vim /etc/nginx/conf.d/
vim /etc/nginx/nginx.conf
service nginx restart
cd /
ls
rm -r Artifactory-backup/
ls
cd /etc/nginx/sites-available/
vim artifactory.conf


