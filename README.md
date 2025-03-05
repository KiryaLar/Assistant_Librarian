# 📚 CRUD-приложение "Библиотека"

## 📝 Описание
Приложение представляет собой веб-сервис для управления библиотечным фондом. Позволяет **добавлять, редактировать, удалять книги и пользователей**, а также **привязывать книги к конкретным читателям**.

## 🚀 Стек технологий
- **Java 17**
- **Spring MVC**
- **JDBC**
- **Thymeleaf** (шаблонизатор)
- **PostgreSQL**
- **Tomcat** (встроенный сервер)
- **Maven** (сборщик проекта)

## 🔧 Установка и запуск

### 1. Клонирование репозитория
```sh
git clone https://github.com/your-username/library-crud-spring.git
cd library-crud-spring
```

### 2. Настройка базы данных
- Убедитесь, что у вас установлена **PostgreSQL**
- Измените `src/main/resources/database.properties.origin` на свои настройки подключения.
- Создайте таблицы с помощью скрипта `src/main/resources/sql/schema.sql`.

### 3. Сборка и запуск проекта
```sh
mvn clean install
mvn spring-boot:run
```

После запуска приложение будет доступно по адресу:
```
http://localhost:8080
```

## 📌 Основные эндпоинты
### 📚 Управление книгами (`/books`)
| Метод  | URL               | Описание                          |
|--------|------------------|----------------------------------|
| GET    | `/books`         | Просмотр списка книг            |
| GET    | `/books/{id}`    | Просмотр информации о книге     |
| GET    | `/books/new`     | Форма для добавления книги      |
| POST   | `/books`         | Создание новой книги            |
| GET    | `/books/{id}/edit` | Форма редактирования книги     |
| PATCH  | `/books/{id}`    | Обновление книги                |
| DELETE | `/books/{id}`    | Удаление книги                  |
| PATCH  | `/books/{id}/release` | Освобождение книги          |
| PATCH  | `/books/{id}/assign`  | Назначение владельца книги  |

### 👥 Управление пользователями (`/people`)
| Метод  | URL               | Описание                          |
|--------|------------------|----------------------------------|
| GET    | `/people`        | Просмотр списка пользователей   |
| GET    | `/people/{id}`   | Просмотр информации о человеке  |
| GET    | `/people/new`    | Форма для добавления пользователя |
| POST   | `/people`        | Добавление пользователя         |
| GET    | `/people/{id}/edit` | Форма редактирования пользователя |
| PATCH  | `/people/{id}`   | Обновление пользователя         |
| DELETE | `/people/{id}`   | Удаление пользователя           |

### 📖 Главная страница библиотеки (`/library`)
| Метод  | URL               | Описание                          |
|--------|------------------|----------------------------------|
| GET    | `/library`       | Главная страница библиотеки    |
