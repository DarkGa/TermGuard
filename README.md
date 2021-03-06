# TermGuard

![Image alt](https://github.com/DarkGa/TermGuard/raw/master/image.png)

## Установка антивируса

> поддерживается только aarch64 архитектура!

1. Обновление пакетов

`apt update; apt upgrade`

2. Установка зависимостей

`apt install git wget -y`

3. Копирование репозитория

`git clone https://github.com/DarkGa/TermGuard.git`

4. Установка антивируса

`cd TermGuard; bash install.sh`

## Мини гайд по использованию

#### Для получения справки
`tguard -h`

#### Для Обновления база данных вредоносного кода
`tguard -u`

#### Для получения информации об утилиты
`tguard -i`

#### Для сканирования файла
`tguard -f file.sh`

> Не пытайтесь проверять бинарники/картинки/видео и т.д., антивирус проверяет только исходный код (пока)


## Дополнения базы данных вредоносным кодом

База данных находится по пути `~/../usr/etc/TermGuard/database.json`, она содержит следующую архитектуру:

```json
{

  "список угроз":
     ["первая угроза", "вторая угроза"],
     
  "первая угроза":
     ["первый вредоносный код", "второй вредоносный код"]

}
```

Чтобы добавить свою угрозу нужно:

1. Добавить название угрозы в ScanList
2. Добавить угрозу и написать вредоносный код для нее

> При следующих сканированиях антивирус будет учитывать и вашу угрозу.

> При обновлении базы данных ваши изменения не сохраняются!

> Чтобы мы добавили ваши угрозы официально в базу данных присылайте ваши угрозы нам в чат (https://t.me/TermGuard_chat) с тегом #new_danger
