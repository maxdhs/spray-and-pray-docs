# Spray and Pray API Documentation

## GET /users

### Request:

```js
fetch(`${API}/users`);
```

### Response:

```js
{
  "success": true,
  "users": [
    {
      "id": "0de64544-2f66-40bc-8649-aa5c618c5b38",
      "name": "Max",
      "count": 2
    },
    {
      "id": "79f31fc8-8ca9-4744-a9ac-a68a89d71be2",
      "name": "Abdel",
      "count": 11
    },
    {
      "id": "a5afe6f1-fca6-4752-856a-ca2fa9a54eb6",
      "name": "Adam",
      "count": 6
    }
  ]
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
    "id": "ee8d4a19-559e-43b5-834f-078efe80ddac",
    "name": "Jhon",
    "count": 0
  }
}
```

## PUT /users/:userId

### Request:

```js
fetch(`${API}/users/ee8d4a19-559e-43b5-834f-078efe80ddac`, {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    count: 3,
    name: "Jhonathan",
  }),
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "ee8d4a19-559e-43b5-834f-078efe80ddac",
    "name": "Jhonathan",
    "count": 3
  }
}
```

## DELETE /user/:userId

### Request:

```js
fetch(`${API}/users/ee8d4a19-559e-43b5-834f-078efe80ddac`, {
  method: "DELETE",
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "ee8d4a19-559e-43b5-834f-078efe80ddac",
    "name": "Jhon",
    "count": 3
  }
}
```
