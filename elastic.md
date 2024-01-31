Задача 1
В этом задании вы потренируетесь в:

установке Elasticsearch,
первоначальном конфигурировании Elasticsearch,
запуске Elasticsearch в Docker.
Используя Docker-образ centos:7 как базовый и документацию по установке и запуску Elastcisearch:

составьте Dockerfile-манифест для Elasticsearch,
соберите Docker-образ и сделайте push в ваш docker.io-репозиторий,
запустите контейнер из получившегося образа и выполните запрос пути / c хост-машины.
Требования к elasticsearch.yml:

данные path должны сохраняться в /var/lib,
имя ноды должно быть netology_test.
В ответе приведите:

текст Dockerfile-манифеста,
ссылку на образ в репозитории dockerhub,
ответ Elasticsearch на запрос пути / в json-виде.
Подсказки:

возможно, вам понадобится установка пакета perl-Digest-SHA для корректной работы пакета shasum,
при сетевых проблемах внимательно изучите кластерные и сетевые настройки в elasticsearch.yml,
при некоторых проблемах вам поможет Docker-директива ulimit,
Elasticsearch в логах обычно описывает проблему и пути её решения.
Далее мы будем работать с этим экземпляром Elasticsearch.

Решение:

Dockerfile-манифеста
<img width="629" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/564937fe-4da1-4dbf-b2ca-debbce364283">

пуш в DockerHub
<img width="680" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/5a7ed715-ae85-462f-90c6-9121c397d198">

ссылка на репозиторий DockerHub
https://hub.docker.com/repository/docker/franky12111990/hub/general

ответ Elasticsearch на запрос пути / в json-виде
<img width="770" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/ea7fb216-24ed-4b8a-a87b-9a6f71172a33">



Решение:
<img width="937" alt="image" src="https://github.com/Franky12111990/sdb-homeworks/assets/121640886/c04ec09d-d07d-4f5d-ad0a-5f51ff582eef">


индексы "ind-2" и "ind-3" находятся в состоянии "yellow", потому что для шардов существует заданное количество реплик, но эти реплики не могут быть созданы.


Задача 3
В этом задании вы научитесь:

создавать бэкапы данных,
восстанавливать индексы из бэкапов.
Создайте директорию {путь до корневой директории с Elasticsearch в образе}/snapshots.

Используя API, зарегистрируйте эту директорию как snapshot repository c именем netology_backup.

Приведите в ответе запрос API и результат вызова API для создания репозитория.

Создайте индекс test с 0 реплик и 1 шардом и приведите в ответе список индексов.

Создайте snapshot состояния кластера Elasticsearch.

Приведите в ответе список файлов в директории со snapshot.

Удалите индекс test и создайте индекс test-2. Приведите в ответе список индексов.

Восстановите состояние кластера Elasticsearch из snapshot, созданного ранее.

Приведите в ответе запрос к API восстановления и итоговый список индексов.

Подсказки:

возможно, вам понадобится доработать elasticsearch.yml в части директивы path.repo и перезапустить Elasticsearch.


Решение:



