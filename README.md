### Up container
```
docker compose up -d
```

### Enter container
```
docker exec -it appproduct bash
```


### Open sqlite and create table products
Inside the container run the follow command
```
sqlite3 db.sqlite
```
```
create table products (id string, name string, price float, status string);
```

### Check cli commands
```
go run main.go cli --help
```

### Create a product
```
go run main.go cli -a=create -n="Product CLI 2" -p=28.0
```

### Open webserver
```
go run main.go http
```

### Get a product
```
curl http://localhost:9000/product/{id}
```
