## Практическая работа №2

Выполниил студент группы ББМО-01-23 Бакин.Д.И.

# 1. Установка docker, docker-compose

![Снимок1](https://github.com/xoz0r/CMuYUUB/assets/145142526/b841247c-a12d-4e81-b381-c9196f917e43)

![Снимок2](https://github.com/xoz0r/CMuYUUB/assets/145142526/f5e8bf0f-cd60-487f-9f25-2cec65138781)

![Снимок3](https://github.com/xoz0r/CMuYUUB/assets/145142526/3c96194a-21dc-4e5c-8b64-a56ab263a416)

Запускаем тестовый докер-контейнер для того чтобы убедиться, что докер установлен

![Снимок4](https://github.com/xoz0r/CMuYUUB/assets/145142526/b138fc34-d911-4862-b4ab-67ccc762bb94)

![Снимок5](https://github.com/xoz0r/CMuYUUB/assets/145142526/021dc7ca-ff43-4d42-93ee-7e8ef26dba8a)

Проверяем следующей командой, что мы установили docker compose

![Снимок6](https://github.com/xoz0r/CMuYUUB/assets/145142526/93574bc8-3cde-4dbc-a2bc-16f8c83d1b01)

# 2. Установить образы с IPS Suricata или развернуть в виртуальной машине.

Далее вся установка и настройка происходит по следующему гайду

```
https://www.digitalocean.com/community/tutorials/how-to-install-suricata-on-debian-11
```

![Снимок7](https://github.com/xoz0r/CMuYUUB/assets/145142526/8e476155-07bb-4ac0-8e4a-3e1a333a5ada)

![Снимок8](https://github.com/xoz0r/CMuYUUB/assets/145142526/84b8f160-0b7b-4b6d-a0a7-28768b00b78f)

# 3. Настроить и запустить IPS Suricata на сетевом адаптере для обработки сетевых пакетов.

![Снимок9](https://github.com/xoz0r/CMuYUUB/assets/145142526/2dbcfefb-d3e3-4eec-b745-9350187c69d4)

# 4. Обновить правила и создать произвольное правило для Suricata.

![Снимок10](https://github.com/xoz0r/CMuYUUB/assets/145142526/d46f844d-73b7-46b8-ab9f-be3f14873921)

Добавление произвольного правила происходит путём добавления правила в файл директории /etc/suricata/rules

![Снимок15](https://github.com/xoz0r/CMuYUUB/assets/145142526/d8b31aec-48e9-4935-8b56-1332c48bb998)

![Снимок11](https://github.com/xoz0r/CMuYUUB/assets/145142526/3ee43f60-e084-4f7d-983b-d1c4c13ff6b1)

Запуск Suricata

![Снимок13](https://github.com/xoz0r/CMuYUUB/assets/145142526/9ac6f76d-6775-49bf-b0be-3abc3a506908)

# 5. Смоделировать ситуацию вторжения, например путем сканирования сетевых портов сканером Nmap или
любым средством тестирования на проникновение.

![Снимок16](https://github.com/xoz0r/CMuYUUB/assets/145142526/74976c7f-9382-4e76-a5e8-1bb0e3ac17c6)
