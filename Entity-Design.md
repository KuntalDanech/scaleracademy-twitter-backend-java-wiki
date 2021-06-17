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

### `posts`
| column_name      | column_definition                  |
|------------------|------------------------------------|
| id               | UUID                               |
| text             | string (30) - alphanumeric         |
| user_id          | UUID - FK(users.id)                |
| images           | array < string (URL) > - MAX 4     |
| mentions         | array < name: string, id: UUID >   |
| original_post_id | UUID (self reference, can be NULL) |
| reply_to_id      | UUID (self reference, can be NULL) |
| like_count       | bigint                             |
| repost_count     | bigint                             |
| hashtags         | array < string >                   |










***

## Database Tables for future implementations