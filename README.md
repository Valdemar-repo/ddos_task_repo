# ddos_task_repo

1. перейдите в каталог со скачаным репозиторием
2. замените в inventory.yml ip адреса на свои, где mariadb-откуда собираются метрики; observability-машина, на которой будут запускаться dashboards
3. в templates/prometheus.yml.j2 укажите в строках 5 и 10 тот же адрес, что и на mariadb в п.2 (сделать через gather_facts)
4. запустите плейбук ansible-playbook -i inventory.yml playbook.yml --diff


не доделан dashboard для mariadb, не внесен ip в templates/prometheus.yml.j2 через gather_facts
если при повторной накатке таска "Ensure exporter user exists with correct privileges" вызывает ошибку, закомментируйте её и пропустите (допилить идемпотентность)

паста
