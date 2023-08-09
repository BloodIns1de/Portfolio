# Отчёт тестирования API в Postman

## №1 Activities. Запрос GET.

1) URL: {{default_url}}/api/v1/Activities

2) Ожидаемый результат: Сервер присылает ответ со списком ID, статус-код 200

3) Заголовки запроса:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 06:43:58 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

4) Тело запроса: Отсутсвует

5) Заголовки ответа:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 06:43:58 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:


```
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-07-17T07:43:58.8412475+00:00",
        "completed": false
```

## №2 Activities. Запрос POST.

1) URL: {{default_url}}/api/v1/Activities

2) Ожидаемый результат: Сервер присылает ответ с записью id в список, статус-код 200

3) Заголовки запроса:

`Content-type: application/json`

`User-agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса:

```
    "id": 7,

 "title": "string",

 "dueDate": "2023-07-10T08:02:25.412Z",

 "completed": true
```

5) Заголовки ответа:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 07:14:19 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 7,
    "title": "string",
    "dueDate": "2023-07-10T08:02:25.412Z",
    "completed": true
```

 ## №3 Activities. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/Activities/{{activities_id}}

2) Ожидаемый результат: Сервер присылает ответ с информацией о id 7, статус-код 200

3) Заголовки запроса:

`User-agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 07:17:28 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 7,
    "title": "string",
    "dueDate": "2023-07-17T14:17:28.5691395+00:00",
    "completed": false
```

 ## №4 Activities. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/Activities/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ с информацией, о том что id 99999999999 не валидный, статус-код 400

3) Заголовки запроса:

`User-agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 07:20:45 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0271b29d50931b42b060c863c21f26a6-9fe6a4f076dffe4e-00",
    "errors": {
        "id": [
            "The value '99999999999' is not valid."
        ]
```

## №5 Activities. Запрос PUT{id}.

1) URL: {{default_url}}/api/v1/Activities/{{activities_id}}

2) Ожидаемый результат: Сервер присылает ответ с информацией о id 11, статус-код 200

3) Заголовки запроса:

`Content-type: application/json`

`User-agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса:

```
 "id": 11,

 "title": "string",

 "dueDate": "2023-07-10T08:22:40.594Z",

 "completed": true
```

5) Заголовки ответа:

`Content-type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 07:20:45 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 11,
    "title": "string",
    "dueDate": "2023-07-10T08:22:40.594Z",
    "completed": true
```

## №6 Activities. Запрос PUT{id} некорректный id.

1) URL: {{default_url}}/api/v1/Activities/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ с информацией, о том что id 99999999999 не валидный, статус-код 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 6c24f272-1717-41a6-a99a-0e026aa50167`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 117`

4) Тело запроса:

```
 "id": 11,

 "title": "string",

 "dueDate": "2023-07-10T08:22:40.594Z",

 "completed": true
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 08:37:17 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-21d2a19e1793064dbf84a034293e1ce9-6af8963169fe5246-00",
    "errors":
        "id": "The value '99999999999' is not valid."
        "$.id": "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."
```

## №7 Activities. Запрос DELETE{id}.

1) URL: {{default_url}}/api/v1/Activities/{{activities_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: cf9ea052-a7c0-43b1-99b2-98cc2c707b0a`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 08:40:42 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`


6) Тело ответа: Отсутствует

## №8 Activities. Запрос DELETE{id} некорректный id.

1) URL: {{default_url}}/api/v1/Activities/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: cf9ea052-a7c0-43b1-99b2-98cc2c707b0a`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 08:40:42 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-dc9705502040d349b4e5f8386aa81278-7d24a5b490b5344c-00",
    "errors":
        "id": "The value '99999999999' is not valid."
```

## №9 Activities. Запрос PUT{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Activities/{{activities_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 6c1d8ce6-5386-4334-bd94-29b7b1f72ee2`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 85`

4) Тело запроса:

```
 "id": 0,

 "title": "string",

 "dueDate": "2023-07-10T10:00:33.915Z",
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 08:45:25 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0cb79f4a58e9ac4ab42b1f24282e21f2-cf981bf411ba2649-00",
    "errors":
        "$": "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 8 | BytePositionInLine: 0."
```

## №10 Activities. Запрос POST{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Activities

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: de00d1e6-dbf1-4b59-a5c4-955ead0e310c`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 114`

4) Тело запроса:

```
 "id": school21,

 "title": "string",

 "dueDate": "2023-07-10T10:32:26.901Z",

 "completed": true
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 08:47:40 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-019fa5557e06164c845479369bf2e7a6-d523e21cb75c9741-00",
    "errors":
        "$.id": "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
