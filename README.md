# Spray and Pray API Documentation

```js
const API = "https://spray-and-pray-backend.onrender.com"
```

## GET /users

### Request:

```js
fetch(`${API}/users`);
```

### Response:

```js
{
"success": true,
"users": [{...}, {...}, {...}]
}
```

## POST /users

### Request:

```js
fetch(`${API}/users`, {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    name: "Jhon",
  }),
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "b52c4655-3cde-489f-aa93-7869bcc0a802",
    "name": "Jhon",
    "count": 0,
  }
}
```

## PUT /users/:userId

### Request:

```js
fetch(`${API}/users/${user.id}`, {
  method: "PUT",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    count: 3,
    name: "Jhon",
  }),
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "b52c4655-3cde-489f-aa93-7869bcc0a802",
    "name": "Jhon",
    "count": 3,
  }
}
```

## DELETE /users/:userId

### Request:

```js
fetch(`${API}/users/${user.id}`, {
  method: "DELETE",
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "b52c4655-3cde-489f-aa93-7869bcc0a802",
    "name": "Jhon",
    "count": 3,
  }
}
```
