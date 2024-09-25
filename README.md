# Создание сервера для мониторинга
1. В данном репозитории находится изменный terraform-код (main.tf) из задания №1 для создания дополнительного сервера (test-vm-2). В "main.tf" нужно прописать данные от Yandex.Cloud.
2. В файле "install-needed-software.yml" находится необходимое ПО для запуска Prometheus и Grafana. Необходимо прописать в поле "targets" в таске "Install Prometheus" ip-адреса и порты node exporter-ов.
3. Открыть файл "hosts" и прописать IP-адрес сервера, и, если нужно, имя пользователя и путь к private-ключу. Если private-ключа нет, то обратиться к главному системному администратору или руководителю проекта.