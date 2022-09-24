# Implicit

Тип предоставления Implicit оптимизирован для общедоступных клиентов, например реализованных в JavaScript или на мобильных устройствах, где учетные данные клиента не могут быть сохранены.

### Пример запроса

```
POST 
/?oauth=authorize HTTP/1.1
 
Headers
Content-Type: application/x-www-form-urlencoded
 
Body Request
response_type=token
&client_id={client-id
```

После успешного запроса браузер пользователя будет перенаправлен обратно к клиенту, содержащему параметры URL.

```
#access_token={access-token}&expires_in=3600&token_type=Bearer&scope=basic
```

Если есть ошибка в аутентификации, сервер ответит, какая такая в параметрах URL.
