## Практика 1. Развертывание и работа с IDS Snort

Выполниил студент группы ББМО-01-23 Бакин.Д.И.

# 1. Установка docker, docker-compose
```
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
$(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

![Снимок1](https://github.com/xoz0r/CMuYUUB/assets/145142526/de53ab6d-cffb-4131-9677-6d2b351f62da)

![Снимок2](https://github.com/xoz0r/CMuYUUB/assets/145142526/8727896d-e09e-43d9-9004-f17251a9cba0)

![Снимок3](https://github.com/xoz0r/CMuYUUB/assets/145142526/842f92b3-5867-4148-9bcf-d626aa44c43b)

Запускаем тестовый докер-контейнер для того чтобы убедиться, что докер установлен

```
sudo docker run hello-world
```

![Снимок4](https://github.com/xoz0r/CMuYUUB/assets/145142526/055e9fe3-cc07-474e-ac6a-6db47841b267)

```
DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
mkdir -p $DOCKER_CONFIG/cli-plugins
curl -SL https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
```

```
chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
```

![Снимок5](https://github.com/xoz0r/CMuYUUB/assets/145142526/9bd1e4ed-04a3-4f07-af04-c5c153a323a8)

Проверяем следующей командой, что мы установили docker compose

```
docker compose version
```

![Снимок6](https://github.com/xoz0r/CMuYUUB/assets/145142526/ce38d04e-4957-4edc-a569-582f72c1b483)

# 2. Установка образов с IDS Snort и DB Barnyard 2

```
sudo git clone https://github.com/fabriziogaliano/docker-snort-ids
```

![Снимок7](https://github.com/xoz0r/CMuYUUB/assets/145142526/72f90d3a-1f1d-4f82-8c24-725ad862413b)

# 3. Установка Snorby для работы через web-интерфейс

```
sudo docker pull polinux/snorby
```

![Снимок8](https://github.com/xoz0r/CMuYUUB/assets/145142526/51a30ded-b1ee-4c8f-a984-ed953a1ced6c)

Получение oink-кода

![Снимок9](https://github.com/xoz0r/CMuYUUB/assets/145142526/103731eb-b517-4be4-843f-051609c61e5d)


# 4. Запуск полученных образов в контейнерах

Запускаем с повышенными правами

```
sudo docker-compose up
```

![Снимок10](https://github.com/xoz0r/CMuYUUB/assets/145142526/fb6a05eb-8e64-4ca2-a11b-520b1ce2716a)

![Снимок11](https://github.com/xoz0r/CMuYUUB/assets/145142526/0d683500-e75f-4dd3-90e2-b8e06d86a4f9)

![Снимок12](https://github.com/xoz0r/CMuYUUB/assets/145142526/c3878b1b-2628-4beb-a05d-ad3f5a65aced)

# 5. Создать произвольное правило для Snort

Данное правило будет детектировать отправку любых icmp пакетов, как пример - ping

![Снимок13](https://github.com/xoz0r/CMuYUUB/assets/145142526/f583e882-1979-48aa-ba73-e44ee98fd7a6)

# 6. Запустить в Snort сниффер пакетов с выводом статистики в консоль или web-интерфейс

Создание активности путём отправки icmp-пакетов ping с разных ВМ

![Снимок14](https://github.com/xoz0r/CMuYUUB/assets/145142526/d849c4b0-eabd-4dbc-9637-e836ae2d27eb)

Просматриваем логи отправки ICMP запросов

![65d9166cbad42_1708725966_65d9166cbad37](https://github.com/xoz0r/CMuYUUB/assets/145142526/3e931ae5-7114-4662-8eb9-580c7ead6ed9)








