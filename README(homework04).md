
Задание 1. Установка RabbitMQ
Используя Vagrant или VirtualBox, создайте виртуальную машину и установите RabbitMQ. Добавьте management plug-in и зайдите в веб-интерфейс.

Итогом выполнения домашнего задания будет приложенный скриншот веб-интерфейса RabbitMQ.

Решение:
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/51b6e771-1f32-4c6b-a371-3aec3659ff6c)


Задание 2. Отправка и получение сообщений
Используя приложенные скрипты, проведите тестовую отправку и получение сообщения. Для отправки сообщений необходимо запустить скрипт producer.py.

Для работы скриптов вам необходимо установить Python версии 3 и библиотеку Pika. Также в скриптах нужно указать IP-адрес машины, на которой запущен RabbitMQ, заменив localhost на нужный IP.

Решение:
после запуска скрипта producer.py
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/eb4cdcc7-8761-49c0-9e6d-7b4c711f8bc9)

![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/3ac305db-11fd-49d9-bfc9-c89da9c2aeec)

после запуска скрипта consumer.py
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/cb5fe263-0c88-4345-b81f-fd279e4cc478)


![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/e0fbffc9-693b-4b44-b1c5-1d6074f914da)

после подключения подключения второго консьюмера


Задание 3. Подготовка HA кластера
Используя Vagrant или VirtualBox, создайте вторую виртуальную машину и установите RabbitMQ. Добавьте в файл hosts название и IP-адрес каждой машины, чтобы машины могли видеть друг друга по имени.

Пример содержимого hosts файла:

$ cat /etc/hosts
192.168.0.10 rmq01
192.168.0.11 rmq02
После этого ваши машины могут пинговаться по имени.

Затем объедините две машины в кластер и создайте политику ha-all на все очереди.

В качестве решения домашнего задания приложите скриншоты из веб-интерфейса с информацией о доступных нодах в кластере и включённой политикой.

Также приложите вывод команды с двух нод:

$ rabbitmqctl cluster_status
Для закрепления материала снова запустите скрипт producer.py и приложите скриншот выполнения команды на каждой из нод:

$ rabbitmqadmin get queue='hello'
После чего попробуйте отключить одну из нод, желательно ту, к которой подключались из скрипта, затем поправьте параметры подключения в скрипте consumer.py на вторую ноду и запустите его.

Приложите скриншот результата работы второго скрипта.

фото rabbitmqctl cluster_status с первой ноды
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/00d8d221-4eee-4460-9a10-897629b1da21)


фото rabbitmqctl cluster_status со второй ноды
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/44c10845-d3ee-4531-945a-95a5242b2392)


результат работы скрипта
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/a3e9540f-5cbb-469c-9cdb-bbf43fd3494e)




