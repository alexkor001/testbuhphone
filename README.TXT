Созданы 2 роли:
 roles\ngnix - установка ngnix, php-fpm и импорт конфигов
     roles\ngnix\templates\nginx.conf -основной конфиг nginx
     roles\ngnix\templates\nginx_vhosts.conf -конфиг виртуальных хостов
 roles\letsencrypt - получение сертификатов
     roles/letsencrypt/templates/nginx-http.j2 -конфиг виртуального хоста для получения сертификата
Переменные:
    Глобальные:
        nginx_user: www-data -пользователь nginx
        letsencrypt_email: alexkor001@gmail.com -почта для получения сертификата
    Определены для хостов
        test7:
            domain: test7.akhancem.uz - доменное имя 1 хоста
            ansible_port: 5555 - порт ssh первого хоста
        test8:
            domain: test8.akhancem.uz - доменое имя 2 хоста
            ansible_port: 5555 - порт ssh 2 хоста
inventory - собственно inventory-файл
playbook.yml - плэйбук для вызова ролей
