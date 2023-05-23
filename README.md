### Установка Node.js и npm в Ubuntu 20.04
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-ru
https://github.com/nodesource/distributions#using-ubuntu

    sudo apt update
    curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
    sudo apt-get install -y nodejs
    node -v
    sudo apt install npm

### Установка Vue3
https://v3.ru.vuejs.org/ru/guide/installation.html#npm

    npm install vue@next

### Установка Vue CLI
https://cli.vuejs.org/ru/guide/installation.html

    npm install -g @vue/cli
    vue --version

### Создание проекта Vue
https://cli.vuejs.org/ru/guide/creating-a-project.html

    vue create vue-nginx-base-app
    vue ui
    npm i
    npm run build

### Install NGINX
https://thucnc.medium.com/deploy-a-vuejs-web-app-with-nginx-on-ubuntu-18-04-f93860219030
    
    sudo apt install nginx
    sudo touch /etc/nginx/sites-available/vue-nginx-base-app
    sudo ln -s /etc/nginx/sites-available/vue-nginx-base-app /etc/nginx/sites-enabled/vue-nginx-base-app
    sudo nano /etc/nginx/sites-available/vue-nginx-base-app

### Delete default config
https://stackoverflow.com/questions/72467210/how-to-host-a-vue-js-app-to-a-ngnix-server

    cd /etc/nginx/sites-available
    sudo rm default
    cd /etc/nginx/sites-enabled
    sudo rm default
    cd /etc/nginx
    sudo nano nginx.conf

### Start, Stop, and Restart Nginx with systemctl
https://phoenixnap.com/kb/nginx-start-stop-restart

    sudo systemctl status nginx
    sudo systemctl reload nginx
    sudo systemctl restart nginx
    sudo systemctl enable nginx

### How can I see what ports are open on my machine?
https://askubuntu.com/questions/9368/how-can-i-see-what-ports-are-open-on-my-machine

    sudo netstat -ntlp

### How to kill a process on a port on ubuntu
https://stackoverflow.com/questions/23389313/kill-all-processes-running-on-port-8080-on-mavericks

    sudo fuser -k 8080/tcp

### Ошибка 500 internal server error Nginx
https://ru.stackoverflow.com/questions/1378502/nginx-%D0%B2%D0%BE%D0%B7%D0%B2%D1%80%D0%B0%D1%89%D0%B0%D0%B5%D1%82-500-internal-server-error
nginx -t


### Ошибка 500 internal server error Nginx
https://www.digitalocean.com/community/questions/502-bad-gateway-nginx-2
https://selectel.ru/blog/tutorials/how-to-configure-firewall-with-ufw-on-ubuntu-20/


### Run service

    /bin/bash -c 'source /opt/airflow/venv/bin/activate && airflow webserver'