```

## №12 CoverPhotos. Запрос GET.

1) URL: {{default_url}}/api/v1/CoverPhotos

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 3073fdb7-bd51-4d0d-8633-237d63047222`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 08:50:24 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`


6) Тело ответа:

```
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
```

## №13 CoverPhotos. Запрос POST.

1) URL: {{default_url}}/api/v1/CoverPhotos

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 381ec045-6dc5-4c5f-a569-237e7453d0b6`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 56`

4) Тело запроса:

```
 "id": 7,

 "idBook": 0,

 "url": "string"
```

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 08:52:51 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`


6) Тело ответа:

```
    "id": 7,
    "idBook": 0,
    "url": "string"
```

## №14 CoverPhotos. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/CoverPhotos/books/covers/{{coverphotos_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: ae430570-929b-4427-ac60-2b86da1b568f`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 08:56:44 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`


6) Тело ответа:

```
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
```

## №15 CoverPhotos. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/CoverPhotos/books/covers/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 24aac1a4-ef95-4896-aabd-bed6ecca81a7`

`Host: fakerestapi.azurewebsites.net`


`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 08:57:54 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f17b36f141f0bd42b7529effdce07bce-ed44ac5e2439db42-00",
    "errors": 
        "idBook": "The value '99999999999' is not valid."
```

## №16 CoverPhotos. Запрос PUT{id}.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{coverphotos_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 93ce9c34-0b5f-4724-9dcd-f68bea83bf35`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 57`

4) Тело запроса:

```
 "id": 11,

 "idBook": 0,

 "url": "string"
```

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 08:59:46 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`


6) Тело ответа:

```
    "id": 11,
    "idBook": 0,
    "url": "string"
```

## №17 CoverPhotos. Запрос PUT{id} некорректный id.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 7e417a82-b8d5-49bc-bf7d-e93786fb5c90`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 66`

4) Тело запроса:

```
 "id": 11071999163,

 "idBook": 0,

 "url": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:01:24 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-98bcae5f6f81cf4d8a3fcd88fab02450-0104f62e2d7ace42-00",
    "errors":
        "id": "The value '99999999999' is not valid."
        "$.id": "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."
```

## №18 CoverPhotos. Запрос DELETE{id}.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{coverphotos_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 360ced07-2f68-42ff-af67-a232e6a0eece`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 09:02:58 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`


6) Тело ответа: Отсутствует

## №19 CoverPhotos. Запрос DELETE{id} некорректный id.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: e6b6f07f-f380-4a29-a93d-3e2b4ba7eedf`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:04:51 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`


6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-815af8fd8cbc7a47bbbbd7c3c9f58457-30dc7478107ff44e-00",
    "errors":
        "id": "The value '99999999999' is not valid."
```

## №20 CoverPhotos. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{coverphotos_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: e51c9b93-a56b-42cd-8ff0-43edd1396f1b`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:06:26 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`


6) Тело ответа:

```
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
```

## №21 CoverPhotos. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 4bd4d186-2ae7-4b7c-b00f-94d1e77376de`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:07:52 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5db03facb24aa74d9dc2cd78defb7b2e-6a69220620f45541-00",
    "errors":
        "id": "The value '99999999999' is not valid."
```

## №22 CoverPhotos. Запрос PUT{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/CoverPhotos/{{coverphotos_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 949fbfac-a5f6-4042-ae86-6e126a32a31e`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 63`

4) Тело запроса:

```
 "id": school21,

 "idBook": 0,

 "url": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:09:24 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3ad7a771be2e2d4a916caa279268e733-514beba900c8e34a-00",
    "errors":
        "$.id": "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
```

## №23 CoverPhotos. Запрос POST{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/CoverPhotos

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: f2628cb6-05f5-41ca-b1dc-4d57eb0ebc91`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 63`

4) Тело запроса:

```
 "id": school21,

 "idBook": 0,

 "url": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:11:00 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-602148ed642a3c4ea865fdb2d77fa3ad-160a38e17b185649-00",
    "errors": 
        "$.id": "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
```

## №24 Users. Запрос GET.

1) URL: {{default_url}}/api/v1/Users

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: a248baaf-575a-43e0-994c-56f0f75b063c`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:12:47 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
```

## №25 Users. Запрос POST.

1) URL: {{default_url}}/api/v1/Users

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: f1e470a3-54f5-44b0-b8f3-38865edfef31`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 71`

4) Тело запроса:

```
 "id": 11,

 "userName": "string",

 "password": "string"
