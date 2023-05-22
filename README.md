### Установка Node.js и npm в Ubuntu 20.04
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-ru

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
