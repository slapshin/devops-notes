# Docker Compose

## Запуск

```bash
# запуск всех сервисов из docker-compose файла и ожидание их выполнения. Очень удобно таким образом запускать сервисы на локальной машине: всегда контролируешь момент остановки.
docker-compose up

# запуск всех сервисов из docker-compose файла без ожидания их выполнения. Удобно, когда нужно на сервере запустить весь стэк сервисов приложения: "запустил и забыл"
docker-compose up -d

# запуск конкретного сервиса из docker-compose файла
docker-compose up <service name>
docker-compose up -d <service name>

docker-compose -p 
```

### что еще почитать

- <https://docs.docker.com/engine/reference/commandline/compose_up/> - официальная документация

## Отладка

```bash
docker-compose config
```
