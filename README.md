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


Ubuntu trust the certificate for service-to-service communication \
cli:
```
dotnet dev-certs https
sudo -E dotnet dev-certs https -ep /usr/local/share/ca-certificates/aspnet/https.crt --format PEM
sudo update-ca-certificates
```
