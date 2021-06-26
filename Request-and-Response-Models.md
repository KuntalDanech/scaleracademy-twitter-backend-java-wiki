


### `User`
```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "username": "string",
  "name": "string",
  "avatar": "string",
  "bio": "string",
  "followerCount": 0,
  "followingCount": 0,
  "verified": true
}
```


### `Post`
```json
[
  {
    "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "text": "string",
    "userId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "images": [
      "string"
    ],
    "repostCount": 0,
    "likeCount": 0,
    "hashtags": [
      "string"
    ],
    "mentions": [
      "string"
    ],
    "originalPostId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "replyToId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "timestamp": "2021-06-26T19:32:31.744Z",
  }
]
```


### `Hashtag`
```json
[
  {
    "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "tag": "string",
    "recentPostCount": 0
  }
]
```


### `Application Error Response` _(under development)_
```json
{
  "empty": true,
  "model": {},
  "modelMap": {
    "additionalProp1": {},
    "additionalProp2": {},
    "additionalProp3": {}
  },
  "reference": true,
  "status": "ACCEPTED",
  "view": {
    "contentType": "string"
  },
  "viewName": "string"
}
```
