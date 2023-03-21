# Команды

## О Docker

```bash
# версия docker
docker version
```

### пример вывода

```bash
Client:
 Cloud integration: v1.0.29
 Version:           20.10.17
 API version:       1.41
 Go version:        go1.17.11
 Git commit:        100c701
 Built:             Mon Jun  6 23:04:45 2022
 OS/Arch:           darwin/arm64
 Context:           default
 Experimental:      true

Server: Docker Desktop 4.12.0 (85629)
 Engine:
  Version:          20.10.17 <-- версия docker
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.17.11
  Git commit:       a89b842
  Built:            Mon Jun  6 23:01:01 2022
  OS/Arch:          linux/arm64
  Experimental:     false
 containerd:
  Version:          1.6.8
  GitCommit:        9cd3357b7fd7218e4aec3eae239db1f68a5a6ec6
 runc:
  Version:          1.1.4
  GitCommit:        v1.1.4-0-g5fd4c4d
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

## Список контейнеров

```bash
# вывести все запущеные контейнеры
docker ps
# вывести все запущеные контейнеры (в том числе остановленные)
docker ps -a
```

## Информация о контейнере

```bash
# информация о запущенном контейнере
docker inspect <container id>
```

## Логи контейнера

```bash
# вывести 100 последних строк логов
docker logs --tail 100 <container id>
# вывести 100 последних строк логов и получать обновления логов в реальном времени
docker logs --tail 100 -f <container id>
```