```

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:16:20 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 11,
    "userName": "string",
    "password": "string"
```

## №26 Users. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/Users/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: cbc078c3-2017-4c0d-ae3c-794289f98807`


`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:18:33 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-060ccbbcd6ee0c4e8de9b1afe20a5cbd-8617d007395fa147-00",
    "errors": 
        "id": "The value '99999999999' is not valid."
```

## №27 Users. Запрос PUT{id}.

1) URL: {{default_url}}/api/v1/Users/{{users_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 840fc97f-c323-4461-b05b-462c2fd6e7fa`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 71`

4) Тело запроса:

```
 "id": 11,

 "userName": "string",

 "password": "string"
```

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:19:35 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 11,
    "userName": "string",
    "password": "string"
```

## №28 Users. Запрос PUT{id} некорректный id.

1) URL: {{default_url}}/api/v1/Users/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: c0e4a34c-c25c-46b6-9ff6-5080d382691`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 80`

4) Тело запроса:

```
 "id": 11071999163,

 "userName": "string",

 "password": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:21:09 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ad215220000f1049a48d69d291625bd1-f2ce1fe53988324e-00",
    "errors":
        "id": "The value '99999999999' is not valid."
        "$.id": "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."
```

## №29 Users. Запрос DELETE{id}.

1) URL: {{default_url}}/api/v1/Users/{{users_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 5446adb2-ce6f-49d9-b76f-e2f2e3def8eb`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 09:22:46 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`

6) Тело ответа: Отсутствует

## №30 Users. Запрос DELETE{id} некорректный id.

1) URL: {{default_url}}/api/v1/Activities/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: f3e5234d-87bb-4b1a-9c9a-9824bfd8ea13`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:24:17 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-00a5a47fe9060c43ae1c28921385379a-ac394f786329c34c-00",
    "errors": 
        "id": "The value '99999999999' is not valid."
```

## №31 Users. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/Users/{{users_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 15604380-ef56-4e30-a3ae-2e67e25edf3f`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:25:32 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
```

## №32 Users. Запрос PUT{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Users/{{users_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 2e025b9d-664a-48ba-bac1-1f53dabbba54`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 81`

4) Тело запроса:

```
 "id": school21,

 "userName": "string",

 "password": "string"
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:27:09 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-72a86c3a3caaa54db4d0d4d1e48efb43-b2b6e5b6d9164343-00",
    "errors": 
        "$.id": "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
```

## №33 Users. Запрос POST{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Users

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 5fbbe4df-5157-4c18-b215-ef25b29774ce`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 81`

4) Тело запроса:

```
 "id": school21,

 "userName": "string",

 "password": "string"
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:29:19 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0adf25dbaf926349bd992c90e9390e55-7c5d04d8dd0ff84f-00",
    "errors": 
        "$.id": "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
```

## №34 Books. Запрос GET.

1) URL: {{default_url}}/api/v1/Books

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 15c5cfe4-6224-4728-9048-139d38828f74`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:31:39 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-07-16T09:31:39.9053005+00:00"
```

## №35 Books. Запрос POST неккоректный id тела запроса.

1) URL: {{default_url}}/api/v1/Books

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 8703eacc-972a-4eef-b0fa-7214d0dd8b38`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 163`

4) Тело запроса:

```
 "id": -1,

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",

 "publishDate": "2023-06-21T16:57:19.320Z"
```
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:33:46 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": -1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-21T16:57:19.32Z"
```

## №36 Books. Запрос POST значение null в id тела запроса.

1) URL: {{default_url}}/api/v1/Books

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: fcb2821e-1608-4af7-8882-ef9ea93f1ebc`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 165`

4) Тело запроса:

```
 "id": null,

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",

 "publishDate": "2023-07-11T14:34:14.320Z"
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 09:35:09 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8ae96fad42d11a48a703176e60e2b83c-e8ee7d886c010f43-00",
    "errors": 
        "$.id": "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
```

## №37 Books. Запрос POST.

1) URL: {{default_url}}/api/v1/Books

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: edcafb20-7e0d-46c6-bf24-1a989909b495`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 162`

4) Тело запроса:

