# DZYABA landing

Статический лендинг (одна страница) для деплоя на Amvera через Docker (Nginx).

## Локальный просмотр

Открыть через простой сервер:

```bash
python3 -m http.server 5173
```

Потом открыть в браузере `http://localhost:5173`.

## Деплой на Amvera (через CLI)

### 1) Установить Amvera CLI

См. документацию Amvera по CLI: `https://docs.amvera.ru/general/cli.html`

### 2) Авторизация

```bash
amvera login
```

### 3) Инициализация и деплой

В корне проекта (где лежит `Dockerfile`):

```bash
amvera init
amvera push
```

Amvera соберёт Docker-образ и запустит сервис на выданном домене.
