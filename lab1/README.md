# Лабораторная работа 1

## Ход работы

### Шаг 1. Создание файлов с конфигурациями

Создаем файлы `docker-compose.yml` и файл `promtail_config.yml` с конфигом для сервиса `promtail`.

![docker-compose.yml](images/Screenshot_1.png)
![promtail_config.yml](images/Screenshot_2.png)

### Шаг 2. Запускаем `docker-compose` и поднимаем сервисы

Используем для этого команду: `docker compose up -d`
![Запуск сервисов](images/Screenshot_0.png)

### Шаг 3. Инициализация Nextcloud

Добавляем юзера в веб-интерфейсе
![Nextcloud](images/Screenshot_3.png)

И смотрим появились ли логи в файле `/var/www/html/data/nextcloud.log`
![Nextcloud logs](images/Screenshot_4.png)

### Шаг 4. Проверка promtail

Проверяем подцепил ли `promtail` лог файл из предыдущего пункта
![Promtail logs](images/Screenshot_5.png)

### Шаг 5. Настройка Zabbix

1. Подключаем темплейт для мониторинга Nextcloud

2. Разрешаем обращение по домену `nextcloud` в контейнере Nextcloud'а при помощи команды: `php occ config:system:set trusted_domains 1 --value="nextcloud"`

![Allow nextcloud domain](images/Screenshot_6.png)

3. Создаем Host с добавленным шаблоном для пинга сервиса Nextcloud
![Add nextcloud host](images/Screenshot_7.png)

4. Видим, что в разделе "Monitoring" появился статус `healthy/unhealthy` для сервиса Nextcloud

![Nextcloud healthiness](images/Screenshot_8.png)

### Шаг 6. Настройка Grafana
1. Устанавливаем плагин Zabbix
![Nextcloud healthiness](images/Screenshot_9.png)

2. Разрешаем плагин Zabbix

3. Добавляем Data source - Loki
![Nextcloud healthiness](images/Screenshot_10.png)

4. Добавляем Data source - Zabbix
![Nextcloud healthiness](images/Screenshot_11.png)
   
5. Создаем дашборд, состоящий из списка логов и таблички, меняющей цвет в зависимости от того, 'здоров' ли сервис Nextcloud

![Nextcloud healthiness](images/Screenshot_12.png)
