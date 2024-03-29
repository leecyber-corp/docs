# Политика тестирования SQL инъекций

Тестирование уязвимостей, которые могут приводить к внедрению команд SQL, должно выполняться в соответствии с данной политикой.

Во время тестирования запрещены любые действия на сервере кроме:

* Получения данных о текущей БД (SELECT `database()`), ее версии (SELECT `@@version`), текущего пользователя (SELECT `user()`, SELECT `system_user()`) или имени хоста (SELECT `@@hostname`).
* Получения схемы БД (SELECT `table_schema`), списка таблиц в ней (SELECT `table_name`) и имен столбцов в таблицах (SELECT `column_name`).
* Выполнения математических, конверсионных или логических запросов (включая использование SLEEP) без извлечения данных (кроме тех, что перечислены выше).

При необходимости проведения иных действий необходимо предварительно согласовать их с командой безопасности LeeCyber.
