## Fake REST API

### №1 GET /api/v1/Activities

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-30T06:16:22.8795491+00:00",
    "completed": false
  }
```
### №2 POST /api/v1/Activities

HTTP-метод: POST

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"dueDate\":\"2023-06-30T05:23:43.155Z\",\"completed\":true}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-30T05:23:43.155Z",
  "completed": true
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-30T05:23:43.155Z",
  "completed": true
}
```
### №3 GET /api/v1/Activities/{11}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/11

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
  "id": 11,
  "title": "Activity 11",
  "dueDate": "2023-06-30T16:42:16.2211624+00:00",
  "completed": false
}
```
### №4 GET /api/v1/Activities/{163}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/163

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 404

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-57ffb23e9c0c02439aa6036efea60374-d61f80687c962a43-00"
}
```
### №5 PUT /api/v1/Activities/{1}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/1

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"dueDate\":\"2023-06-30T15:36:43.477Z\",\"completed\":true}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-30T15:36:43.477Z",
  "completed": true
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-30T15:36:43.477Z",
  "completed": true
}
```
### №6 PUT /api/v1/Activities/{9999991234}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/9999991234

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"dueDate\":\"2023-06-30T15:36:43.477Z\",\"completed\":true}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-30T15:36:43.477Z",
  "completed": true
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-7836256abf13184f8d0b1970430ffa03-4401ea6ac176cc40-00",
  "errors": {
    "id": [
      "The value '9999991234' is not valid."
    ]
  }
}
```
### №7 DELETE /api/v1/Activities/{1}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа: Отсутствует

### №8 DELETE /api/v1/Activities/{9999912356}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/9999912356

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-e56e4e833c830b42aba68eea8d84bcc4-c79ac8927d5f7442-00",
  "errors": {
    "id": [
      "The value '9999912356' is not valid."
    ]
  }
}
```

### №9 GET /api/v1/Authors

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  }
```

### №10 POST /api/v1/Authors

HTTP-метод: POST

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"firstName\":\"string\",\"lastName\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### №11 GET /api/v1/Authors/authors/books/{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  }
```

### №12 GET /api/v1/Authors/authors/books/{9999901783}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/9999901783

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-f3895c118004f446a885efaf7492a13b-79a86ffc80b2c143-00",
  "errors": {
    "idBook": [
      "The value '9999901783' is not valid."
    ]
  }
}
```

### №13 GET /api/v1/Authors/{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}
```

### №14 GET /api/v1/Authors/{9999999}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/9999999

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 404

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-d3ac77764232fd4c8772ae9f4eec8d45-0160fbb6b367154b-00"
}
```

### №15 PUT /api/v1/Authors/{1}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"firstName\":\"string\",\"lastName\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### №16 PUT /api/v1/Authors/{9999999217}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/9999999217

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"firstName\":\"string\",\"lastName\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-8f14b3488851304ba8d399492004048f-77dbaaea33677645-00",
  "errors": {
    "id": [
      "The value '9999999217' is not valid."
    ]
  }
}
```

### №17 DELETE /api/v1/Authors/{1}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа: Отсутствует

### №18 DELETE /api/v1/Authors/{9999999213}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/9999999213

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-687f20e248f8c24e85376e1cfa3141bd-44ad22b730d62f41-00",
  "errors": {
    "id": [
      "The value '9999999213' is not valid."
    ]
  }
}
```

### №19 GET /api/v1/Books

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-29T15:52:48.0933352+00:00"
  }
```

### №20 POST /api/v1/Books

HTTP-метод: POST

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"description\":\"string\",\"pageCount\":0,\"excerpt\":\"string\",\"publishDate\":\"2023-06-30T15:53:37.923Z\"}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-30T15:53:37.923Z"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-30T15:53:37.923Z"
}
```

### №21 GET /api/v1/Books{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/1

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
  "id": 1,
  "title": "Book 1",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 100,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-29T15:54:54.0000118+00:00"
}
```

### №22 GET /api/v1/Books{999}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/999

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 404

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-8d3f28ab21057e4c83bee57d1adc1048-fc762da7a550604e-00"
}
```

