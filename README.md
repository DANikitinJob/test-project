# Task Management API

REST API для управления задачами, построенное на Laravel.

## Требования

- PHP 8.0+
- Composer
- MySQL/SQLite

## Установка

1. Клонируйте репозиторий
```bash
git clone https://github.com/DANikitinJob/test-project.git
```

2. Установите зависимости
```bash
composer install
```

3. Настройте .env файл
```bash
cp .env.example .env
php artisan key:generate
```

4. Выполните миграции
```bash
php artisan migrate
```

## API Endpoints

| Метод | Endpoint | Описание |
|-------|----------|----------|
| GET | /api/tasks | Получить все задачи |
| POST | /api/tasks | Создать новую задачу |
| GET | /api/tasks/{id} | Получить задачу по ID |
| PUT | /api/tasks/{id} | Обновить задачу |
| DELETE | /api/tasks/{id} | Удалить задачу |

## Формат данных

### Создание задачи
```json
{
    "title": "Название задачи",
    "description": "Описание задачи",
    "status": "pending"
}
```

### Статусы задач
- pending
- in_progress
- done
