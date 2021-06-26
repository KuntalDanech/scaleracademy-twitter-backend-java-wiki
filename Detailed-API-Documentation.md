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
```bash
curl -X GET "http://localhost:8082/users/%40first"
```

### Response
```json
{
  "id": "30761418-70e6-46dc-8af5-17670e78f293",
  "username": "first",
  "name": "Nice Name",
  "avatar": "URL://updated-picture.png",
  "bio": "Updated Bio",
  "followerCount": 0,
  "followingCount": 0,
  "verified": false
}
```
Get details of a given user by username

### `GET` `/users/{userid}`
#### Request
```bash
curl -X GET "http://localhost:8082/users/30761418-70e6-46dc-8af5-17670e78f293"
```

### Response
```json
{
  "id": "30761418-70e6-46dc-8af5-17670e78f293",
  "username": "first",
  "name": "Nice Name",
  "avatar": "URL://updated-picture.png",
  "bio": "Updated Bio",
  "followerCount": 0,
  "followingCount": 0,
  "verified": false
}
```
Get details of a given user by userid

### `POST` `/users`
#### Request
```json
{
  "username": "first",
  "name": "Nice Name",
  "bio": "Bio of 240 characters",
  "avatar": "URL://picture.png"
}
```

### Response
```json
{
  "id": "30761418-70e6-46dc-8af5-17670e78f293",
  "username": "first",
  "name": "Nice Name",
  "avatar": "URL://picture.png",
  "bio": "Bio of 240 characters",
  "followerCount": 0,
  "followingCount": 0,
  "verified": false
}
```
Create a new user

### `PATCH` `/users` 🔒 
#### Request
```json
{
  "id": "30761418-70e6-46dc-8af5-17670e78f293",
  "username": "first",
  "name": "Nice Name",
  "avatar": "URL://updated-picture.png",
  "bio": "Updated Bio"
}
```

### Response
```json
{
  "id": "30761418-70e6-46dc-8af5-17670e78f293",
  "username": "first",
  "name": "Nice Name",
  "avatar": "URL://updated-picture.png",
  "bio": "Updated Bio",
  "followerCount": 0,
  "followingCount": 0,
  "verified": false
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