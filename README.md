На первом сервере: запуск базовый `docker-compose up -d`     достаточно



Важное примечание где the second server - это все файлы на другом сервере  
``` Запускаем через докер также на 2 сервере 
docker run -d --name=filebeat \
  --user=root \
  --volume=/home/user1/filebeat/filebeat.yml:/usr/share/filebeat/filebeat.yml:ro \
  --volume=/var/log/nginx:/var/log/nginx:ro \
  --network=elk-network \
  elastic/filebeat:8.14.3 \
  -e -strict.perms=false
```
