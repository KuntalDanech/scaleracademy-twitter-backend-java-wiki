## Database Tables that are currently in use

### `users`
| column_name     | column_definition          |
|-----------------|----------------------------|
| id              | UUID                       |
| username        | string (30) - alphanumeric |
| name            | string (50)                |
| email           | string (50)                |
| avatar          | string (URL)               |
| bio             | string (240)               |
| follower_count  | bigint                     |
| following_count | bigint                     |
| verified        | boolean                    |
| created_at      | datetime                   |
| updated_at      | datetime                   |

### `posts`
| column_name      | column_definition                                       |
|------------------|---------------------------------------------------------|
| id               | UUID                                                    |
| text             | string (30) - alphanumeric                              |
| user_id          | UUID - FK(users.id)                                     |
| images           | map < key: string (URL) , value: datetime > - MAX 4     |
| mentions         | map < key: UUID - FK(users.id) , value: datetime >      |
| original_post_id | UUID (self reference, can be NULL)                      |
| reply_to_id      | UUID (self reference, can be NULL)                      |
| like_count       | bigint                                                  |
| repost_count     | bigint                                                  |
| hashtags         | array < string >                                        |
| created_at       | datetime                                                |
| updated_at       | datetime                                                |

### `hashtags`
| column_name       | column_definition                        |
|-------------------|------------------------------------------|
| id                | UUID                                     |
| tag               | string (240) (only /^[ A-Za-z0-9_ ]*$/ ) |
| recent_post_count | bigint                                   |
| created_at        | datetime                                 |
| updated_at        | datetime                                 |

### `like`
| column_name | column_definition   |
|-------------|---------------------|
| id          | UUID                |
| post_id     | UUID - FK(posts.id) |
| user_id     | UUID - FK(users.id) |
| created_at  | datetime            |
| updated_at  | datetime            |

### `hashtags_post`
| column_name | column_definition      |
|-------------|------------------------|
| id          | UUID                   |
| hashtag_id  | UUID - FK(hashtags.id) |
| post_id     | UUID - FK(posts.id)    |
| created_at  | datetime               |
| updated_at  | datetime               |

### `users_following`
| column_name   | column_definition   |
|---------------|---------------------|
| id            | UUID - FK(users.id) |
| following_key | UUID (users.id)     |
| following     | datetime            |

### `users_follower`
| column_name  | column_definition   |
|--------------|---------------------|
| id           | UUID - FK(users.id) |
| follower_key | UUID (users.id)     |
| follower     | datetime            |

### `posts_images`
| column_name | column_definition   |
|-------------|---------------------|
| post_id     | UUID - FK(posts.id) |
| images_key  | string(URL)         |
| images      | datetime            |

### `posts_mention`
| column_name  | column_definition   |
|--------------|---------------------|
| post_id      | UUID - FK(posts.id) |
| mentions_key | UUID (users.id)     |
| mentions     | datetime            |

### `posts_hashtag`
| column_name  | column_definition   |
|--------------|---------------------|
| post_id      | UUID - FK(posts.id) |
| hashtags_key | UUID (hashtags.id)  |
| hashtags     | datetime            |




***

## Database Tables for future implementations (proposed)