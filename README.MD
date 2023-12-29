#Установка и настройка Yandex.Cloud MDB PostgreSQL Cluster с использованием Terraform

Подготовка
Установка [Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli) и подготовка спецификации для создания виртуальной машины (ВМ) и управляемой базы данных (PostgreSQL) в облаке Yandex.Cloud.

[Настройка](https://cloud.yandex.ru/docs/tutorials/infrastructure-management/terraform-quickstart#configure-provider) провайдера Yandex.Cloud в файле [my-config.tf](http://my-config.tf/), указав необходимые параметры, такие как token, cloud_id, folder_id, и zone.

Создание виртуальной машины
В файле спецификации my-config.tf добавьте блок, описывающий создание виртуальной машины. Используйте образ ВМ. Добавьте переменную image-id для идентификатора образа и файл my-variables.tfvars для хранения значений переменных.

Скорректируйте описание сети и подсети в спецификации, указав уникальные имена и IP-адреса.

Проверьте синтаксис спецификации с помощью команды terraform plan и, при необходимости, внесите корректировки.

Примените спецификацию с помощью команды terraform apply, создав в облаке виртуальную машину.

Создание кластера PostgreSQL
Расширьте спецификацию для добавления кластера базы данных PostgreSQL. Повторно проверьте синтаксис и примените обновленную спецификацию.

Проверьте, создан ли кластер PostgreSQL в Yandex.Cloud, и удостоверьтесь, что его статус - Alive.

Динамика изменения стейт-файла
Посмотрите, как изменился стейт-файл Terraform с добавлением нового объекта для кластера PostgreSQL.

Удаление инфраструктуры
Для завершения работы удалите созданную инфраструктуру с помощью команды terraform destroy. Подтвердите выполнение команды вводом "yes".