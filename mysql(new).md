
Задача 1
Используя Docker, поднимите инстанс MySQL (версию 8). Данные БД сохраните в volume.

Изучите бэкап БД и восстановитесь из него.

Перейдите в управляющую консоль mysql внутри контейнера.

Используя команду \h, получите список управляющих команд.

Найдите команду для выдачи статуса БД и приведите в ответе из её вывода версию сервера БД.

Подключитесь к восстановленной БД и получите список таблиц из этой БД.

Приведите в ответе количество записей с price > 300.

В следующих заданиях мы будем продолжать работу с этим контейнером.

Решение:
версия 8.3.0
<img width="579" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/42908d3d-537d-4c5e-91be-0e17892ba2e3">

<img width="363" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/39a42086-4471-428b-b440-93acc95e2391">


Задача 2
Создайте пользователя test в БД c паролем test-pass, используя:

плагин авторизации mysql_native_password
срок истечения пароля — 180 дней
количество попыток авторизации — 3
максимальное количество запросов в час — 100
аттрибуты пользователя:
Фамилия "Pretty"
Имя "James".
Предоставьте привелегии пользователю test на операции SELECT базы test_db.

Используя таблицу INFORMATION_SCHEMA.USER_ATTRIBUTES, получите данные по пользователю test и приведите в ответе к задаче.

Решение:


<img width="909" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/0b5c4ed2-176a-460c-87d7-427add1d403d">


Задача 3
Установите профилирование SET profiling = 1. Изучите вывод профилирования команд SHOW PROFILES;.

Исследуйте, какой engine используется в таблице БД test_db и приведите в ответе.

Измените engine и приведите время выполнения и запрос на изменения из профайлера в ответе:

на MyISAM,
на InnoDB.


Решение:

<img width="557" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/accf339b-7198-4957-bd73-b2b174e07bc7">


Задача 4
Изучите файл my.cnf в директории /etc/mysql.

Измените его согласно ТЗ (движок InnoDB):

скорость IO важнее сохранности данных;
нужна компрессия таблиц для экономии места на диске;
размер буффера с незакомиченными транзакциями 1 Мб;
буффер кеширования 30% от ОЗУ;
размер файла логов операций 100 Мб.
Приведите в ответе изменённый файл my.cnf.

Решение:

<img width="584" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/c442ff82-c07d-4017-80d3-82c23c8430e6">



