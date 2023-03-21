# Команды

## Копирование

```bash
# копирование файлов с сохранением прав доступа
cp -rp <src> <desc>
```

## Просмотр логов

```bash
# просмотр последних системных логов
sudo journalctl -r
# просмотр логов процесса 
sudo journalctl _PID=8088
# просмотр логов пользователя за сегодня
sudo journalctl _UID=33 --since today
# просмотр логов пользователя/сервиса...
sudo journalctl -u minidlna.service -r 
# просмотр логов за последние 2 дня 
sudo journalctl -u minidlna.service -r --since "2 days ago"
```
