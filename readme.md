# Kiplo - API Documentation (v1)
## API Authentication
Kiplo uses Basic Auth of the user's API key and secret to authenticate each request. To retrieve a user's API key and secret, use the `POST /auth` endpoint, passing the user's email and password authenticated with Basic Auth.
## API Endpoints
### POST /auth
Authenticates user and returns user API keys

#### Request
```shell
curl -X POST -u email:password http://kiplo.net/api/auth
```

#### Response
```json
{
  "api_key": "d691dfa5498c932b852fd6a45a2d0515",
  "api_secret": "4ca8dbe87d76306ae00cce35967b619b"
}
```

-
### GET /ping
Pings the server.

#### Response
```json
{
  "ping": "pong"
}
```

-
### GET /users/me

Returns the current user.

#### Response
```json
{
  "id": "1",
  "email": "barraca@anaba.com",
  "firstname": "Barraca",
  "lastname": "Abana",
  "created_at": "2013-07-12 08:22:37",
  "updated_at": "2013-07-12 08:22:37"
}
```

-
### GET /users

Returns array of users associated with your sites and the sites you belong to.

#### Response
```json
[
 {
   "id": "1",
   "email": "barraca@anaba.com",
   "firstname": "Barraca",
   "lastname": "Abana",
   "created_at": "2013-07-12 08:22:37",
   "updated_at": "2013-07-12 08:22:37"
 }
]
```

-
