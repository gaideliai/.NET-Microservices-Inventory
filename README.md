# .NET-Microservices-Inventory

Endpoints:

Assign catalog item to a user: \
POST `https://localhost:5005/items`
```
{
    "userId": "{{$guid}}", //for random guid
    "catalogItemId": "guid",
    "quantity": "int"
}
```

Get the user's catalog items \
GET `https://localhost:5005/items?userId=<guid>`
