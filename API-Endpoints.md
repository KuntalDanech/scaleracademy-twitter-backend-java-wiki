## Key

### 🔒: API is secured with JWT

### 📃: API is Paginated



## Authentication API

### `POST` `/authenticate`
Authenticate the User and provides them with a JWT token as a response



## User Related APIs

### `GET` `/user/@{username}`
Get details of given user by username

### `GET` `/user/{userid}`
Get details of given user by userid

### `POST` `/user`
Create a new user

### `PATCH` `/user` 🔒 
Update bio/name/image etc of an user

### `PUT` `/user/{userid}/follow` 🔒 
Follow the given user

### `DELETE` `/user/{userid}/follow` 🔒 
Un-follow the given user

### `GET` `/user/{userid}/followers` 📃 
Get a list of all followers of this user

### `GET` `/user/{userid}/followings` 📃 
Get a list of all following of this user



## Post Related APIs

### `GET` `/posts` 📃 
Get list of all posts

### `GET` `/post/{postid}`
Get Details of a post

### `POST` `/post` 🔒 
Create a new post

### `DELETE` `/post/{postid}` 🔒 
Delete a given post

### `PUT` `/post/{postid}/like` 🔒 
Like the given post

### `DELETE` `/post/{postid}/like` 🔒 
Un-like the given post



## Hashtag Related APIs

### `GET` `/hashtags` 📃 
Top hashtags (default top 10)

### `GET` `/hashtag/{tag}/posts` 📃 
All posts of this given hashtag