```
 "id": 7,

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",

 "publishDate": "2023-07-11T14:34:14.320Z"
```
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:37:57 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 7,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-11T14:34:14.32Z"
```

## №38 Books. Запрос POST некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Books

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: b8c78575-7936-4387-83de-4d44856ea6aa`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 66`

4) Тело запроса:

```
 "id": 0,

 "title": "string",

 "description": "string",`
 ```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:39:21 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a2cb4237a34d0e449e2f6ccd535c6e8d-e4d99a1f1371c143-00",
    "errors": 
        "$": "Expected start of a property name or value, but instead reached end of data. Path: $ | LineNumber: 6 | BytePositionInLine: 24."
```

## №39 Books. Запрос GET{id} значение null.

1) URL: {{default_url}}/api/v1/Books/{{null}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 404

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 5e5f9e89-f708-4e06-996d-49c0060d25a6`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 09:41:04 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-4b3a8b9ce18fd14aac31e0455b214530-00eb53db2be97b41-00"
```

## №40 Books. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/Books/{{books_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: d5e2304f-2b94-4441-a418-cd57997968b8`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:23:35 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-07-16T10:23:36.0883459+00:00"
```

## №41 Books. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/Books/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: c558ad40-a693-402c-a4ed-1ff6d594ecf3`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 10:24:52 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c2181b5e92e2a941b4dc799abe88c80a-7661c57bac9c1b40-00",
    "errors": 
        "id": "The value '99999999999' is not valid."
```

## №42 Books. Запрос PUT{id}.

1) URL: {{default_url}}/api/v1/Books/{{books_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 10b6081e-b2ec-4555-bf58-a5696f926ff6`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 162`

4) Тело запроса:

```
 "id": 1,

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",

 "publishDate": "2023-07-12T11:02:57.145Z"
```
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:25:59 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-12T11:02:57.145Z"
```

## №43 Books. Запрос PUT{id} некорректный id.

1) URL: {{default_url}}/api/v1/Books/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 41222537-b3d3-4b23-a8d3-7a5ba4009d26`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 172`

4) Тело запроса:

```
 "id": 99999999999,

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",

 "publishDate": "2023-07-12T11:22:35.887Z"
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 10:27:57 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0ded75913f8d2a4bab2c4124fc14dce8-4be80b8faebd954f-00",
    "errors": 
        "id": "The value '99999999999' is not valid."
        "$.id": "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."
```

## №44 Books. Запрос PUT{id} некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Books/{{books_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: fdb63a40-5ed2-4d3d-90e4-92d2e932687e`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 66`

4) Тело запроса:

```
 "id": 1,

 "title": "string",

 "description": "string",`
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 10:29:11 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-270f1972e922934597ea4f4f5f5aa54a-a311df8f52a02a4b-00",
    "errors": 
        "$": "Expected start of a property name or value, but instead reached end of data. Path: $ | LineNumber: 6 | BytePositionInLine: 24."
```

## №45 Books. Запрос DELETE{id} некорректный id.

1) URL: {{default_url}}/api/v1/Books/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 84afb554-0101-40b6-86fe-a43c985a1b12`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 10:30:54 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-36697a195ada8a449b3fd9f6442f2fb2-98dd295ec081dd45-00",
    "errors":
        "id": "The value '99999999999' is not valid."
```

## №46 Books. Запрос DELETE{id}.

1) URL: {{default_url}}/api/v1/Books/{{books_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 4bc7d908-26d4-48ef-9395-7f4c804a9801`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 10:32:21 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`

6) Тело ответа: Отсутствует

## №47 Authors. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/Authors/{{authors_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 44f841e9-ba84-4e72-9cc2-746df78b6d8a`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:34:00 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
```

## №48 Authors. Запрос GET{id}.

1) URL: {{default_url}}/api/v1/Authors/authors/books/{{authors_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 99bbdd12-56f2-4f16-8b40-ac71f34ea366`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:35:06 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
```

## №49 Authors. Запрос POST.

1) URL: {{default_url}}/api/v1/Authors

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 36fb7118-f5c1-4f57-816c-1b85efb59016`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 82`

4) Тело запроса:

```
  "id": 1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
```
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:55:14 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
```

## №50 Authors. Запрос PUT{id}.

