## Баг-репорты

### Баг №1 - GET​/api​/v1​/Activities несоответствие между кодом HTTP и телом ответа

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел Activities

2. Шаги воспроизведения
- отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/Activities
- проверить код состояния ответа
- проверить тело ответа

3. Фактичестий результат
- Код состояния 200
- Тело ответа содержит:
```
{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-07-13T12:56:00.4987757+00:00",
    "completed": false
  }
  ```

4.	Ожидаемый результат
- при коде состоянии 200 в конце тела ответа должно быть значение "true"

5.	Статус
- Critical

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)

### Баг №2 - PUT​/api​/v1​/Authors некорректный статус ответа

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел Authors

2. Шаги воспроизведения
- в поле для ввода id ввести значение "-7"
- отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- проверить код состояния ответа

3. Фактичестий результат
- код ответа 200 Ok
4.	Ожидаемый результат
- код ответа 400 Bad Request

5.	Статус
- Critical

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)

### Баг №3 - GET​/api​/v1​/Books​/{id} невозможность отправки запроса

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел Books

2. Шаги воспроизведения
- ввести в поле для ввода "id" значение null
- отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/Books/
- проверить код состояния ответа

3. Фактичестий результат
- невозможность отправки запроса
4.	Ожидаемый результат
- код ответа 400 Bad Request

5.	Статус
- Minor

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)

### Баг №4 - PUT​/api​/v1​/CoverPhotos​/{id} значение id из "поля ввода id" не отображается в теле ответа

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел CoverPhotos

2. Шаги воспроизведения
- ввести в поле для ввода "id" значение 7
- отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Users/7
- проверить тело ответа

3. Фактичестий результат
- в теле ответа не отображается введенное ранее значение id
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
4.	Ожидаемый результат
- совпадение введенного значения в поле для ввода id со значением в теле ответа
```
{
  "id": 7,
  "userName": "string",
  "password": "string"
}
```

5.	Статус
- Critical

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)

### Баг №4 - PUT​/api​/v1​/CoverPhotos​/{id} значение id из "поля ввода id" не отображается в теле ответа

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел CoverPhotos

2. Шаги воспроизведения
- ввести в поле для ввода "id" значение 7
- отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Users/7
- проверить тело ответа

3. Фактичестий результат
- в теле ответа не отображается введенное ранее значение id
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
4.	Ожидаемый результат
- совпадение введенного значения в поле для ввода id со значением в теле ответа
```
{
  "id": 7,
  "userName": "string",
  "password": "string"
}
```

5.	Статус
- Critical

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)

### Баг №5 - PUT​/api​/v1​/Users некорректный статус ответа

1. Предшедствующие условия
- открыть страницу https://fakerestapi.azurewebsites.net/index.html
- Открыть раздел Users

2. Шаги воспроизведения
- в поле для ввода id ввести значение "-7"
- отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- проверить код состояния ответа

3. Фактичестий результат
- код ответа 200 Ok
4.	Ожидаемый результат
- код ответа 400 Bad Request

5.	Статус
- Critical

6.	Окружение
- браузер Google Chrome, Версия 109.0.5414.120 (Официальная сборка), (64 бит)