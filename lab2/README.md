# Лабораторная работа 2

## Ход работы

### Работа по гайду

#### Часть 1

1. Создаем директорию для работы <br>
![Screenshot](images/Screenshot_0.png)

2. Проверяем что сервер с Ansible подключился к “клиенту” <br>
![Screenshot](images/Screenshot_1.png)

3. Попробуем создать файл через модуль shell Ansible. <br>
![Screenshot](images/Screenshot_2.png)
#### Часть 2
1. Инициализируем исходное конфигурационное “дерево” <br>
![Screenshot](images/Screenshot_3.png)
![Screenshot](images/Screenshot_4.png)
2. Создадим файл конфигурации плейбука <br>
![Screenshot](images/Screenshot_5.png) <br>
3. Заполним файл `roles/caddy_deploy/tasks/main.yml`
![Screenshot](images/Screenshot_9.png) <br>
4. Проверим работает ли плейбук
![Screenshot](images/Screenshot_7.png) <br>
#### Часть 3
1. Купили домен и привязали к IP-адресу сервера <br>
![Screenshot](images/Screenshot_20.png)
2. Создадим файлы `Caddyfile.j2` и `vars/main.yml` <br>
![Screenshot](images/Screenshot_8.png)
3. Проверим работу плейбука <br>
![Screenshot](images/Screenshot_10.png)
![Screenshot](images/Screenshot_11.png)

### Задание
1. Создадим плейбук для создания, изменения и удаления тестового файла. <br>
![Screenshot](images/Screenshot_12.png)

2. Проверим его работу <br>
![Screenshot](images/Screenshot_13.png)

3. Настроим Caddyfile для передачи кастомного хедера и `index.html` файла из нужной нам директории <br>
![Screenshot](images/Screenshot_18.png)
4. Добавим `index.html` в директорию `/var/www/lab2` <br>
![Screenshot](images/Screenshot_16.png)
   
5. Проверим отдается ли теперь кастомный хедер <br>
![Screenshot](images/Screenshot_14.png)

6. Проверим что страница-заглушка Caddy пропала <br>
![Screenshot](images/Screenshot_19.png)
   