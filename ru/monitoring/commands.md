# Команды

## Просмотр логов

```bash
# просмотр последних системных логов
sudo journalctl -r
# просмотр логов процесса 
sudo journalctl _PID=8088
# просмотр логов пользователя за сегодня
sudo journalctl _UID=33 --since today
```
