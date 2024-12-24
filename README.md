# poc-mockserver-expectations
Testing mockserver via docker-compose

---

### How to run 🎯

- `docker-compose up`

### Dashboard 📱

- http://localhost:1080/mockserver/dashboard

---

### Requests / Responses ✅

**GET**

````
curl --location 'http://localhost:1080/api/v1/books?code=13200'
````

````json
{
    "name": "Memorial do Convento"
}
````

**PUT**

````
curl --location --request PUT 'http://localhost:1080/api/v1/books/13200' \
--header 'Content-Type: application/json' \
--data '{
  "id": 13200,
  "name": "Memorial do Convento v2024",
  "status": "active"
}'
````

````json
{
    "message": "Resource updated successfully",
    "updatedResource": {
        "id": 13200,
        "name": "Memorial do Convento v2024",
        "status": "active"
    }
}
````
