# ML_pipeline

Запуск: docker-compose up -d

Superset может заработать не сразу, тогда дополнительно нужно выполнить:
1. docker exec -it superset superset db upgrade
2. docker exec -it superset superset fab create-admin --username admin --firstname Admin --lastname User --email admin@superset.com --password admin
3. docker exec -it superset superset init
4. docker-compose restart superset

Теперь:
1. PostgreSQL работает на localhost:5432 (логин: admin, пароль: admin, БД: oil_and_gas_db)
2. MinIO работает на localhost:9001 (логин/пароль: minioadmin)
3. Jupyter работает на localhost:8888 (токен: admin123). Jupyter-ноутбук с выполненным заданием лежит в директории notebooks
4. Superset работает на localhost:8088 (логин/пароль: admin/admin)

Построенные дашборды расположены в директории dashboards