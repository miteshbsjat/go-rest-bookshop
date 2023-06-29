# Bookstore REST API using Gin and Gorm

## Build the code golang 1.19 version

```bash
go build main.go
```


## Run the service

```bash
./main
```

## Post some books
```bash
curl -H 'Content-Type: Application/Json' -d '{"title":"Start learning golang","author":"Mitesh Jat"}' localhost:8080/books
curl -H 'Content-Type: Application/Json' -d '{"title":"Start learning rest with go","author":"Reenu S"}' localhost:8080/books
```

## Read the Books 

```bash
curl localhost:8080/books | jq
{
  "data": [
    {
      "id": 1,
      "title": "Start learing golang",
      "author": "Mitesh Jat"
    },
    {
      "id": 2,
      "title": "Start learning rest with go",
      "author": "Reenu S"
    }
  ]
}

```