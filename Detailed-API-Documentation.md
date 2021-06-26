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



## User Related APIs

### `GET` `/users/@{username}`
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
Get details of a given user by username

### `GET` `/users/{userid}`
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
Get details of a given user by userid

### `POST` `/users`
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
Create a new user

### `PATCH` `/users` 🔒 
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
Update bio/name/image etc of an user

### `PUT` `/users/{userid}/follow` 🔒 
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
Follow the given user

### `DELETE` `/users/{userid}/follow` 🔒 
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
Un-follow the given user

### `GET` `/users/{userid}/followers` 📃 
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
Get a list of all followers of this user

### `GET` `/users/{userid}/followings` 📃 
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
Get a list of all following of this user




## Post Related APIs

### `GET` `/posts` 📃 
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
Get the list of all posts

### `GET` `/posts/{postid}`
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
Get Details of a post

### `POST` `/posts` 🔒 
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
Create a new post

### `DELETE` `/posts/{postid}` 🔒 
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
Delete a given post

### `PUT` `/posts/{postid}/like` 🔒 
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
Like the given post

### `DELETE` `/posts/{postid}/like` 🔒 
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
Un-like the given post



## Hashtag Related APIs

### `GET` `/hashtags` 📃 
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
Top hashtags (default top 10)

### `GET` `/hashtags/{hashtag}/posts` 📃 
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
All posts of this given hashtag