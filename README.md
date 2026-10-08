# Task Tracker Infrastructure

Infrastructure-репозиторий проекта Task Tracker.

Содержит Docker Compose конфигурацию для запуска всех микросервисов и необходимых инфраструктурных компонентов.

## Микросервисы

| Репозиторий                                                                           | Ответственность                                             |
| ------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [task-tracker-backend](https://github.com/eriicyaan/task-tracker-backend)             | Пользователи, авторизация и управление задачами             |
| [task-tracker-scheduler](https://github.com/eriicyaan/task-tracker-scheduler)         | Планирование и формирование ежедневных отчётов              |
| [task-tracker-email-sender](https://github.com/eriicyaan/task-tracker-email-sender)   | Отправка email через SMTP                                   |
| [task-tracker-summarization](https://github.com/eriicyaan/task-tracker-summarization-server) | Генерация отчётов по задачам с использованием LLM           |
| [task-tracker-contracts](https://github.com/eriicyaan/task-tracker-contracts)         | Общие DTO, события и контракты межсервисного взаимодействия |

## Infrastructure

Для работы приложения используются:

* PostgreSQL
* Apache Kafka

Все компоненты проекта запускаются через Docker Compose.

## Структура проекта

```text
Task Tracker
│
├── task-tracker-backend
├── task-tracker-scheduler
├── task-tracker-email-sender
├── task-tracker-summarization
├── task-tracker-contracts
└── task-tracker-infrastructure
```

## Запуск

```bash

docker compose up
```

Остановка:

```bash

docker compose down
```

## Клонирование репозитория

```bash

git clone https://github.com/eriicyaan/task-tracker-infrastructure.git
```
