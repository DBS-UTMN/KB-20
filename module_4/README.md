# Модуль 4

## Задания
###### Изоляция транзакций (параллелизм) и блокировки
Используя таблицу с высоко дискретными данными (данные положения судов), создать и описать ситуации воспроизводящие следующие проблемы сериализации транзакций:
- Проблема грязного чтения
- Проблема фантомного чтения
- Проблема потерянного обновления
- Пробелма невоспроизводимого чтения
- Посмотреть и вывести в отчет различные результаты выполнения следующего SQL при обновлении,удалении, вставки без фиксации транзакций (не нажат Commit):
```sql
select
  lock.locktype,
  lock.relation::regclass,
  lock.mode,
  lock.transactionid as tid,
  lock.virtualtransaction as vtid,
  lock.pid,
  lock.granted
from pg_catalog.pg_locks lock
  left join pg_catalog.pg_database db
    on db.oid = lock.database
where (db.datname = 'ships' or db.datname is null)
  and not lock.pid = pg_backend_pid()
order by lock.pid;
```

###### Репликация
- Настроить репликацию данных для 1-2 таблиц из любой прошлой ЛР через триггеры и postgres_fdw (реализация через вставку в таблицу на удаленном сервере) (PULL или PUSH)
- Настроить репликацию через пересылку WAL на удаленный сервер (publisher/subscriber реализация) 

