## Database Tables that are currently in use

### `user`
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

### `post`
| column_name      | column_definition                                       |
|------------------|---------------------------------------------------------|
| id               | UUID                                                    |
| text             | string (30) - alphanumeric                              |
| user_id          | UUID - FK(users.id)                                     |
| images           | map < key: string (URL) , value: datetime > - MAX 4     |
| mentions         | map < key: UUID - FK(user.id) , value: datetime >       |
| original_post_id | UUID (self reference, can be NULL)                      |
| reply_to_id      | UUID (self reference, can be NULL)                      |
| like_count       | bigint                                                  |
| repost_count     | bigint                                                  |
| hashtags         | array < string >                                        |
| created_at       | datetime                                                |
| updated_at       | datetime                                                |

### `hashtag`
| column_name       | column_definition                        |
|-------------------|------------------------------------------|
| id                | UUID                                     |
| tag               | string (240) (only /^[ A-Za-z0-9_ ]*$/ ) |
| recent_post_count | bigint                                   |
| created_at        | datetime                                 |
| updated_at        | datetime                                 |

### `like`
| column_name | column_definition  |
|-------------|--------------------|
| id          | UUID               |
| post_id     | UUID - FK(post.id) |
| user_id     | UUID - FK(user.id) |
| created_at  | datetime           |
| updated_at  | datetime           |

### `hashtag_post`
| column_name | column_definition     |
|-------------|-----------------------|
| id          | UUID                  |
| hashtag_id  | UUID - FK(hashtag.id) |
| post_id     | UUID - FK(post.id)    |
| created_at  | datetime              |
| updated_at  | datetime              |

### `user_following`
| column_name   | column_definition  |
|---------------|--------------------|
| id            | UUID - FK(user.id) |
| following_key | UUID (user.id)     |
| following     | datetime           |

### `user_follower`
| column_name  | column_definition  |
|--------------|--------------------|
| id           | UUID - FK(user.id) |
| follower_key | UUID (user.id)     |
| follower     | datetime           |

### `post_images`
| column_name | column_definition  |
|-------------|--------------------|
| post_id     | UUID - FK(post.id) |
| images_key  | string(URL)        |
| images      | datetime           |

### `post_mention`
| column_name  | column_definition  |
|--------------|--------------------|
| post_id      | UUID - FK(post.id) |
| mentions_key | UUID (user.id)     |
| mentions     | datetime           |

### `post_hashtag`
| column_name  | column_definition  |
|--------------|--------------------|
| post_id      | UUID - FK(post.id) |
| hashtags_key | UUID (hashtag.id)  |
| hashtags     | datetime           |




***

## Database Tables for future implementations (proposed)