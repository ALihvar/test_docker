Создайте и отметьте образ Docker:
$ docker build -t sample:dev .
Затем разверните контейнер после завершения сборки:
$ docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3001:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    sample:dev
    
    
 Через docker-compose.yml
 
 Создайте образ и запустите контейнер:
$ docker-compose up -d --build

Перед тем как продолжить, опустите контейнер:
$ docker-compose stop
