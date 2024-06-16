# Access_Apache_Parser_Log

<!--Установка-->
## Установка
1. Клонирование репозитория:
```git clone https://github.com/NoxAu/Access_Apache_Parser_Log.git```

2. Переход в каталог проекта:
```cd Access_Apache_Parser_Log```

3. Устанавливаем зависимости:
```pip install -r requirements.txt```

4. Настраиваем конфигурационный файл config.yml:
```app:
  # automatic aggregation of logs
  schedule_update_logs_enabled: True
  # aggregation interval in seconds
  schedule_update_logs_delay: 30
  # automatic launch of the Apache web server
  start_apache_server: True

logs:
  format: '%h %l %u %t \"%r\" %>s %b'
  # the path to the folder with logs
  path: server/Apache24/logs
  # the name of the file with access logs
  access_log: access.log```