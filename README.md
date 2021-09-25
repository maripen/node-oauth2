# Oauth2 play

## Run the application

```
    npm test && node .
```

## Tech Stack Used

- `Docker`
- `ExpressJS`
- `NodeJS`
- `Sequelize`
- `Finale`
- `SQLite`
- `Okta`

## Test commands - unauthorised

```

curl localhost:3000/parts
```
```
curl localhost:3000/parts -X POST -d '{
"partNumber": "abc-123",
"modelNumber": "xyz-789",
"name": "Alphabet Soup",
"description": "Soup with letters and numbers in it"
}'
```
```
curl localhost:3000/parts
```

## Test commands - with Okta auth

```

node client http://localhost:3000/parts
```
```
node client http://localhost:3000/parts post '{
  "partNumber": "ban-bd",
  "modelNumber": 1,
  "name": "Banana Bread",
  "description": "Bread made from bananas"
}'
```
```
node client http://localhost:3000/parts
```
```
node client http://localhost:3000/parts/1 delete
```