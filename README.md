# Установка дополнительного ПО
1. Открыть файл "hosts" и прописать IP-адрес сервера, и, если нужно, имя пользователя и путь к private-ключу. Если private-ключа нет, то обратиться к главному системному администратору или руководителю проекта.
2. В файле "install-template-service.yml" в переменной docker_image прописать нужный docker-образ, а также раскомментировать нижнюю строку, если нужно активировать автозагрузку сервиса.
3. Перейти по пути "roles/robertdebock.gitlab_runner/defaults" и открыть файл "mail.yml". Ввести нужные данные для регистрации и запуска GitLab-раннера. Если что-то непонятно, то переходим по [ссылке](https://github.com/robertdebock/ansible-role-gitlab_runner/) и изучаем инструкцию.
4. Проверяем "main.yml". В переменной "gitlab_runner_executor" должен быть указан "shell".
5. Запустить "install-needed-software.yml" с ключом "-b".

P.S.: если не хватает ПО, то нужно запустить данный [playbook](https://github.com/h4ck3r1121/infrastructure-for-testing/blob/infra/install-needed-software.yml)