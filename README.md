# «Работа с Playbook» - Дрибноход Давид

## Подготовка к выполнению

1. * Необязательно. Изучите, что такое [ClickHouse](https://www.youtube.com/watch?v=fjTNS2zkeBs) и [Vector](https://www.youtube.com/watch?v=CgEhyffisLY).
2. Создайте свой публичный репозиторий на GitHub с произвольным именем или используйте старый.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.
4. Подготовьте хосты в соответствии с группами из предподготовленного playbook.

## Основная часть

1. Подготовьте свой inventory-файл `prod.yml`.
2. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает [vector](https://vector.dev). Конфигурация vector должна деплоиться через template файл jinja2. От вас не требуется использовать все возможности шаблонизатора, просто вставьте стандартный конфиг в template файл. Информация по шаблонам по [ссылке](https://www.dmosk.ru/instruktions.php?object=ansible-nginx-install). не забудьте сделать handler на перезапуск vector в случае изменения конфигурации!
3. При создании tasks рекомендую использовать модули: `get_url`, `template`, `unarchive`, `file`.
4. Tasks должны: скачать дистрибутив нужной версии, выполнить распаковку в выбранную директорию, установить vector.
5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть.
6. Попробуйте запустить playbook на этом окружении с флагом `--check`.
7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.
8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.
9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги. Пример качественной документации ansible playbook по [ссылке](https://github.com/opensearch-project/ansible-playbook). Так же приложите скриншоты выполнения заданий №5-8
10. Готовый playbook выложите в свой репозиторий, поставьте тег `08-ansible-02-playbook` на фиксирующий коммит, в ответ предоставьте ссылку на него.

## Решение

1.

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/5a181f6d-09af-4f80-8d9d-66b2a9c97227)

2. 

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/cbb24d2e-f552-40e3-b9bd-f1b4e5fc7c77)

3. Использовал `get_url`, `template`
4.   

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/ddd6ea7a-d344-4081-b6fb-4528888a77d7)

5. До исправления

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/e2eb9b4f-a307-4b60-95a6-c668aeffbf96)

После исправления

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/ab1bf237-0fc0-48c6-af06-4a7170467202)

6.

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/4320007c-d28c-4dad-a098-4b8042ef819e)

7.

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/85a5dca9-b649-485b-9256-f4935e1f3699)

8. playbook идемпотентен

![image](https://github.com/DrDavidN/ans08_02hw/assets/128225763/0d94b686-3790-49e7-89cb-d52a85cada09)

9. 
