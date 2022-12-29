### Deployment
1. Create lambda for go 1.x
    - with new role from template simple microservice with priviligies to dynamodb
    - upload zip archive with build main out of cmd/main.go- 
    - change Lambda's runtime setting - change handler to "main"
2. Deploy API Gataway - rest api, create a single method - any
3. Create dynamodb table - LambdaInGoUser

### Testing
1. Create user 
```
POST method
HEADER Content-Type : application/json
Body 
{
    "email": "Toby@example.com",
    "firstName": "Michael",
    "lastName": "Va"
}
```

2. Update USER
```
PUT method
HEADER Content-Type : application/json
Body 
{
    "email": "Toby@example.com",
    "firstName": "Newname",
    "lastName": "Newdata"
}
```

3. Get User
```
GET method
HEADER Content-Type : application/json
Body 
{
    "email": "Toby@example.com",
}
```

4. Delete user
```
DELETE method
HEADER Content-Type : application/json
Body 
{
    "email": "Toby@example.com",
}
```