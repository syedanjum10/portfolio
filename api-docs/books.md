# Books API
## Overview
The Books API allows clients to retrieve information about books available in the BookHub catalog.
## GET All Books
### Endpoint
```http
GET /books
```
### Description
Returs a list of all books availaible in the BookHub catalog.

### Sample Response
```json
[
{
    "id": 101,
    "title": "Atomic Habits",
    "author": "James Clear",
    "price": 19.99,
    "available": true
},
{
    "id": 102,
    "title": "Deep Work",
    "author": "Cal Newport",
    "price": 15.99,
    "available": false
}
]
```

### Response Fields

| Field | Type | Description |
|-------|------|-------------|
| `id` | Integer | Unique identifier for the book. |
| `title` | String | Title of the book. |
| `author` | String | Name of the author. |
| `price` | Number | Price of the book. |
| `available` | Boolean | Indicates whether the book is available for purchase. |

### Status Codes

| Status Code| Description |
|-------|-------------|
| `200 ok` | The request was successful, and the list of books was returned. |
| `400 Bad Request` | The request is invalid or contains incorrect parameters. |
| `404 Not Found` | The requested resource was not found. |
| `500 Internal Server Error` | An unexpected error occured on the server. |

### Example Request

```bash
curl -X GET https://api.bookhub.com/books
```

### Notes

- This endpoint returns all the books available in the BookHub catalog.
- The response is returned in JSON format.
- Each book in the response contains details such as the title, author, price, and availability.
- The Status Code indicates the success or failure of the response.