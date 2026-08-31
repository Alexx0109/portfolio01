# API Testing

## Инструменты
- Postman
- JSON
- HTTP
- GitHub

## Проверенные методы:

API User details bu email: Получение сведений об учетной записи пользователя по электронной почте.

URL API: https://automationexercise.com/api/getUserDetailByEmail

Метод запроса: GET

Параметры запроса: email

Код ответа: 200

JSON-ответ: Подробная информация о пользователе в postman

API Verify login - missing email: POST-запрос для подтверждения входа без параметра email.

URL API: https://automationexercise.com/api/verifyLogin
Метод запроса: POST

Параметр запроса: пароль

Код ответа: 400

Сообщение об ошибке: Неверный запрос, в POST-запросе отсутствует параметр email или password.


API Verify login - invalid credentials : POST-запрос для проверки входа в систему с неверными данными.

URL API: https://automationexercise.com/api/verifyLogin

Метод запроса: POST

Параметры запроса: email, password (недопустимые значения)

Код ответа: 404

Ответное сообщение: Пользователь не найден!


