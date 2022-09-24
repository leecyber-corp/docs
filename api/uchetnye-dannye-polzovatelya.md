# Учетные данные пользователя

Учетные данные пользователя позволят вам напрямую использовать данные для входа пользователя в вашем приложении.

**Пример запроса**

Запрос примеров использования разрывов строк для содержимого тела, чтобы облегчить его чтение. Заголовок авторизации состоит из значения в кодировке base64 для "**client\_id:client\_secret**".

<pre><code><strong>POST 
</strong>/?oauth=token HTTP/1.1
 
Headers
Authorization: Basic cXhaNmZDb0dsadsa9NajRjTks4U1hSSGE1bnVnNnZuc3dsRldTRjM3aHNXMzpMMWZ6TG9zSmY5VGx3bkNDVFo1cGtLbWRxcWtIU2hLRWkwZDRvRk5F
Content-Type: application/x-www-form-urlencoded
 
Body Request
grant_type=password
&#x26;username={users-username}
&#x26;password={users-password}</code></pre>

Успешный ответ будет содержать следующее.

```
{
  "access_token": "apvwxkbcxrnm9o92wmp4yjlbmoajeycfbn4ws6nx",
  "expires_in": 9087654,
  "token_type": "Bearer",
  "scope": "basic",
  "refresh_token": "z8wpp3pshgled4d81b4z8dmlc6ftwdscpgktyh7u"
}
```

**Заметка:**

Некоторые серверы, на которых работает CGI, не могут обрабатывать заголовки авторизации. В этом случае можно передать «client\_id» и «client\_secret» в теле запроса.

```
POST /?oauth=token HTTP/1.1
 
Headers
Content-Type: application/x-www-form-urlencoded
 
Body Request
grant_type=password
&username={users-username}
&password={users-password}
&client_id={client_id}
&client_secret={client_secret}
```
