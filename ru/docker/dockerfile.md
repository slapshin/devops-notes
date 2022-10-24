# Dockerfile best practices

Другие полезные ресурсы:

- <https://docs.docker.com/develop/develop-images/dockerfile_best-practices/>
- <https://sysdig.com/blog/dockerfile-best-practices/>
- <https://habr.com/ru/company/domclick/blog/546922/>

## 1. Использование [hadolint](https://github.com/hadolint/hadolint) для проверки

Отличный способ проверить Dockerfile на соответствие лучшим практикам. Много раз выручал.

```bash
# обычный запуск
hadolint <Dockerfile>
# запуск через docker
docker run --rm -i hadolint/hadolint < Dockerfile
```

## 2. Обязательное использование не-root пользователя в контейнере

В dockerfile создаем и указываем не-root пользователя, чтобы во время работы контейнера предоставить минимально необходимый набор прав. Таким образом очень повышается безопасность.

```dockerfile
...
RUN groupadd --system --gid 10001 app \
    && useradd --system --uid 10001 --no-log-init -g app app
...
USER app
...
```

## 3. Максимальное использование кэширования слоев

## 4. Использование максимально детализированной версии базового образа

```dockerfile
# bad
FROM python
FROM python:latest
FROM python:3
# good
FROM python:3.9.15
```