1) URL: {{default_url}}/api/v1/Authors/{{authors_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 2b08a9a7-c944-42fe-a25b-be967cc59a25`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 82`

4) Тело запроса:

```
  "id": 1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
```
 
5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 10:57:18 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 1,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
```

## №51 Authors. Запрос DELETE{id}.

1) URL: {{default_url}}/api/v1/Authors/{{authors_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 200

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: ae93c62b-33f3-46bc-968f-f0792b6f02b2`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`


4) Тело запроса: Отсутствует
 
5) Заголовки ответа:

`Content-Length: 0`

`Date: Mon, 17 Jul 2023 10:58:40 GMT`

`Server: Kestrel`

`api-supported-versions: 1.0`

6) Тело ответа: Отсутствует

## №52 Authors. Запрос POST, некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Authors

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: e1ca3d91-198f-47f5-8d69-580de1dd1494`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 31`


4) Тело запроса:

```

 "id": 0,

 "idBook": 0,`
 ```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:00:10 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1a8ed80280657243a9b011b9a68b5d51-448662ee43759346-00",
    "errors": 
        "$": "Expected start of a property name or value, but instead reached end of data. Path: $ | LineNumber: 4 | BytePositionInLine: 12."
```

## №53 Authors. Запрос PUT, некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Authors/{{authors_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 0a77678d-b859-4b85-ac42-1ebab08edf80`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 31`


4) Тело запроса:

```

 "id": 1,

 "idBook": 0,`
```
 
5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:02:47 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2f09ebf3e4ebc540b0922b1e05a67771-527a7b8553d55844-00",
    "errors": 
        "$": "Expected start of a property name or value, but instead reached end of data. Path: $ | LineNumber: 4 | BytePositionInLine: 12."
```

## №54 Authors. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/Authors/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: acbd92f9-b34e-49d6-aa76-9bb0733bd90f`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:04:36 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4ddf72a157fc474ea5df6b159102bb02-e3eeb9e6a4f63247-00",
    "errors":
        "id": "The value '99999999999' is not valid.
```

## №55 Authors. Запрос PUT{id} некорректный id.

1) URL: {{default_url}}/api/v1/Authors/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 190a05f9-7757-48c0-a984-1301bd59ff83`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 96`


4) Тело запроса:

```
 "id": 999999999,

 "idBook": 0,

 "firstName": "string",

 "lastName": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:06:19 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0aea86b90857794393022c38b8033b5e-90f8f34a6010894b-00",
    "errors":
        "id": "The value '99999999999' is not valid."
```

## №56 Authors. Запрос POST, значение null в теле запроса.

1) URL: {{default_url}}/api/v1/Authors

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: d9768a7c-d99b-40ec-9c94-392ffb797373`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 91`


4) Тело запроса:

```
 "id": null,

 "idBook": 0,

 "firstName": "string",

 "lastName": "string"
```

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:08:06 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e9e8c7be68169543bf15dcc9306dd569-4956067adc13a44f-00",
    "errors":
        "$.id":
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
```

## №57 Authors. Запрос POST, некорректное тело запроса.

1) URL: {{default_url}}/api/v1/Authors

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`Content-Type: application/json`

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 4baf6051-b862-470e-8251-ddb5396456fd`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`

`Content-Length: 96`


4) Тело запроса:

```
 "id": 999999999,

 "idBook": 0,

 "firstName": "string",

 "lastName": "string"
```

5) Заголовки ответа:

`Content-Type: application/json; charset=utf-8; v=1.0`

`Date: Mon, 17 Jul 2023 11:09:11 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

`api-supported-versions: 1.0`

6) Тело ответа:

```
    "id": 999999999,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
```

## №58 Authors. Запрос GET{id} некорректный id.

1) URL: {{default_url}}/api/v1/Authors/authors/books/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 571fb321-0d2e-4087-a22a-a3511de14bdd`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`


4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:13:45 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9753aea67f034c46834160104fab398e-064ef9481e098745-00",
    "errors":
        "idBook":
            "The value '99999999999' is not valid."
```

## №59 Authors. Запрос DELETE{id} некорректный id.

1) URL: {{default_url}}/api/v1/Authors/{{wrong_id}}

2) Ожидаемый результат: Сервер присылает ответ со статус-кодом 400

3) Заголовки запроса:

`User-Agent: PostmanRuntime/7.32.3`

`Accept: */*`

`Postman-Token: 87ddd82e-3459-4d60-8021-43cbb8fce693`

`Host: fakerestapi.azurewebsites.net`

`Accept-Encoding: gzip, deflate, br`

`Connection: keep-alive`


4) Тело запроса: Отсутствует

5) Заголовки ответа:

`Content-Type: application/problem+json; charset=utf-8`

`Date: Mon, 17 Jul 2023 11:13:45 GMT`

`Server: Kestrel`

`Transfer-Encoding: chunked`

6) Тело ответа:

```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d09a89e161abe34ba4253ee91898af6a-9973ee770849384e-00",
    "errors":
        "id":"The value '99999999999' is not valid."
```