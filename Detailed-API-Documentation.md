## Authentication API

### `POST` `/authenticate`
#### Request
```json
{
  "username": "username",
  "password": "Password"
}
```

### Response
```json
{
  "jwt": "JSON.Web.Token"
}
```


Authenticate the User and provides them with a JWT token as a response