# Лабораторная работа 2

## Ход работы

### Работа по гайду

#### Часть 1

1. Создаем директорию для работы
![Screenshot](images/Screenshot_0.png)

2. Проверяем что сервер с Ansible подключился к “клиенту”
![Screenshot](images/Screenshot_1.png)

3. Попробуем создать файл через модуль shell Ansible.
![Screenshot](images/Screenshot_2.png)
#### Часть 2
1. Инициализируем исходное конфигурационное “дерево”
![Screenshot](images/Screenshot_3.png)
![Screenshot](images/Screenshot_4.png)
2. Создадим файл конфигурации плейбука
![Screenshot](images/Screenshot_5.png)
3. Заполним файл `roles/caddy_deploy/tasks/main.yml`
![Screenshot](images/Screenshot_9.png)
4. Проверим работает ли плейбук
![Screenshot](images/Screenshot_7.png)
#### Часть 3
1. Купили домен и привязали к IP-адресу сервера
![Screenshot](images/Screenshot_20.png)
2. Создадим файлы `Caddyfile.j2` и `vars/main.yml`
![Screenshot](images/Screenshot_8.png)
3. Проверим работу плейбука
![Screenshot](images/Screenshot_10.png)
![Screenshot](images/Screenshot_11.png)

### Задание
1. Создадим плейбук для создания, изменения и удаления тестового файла.
![Screenshot](images/Screenshot_12.png)

2. Проверим его работу
![Screenshot](images/Screenshot_13.png)

3. Настроим Caddyfile для передачи кастомного хедера и `index.html` файла из нужной нам директории
![Screenshot](images/Screenshot_18.png)
4. Добавим `index.html` в директорию `/var/www/lab2`
![Screenshot](images/Screenshot_16.png)
   
5. Проверим отдается ли теперь кастомный хедер
![Screenshot](images/Screenshot_14.png)

6. Проверим что страница-заглушка Caddy пропала
![Screenshot](images/Screenshot_19.png)
   