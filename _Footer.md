***
Twitter Clone Backend


**User Related APIs**

*   Type - *GET* /users/@{username}
    *   Get details of given user by username

*   Type - *GET* /users/{userid}
    *   Get details of given user by userid

*   Type - *POST* /users
    *   Create a new user

*   Type - *PATCH* /users/{userid}
    *   Update bio/name/image etc of an user

*   Type - *PUT* /users/{userid}/follow
    *   Follow the given user

*   Type - *DELETE* /users/{userid}/follow
    *   Un-follow the given user

*   Type - *GET* /users/{userid}/followers
    *   Get a list of all followers of this user

*   Type - *GET* /users/{userid}/followees
    *   Get a list of all followees of this user


**Posts Related APIs**

*   Type - *GET* /posts
    *   Get list of all posts

*   Type - *GET* /posts/{postid}
    *   Get Details of a post

*   Type - *POST* /posts
    *   Create a new post

*   Type - *DELETE* /posts/{postid}
    *   Delete a given post id

*   Type - *PUT* /posts/{postid}/like
    *   Like the given post

*   Type - *DELETE* /posts/{postid}/like 
    *   Un-like the given post


**Hashtags Related APIs**

*   Type - *GET* /hashtags
    *   Top hashtags (default top 10)

*   Type - *GET* /hashtags/{tag}/posts
    *   All posts of this given hashtag