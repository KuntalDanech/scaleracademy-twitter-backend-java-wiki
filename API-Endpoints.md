## Key

### 🔒: API is secured with JWT

### 📃: API is Paginated



## Authentication API

### `POST` `/authenticate`
Authenticate the User and provides them with a JWT token as a response



## User Related APIs

### `GET` `/users/@{username}`
Get details of given user by username

### `GET` `/users/{userid}`
Get details of given user by userid

### `POST` `/users`
Create a new user

### `PATCH` `/users/{userid}` 🔒 
Update bio/name/image etc of an user

### `PUT` `/users/{userid}/follow` 🔒 
Follow the given user

### `DELETE` `/users/{userid}/follow` 🔒 
Un-follow the given user

### `GET` `/users/{userid}/followers` 📃 
Get a list of all followers of this user

### `GET` `/users/{userid}/followings` 📃 
Get a list of all following of this user



## Posts Related APIs

### `GET` `/posts` 📃 
Get list of all posts

### `GET` `/posts/{postid}`
Get Details of a post

### `POST` `/posts` 🔒 
Create a new post

### `DELETE` `/posts/{postid}` 🔒 
Delete a given post id

### `PUT` `/posts/{postid}/like` 🔒 
Like the given post

### `DELETE` `/posts/{postid}/like` 🔒 
Un-like the given post



## Hashtags Related APIs

### `GET` `/hashtags` 📃 
Top hashtags (default top 10)

### `GET` `/hashtags/{tag}/posts` 📃 
All posts of this given hashtag