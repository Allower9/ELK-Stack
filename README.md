#### На первом сервере: запуск базовый `docker-compose up -d`     достаточно



####  Важное примечание где the second server - это все файлы на другом сервере  
``` Запускаем через докер также на 2 сервере 
docker run -d --name=filebeat \
  --user=root \
  --volume=/home/user1/filebeat/filebeat.yml:/usr/share/filebeat/filebeat.yml:ro \
  --volume=/var/log/nginx:/var/log/nginx:ro \
  --network=elk-network \
  elastic/filebeat:8.14.3 \
  -e -strict.perms=false
```

####  Добавлены больше как для тесты разные конфигурация
<img width="2852" height="1298" alt="image" src="https://github.com/user-attachments/assets/04039253-a48f-4042-9421-3a36354a5ae5" />


####  Также логи 
<img width="1433" height="798" alt="Снимок экрана 2025-09-22 в 14 37 17" src="https://github.com/user-attachments/assets/7f0307e2-d483-412f-a298-99bcede77ced" />

####  Проверка Dashboards
<img width="2880" height="1704" alt="image" src="https://github.com/user-attachments/assets/7a3fcd52-1a70-4de2-8366-dcbb58f47d48" />


