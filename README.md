﻿# Лабораторные работы по БСБД для  группы KB-20

## Модули
- [Модуль 1](https://github.com/DBS-UTMN/KB-20/tree/main/module_1) - Создание структуры БД, нормализация, ограничения целостности
- [Модуль 2](https://github.com/DBS-UTMN/KB-20/tree/main/module_2) - Внешние таблицы, функции, вычесляемые столбцы, партицирование

## Полезные ссылки

- [DBeaver](https://dbeaver.io/download/) - Утилита для работы с базой данных (поддержка большинства популярных движков СУБД)!
- [Docker desktop](https://www.docker.com/products/docker-desktop/) - Утилита для запуска и управления контейнера в среде Windows
- [VS Code](https://code.visualstudio.com/Download) - IDE с поддержкой большинства современных языков программирования и наличием огромного количества расширений.

## Запуск контейнеров 
```sh
cd module_${номер_модуля}
docker compose . up -d
```
Логины и пароли будут указаны в docker-compose файле или подробнее будет указано в самом модуле.


