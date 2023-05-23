### Установка Node.js и npm в Ubuntu 20.04
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-ru
https://github.com/nodesource/distributions#using-ubuntu

    sudo apt update
    curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
    sudo apt-get install -y nodejs
    nodejs -v
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