### №23 PUT /api/v1/Books{1}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/1

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"description\":\"string\",\"pageCount\":0,\"excerpt\":\"string\",\"publishDate\":\"2023-06-30T15:57:37.965Z\"}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-30T15:57:37.965Z"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-30T15:57:37.965Z"
}
```

### №24 PUT /api/v1/Books{9999651305}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/9999651305

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"title\":\"string\",\"description\":\"string\",\"pageCount\":0,\"excerpt\":\"string\",\"publishDate\":\"2023-06-30T15:57:37.965Z\"}"

Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-30T15:57:37.965Z"
}
```
Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-21231b6d7c4db14fad0bc810be26d7ee-ac0810a78ae5dc4f-00",
  "errors": {
    "id": [
      "The value '9999651305' is not valid."
    ]
  }
}
```

### №25 DELETE /api/v1/Books{1}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа: Отсутствует

### №26 DELETE /api/v1/Books{9999975490}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/9999975490

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2c653ea88deb7b488877c4a870192a04-e976ea17c424f94a-00",
  "errors": {
    "id": [
      "The value '9999975490' is not valid."
    ]
  }
}
```

### №27 GET /api/v1/CoverPhotos

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
```

### №28 POST /api/v1/CoverPhotos

HTTP-метод: POST

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"url\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
### №29 GET /api/v1/CoverPhotos/books/covers/{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
```
### №30 GET /api/v1/CoverPhotos/books/covers/{99999236576}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/99999236576

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-1585f565443a9f4799842eb440c3a7a5-4b143dddc480e049-00",
  "errors": {
    "idBook": [
      "The value '99999236576' is not valid."
    ]
  }
}
```
### №31 GET /api/v1/CoverPhotos/{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
### №32 GET /api/v1/CoverPhotos/{999}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/999

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 404

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-df1ce0d5efeec243b8d7003336bda56b-78ff438f9041f24b-00"
}
```
### №33 PUT /api/v1/CoverPhotos/{1}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"url\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
### №34 PUT /api/v1/CoverPhotos/{9992399125}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/9992399125

Заголовки запроса: "accept: text/plain; v=1.0", "Content-Type: application/json; v=1.0", "{\"id\":0,\"idBook\":0,\"url\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-313937f6a337ee42a92413f7e3cba491-d8ba4acd44b9e544-00",
  "errors": {
    "id": [
      "The value '9992399125' is not valid."
    ]
  }
}
```
### №35 DELETE /api/v1/CoverPhotos/{1}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа: Отсутствует

### №36 DELETE /api/v1/CoverPhotos/{9999865231}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/9999865231

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-424ba16517333a4baf37ad0b133735ff-53ffec1046b2f84b-00",
  "errors": {
    "id": [
      "The value '9999865231' is not valid."
    ]
  }
}
```
### №37 GET /api/v1/Users

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users

Заголовки запроса: "accept: text/plain; v=1.0"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  }
```
### №38 POST /api/v1/Users

HTTP-метод: POST

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"userName\":\"string\",\"password\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
### №39 GET /api/v1/Users/{1}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа:
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```
### №40 GET /api/v1/Users/{99}

HTTP-метод: GET

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/99

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 404

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-0478e76b07c2a547bf71e4407d60d28c-11394336d927bc4c-00"
}
```
### №41 PUT /api/v1/Users/{1}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/1

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"userName\":\"string\",\"password\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 200

Тело ответа:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
### №42 PUT /api/v1/Users/{9987574321}

HTTP-метод: PUT

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/9987574321

Заголовки запроса: "accept: */*", "Content-Type: application/json; v=1.0", "{\"id\":0,\"userName\":\"string\",\"password\":\"string\"}"

Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-8ae881e777ae194e8c314e9a7e578034-5fe65babb7590848-00",
  "errors": {
    "id": [
      "The value '9987574321' is not valid."
    ]
  }
}
```
### №43 DELETE /api/v1/Users/{1}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/1

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 200

Тело ответа: Отсутствует

### №44 DELETE /api/v1/Users/{9988432609}

HTTP-метод: DELETE

Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/9988432609

Заголовки запроса: "accept: */*"

Тело запроса: Отсутствует

Статус-код ответа: 400

Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-d757e93204109b4dad332326b607b12e-6e41af434de49344-00",
  "errors": {
    "id": [
      "The value '9988432609' is not valid."
    ]
  }
}
```
