# airflow_etl
ETL скрипт на Python, который обращается к API worldweatheronline (https://www.worldweatheronline.com/) и получает данные о погоде, обрабатывает, и записывает в PostgreSQL.

## Запуск

    docker-compose -f docker-compose-CeleryExecutor.yml up -d

Занести API key http://0.0.0.0:8080/admin/variable/ (KEY_API_WWO)
Создать соединение http://0.0.0.0:8080/admin/connection/ (Conn Id: database_PG; Port: 5432; кредиты в database.env; а также сверить host контейнера postgres командой ниже)
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' *container_name_or_id*
