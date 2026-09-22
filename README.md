# Hexlet Chat

Realtime SPA-мессенджер на React.

[Демо проекта](https://frontend-project-12-backend.onrender.com)

## О проекте

Одностраничное приложение для обмена сообщениями в реальном времени.

Пользователь может зарегистрироваться, авторизоваться, создавать и удалять каналы, переименовывать их и обмениваться сообщениями с другими пользователями.

## Возможности

* регистрация и авторизация;
* защищённые маршруты;
* восстановление авторизации;
* создание, переименование и удаление каналов;
* отправка сообщений;
* realtime-обновление сообщений и каналов через WebSocket;
* валидация пользовательского ввода;
* обработка ошибок API;
* пользовательские уведомления;
* интернационализация интерфейса;
* Error Boundary и мониторинг ошибок через Sentry.

## Технологии

* JavaScript ES6+
* React
* Redux Toolkit
* React Router
* Axios
* Socket.IO
* Formik
* Yup
* Bootstrap
* Mantine
* i18next
* Vite
* GitHub Actions

## Архитектура

Состояние приложения разделено на несколько Redux slices:

* `auth` — авторизация пользователя;
* `channels` — каналы и активный канал;
* `messages` — сообщения;
* `socket` — состояние WebSocket-соединения;
* `modal` — состояние модальных окон.

Для коллекций каналов и сообщений используется Redux Toolkit `createEntityAdapter`.

Работа с realtime-событиями вынесена в отдельный `useSocket` hook.

## Запуск

```bash
git clone https://github.com/TheKr1d/frontend-project-12.git
cd frontend-project-12
make install
make develop
```

## Демо

[Открыть приложение](https://frontend-project-12-backend.onrender.com)
