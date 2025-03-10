# 🚀 AuthorizationApp

AuthorizationApp - это Spring Boot приложение, реализующее систему аутентификации и авторизации пользователей с использованием Spring Security, Hibernate и встроенной базы данных H2.

## 🔥 Возможности
- 🔑 Аутентификация пользователей и ролевая авторизация.
- 🔒 Шифрование паролей с использованием BCrypt.
- 🗄 H2 in-memory база данных для удобного тестирования.
- 📌 Предзаполненные пользователи и роли для быстрого старта.
- 🛠 Кастомные `UserDetails` и `UserDetailsService`.

## 🛠 Используемые технологии
- ☕ Java 17
- 🌱 Spring Boot
- 🔐 Spring Security
- 🏛 Hibernate (JPA)
- 🗃 H2 Database
- 🔑 BCrypt Password Encoding

## ⚡ Установка и запуск

### ✅ Предварительные требования
Перед началом убедитесь, что у вас установлены:
- Java 17 или новее
- Maven

### 🚀 Шаги для запуска
1. Клонируйте репозиторий:
   ```sh
   git clone https://github.com/ult1mq/JavaSecurityAuth.git
   cd JavaSecurityAuth
   ```
2. Соберите проект:
   ```sh
   mvn clean install
   ```
3. Запустите приложение:
   ```sh
   mvn spring-boot:run
   ```
4. Доступ к приложению:
   - Сервер работает на порту `8080`
   - Консоль H2: `http://localhost:8080/h2-console`
     (JDBC URL: `jdbc:h2:mem:testdb`, логин: `sa`, пароль: `password`)

## 👤 Предустановленные пользователи
| 👤 Логин | 🔑 Пароль | 🏷 Роль |
|---------|---------|------|
| admin   | admin   | ROLE_ADMIN |
| user    | user    | ROLE_USER  |

## 🌐 API Эндпоинты
| 🔗 Эндпоинт      | 🔄 Метод | 🔐 Доступ |
|---------------|--------|--------|
| `/`           | GET    | Публичный |
| `/login`      | POST   | Публичный |
| `/logout`     | GET    | Публичный |
| `/h2-console` | GET    | Публичный |
| Другие защищенные маршруты | - | Требуется аутентификация |

## 📁 Структура проекта
- `AuthorizationApp.java` - Точка входа в Spring Boot приложение.
- `SecurityConfig.java` - Конфигурация Spring Security.
- `CustomUserDetails.java` - Реализация `UserDetails` для аутентификации.
- `CustomUserDetailsService.java` - Загрузка пользователей из базы данных.
- `User.java` & `Role.java` - Классы сущностей пользователей и ролей.
- `UserRepository.java` & `RoleRepository.java` - Репозитории Spring Data JPA.
- `DataInitializer.java` - Инициализация пользователей и ролей.
- `application.properties` - Конфигурация базы данных и сервера.

## 📜 Лицензия
Проект распространяется под лицензией MIT

