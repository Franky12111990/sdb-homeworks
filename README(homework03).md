Задание 1. Elasticsearch
Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный.

Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name.

Решение:

![elasticsearch](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/5f7f181b-a4c3-4af2-a433-08aece97735c)

Задание 2. Kibana
Установите и запустите Kibana.

Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty.

Решение:
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/1d99b2a8-520a-418a-a5be-c715624ed05c)

Задание 3. Logstash
Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.

Ответ:
Я увлёкся и сделал сразу четвертое задание.)

Задание 4. Filebeat.
Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat
![image](https://github.com/Franky12111990/sdb-homeworks/assets/121640886/dff3cdb6-ab39-4bc6-8b0d-e47360ebe505)

