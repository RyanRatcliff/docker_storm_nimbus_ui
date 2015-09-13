# Docker Nimbus UI
A very basic Docker Nimbus container, with an additional fake AWS credential file to allow for connections to a local dynamodb instance.

### To build the container
```
docker build -t ryanratcliff/nimbus_ui .
```

### Alternatively, the container can be pulled from Docker Registry
```
docker pull ryanratcliff/nimbus_ui
```

# Example usages

### To startup as is, requires a zookeeper instance defined as 'zookeeper'
```
docker run -d --link my_zookeeper:zookeeper ryanratcliff/nimbus_ui
```

### To startup with all ports exposed to host
```
docker run -d -P --link my_zookeeper:zookeeper ryanratcliff/nimbus_ui
```

### To startup with specific port exposed
```
docker run -d p 8080:8080 --link my_zookeeper:zookeeper ryanratcliff/nimbus_ui
```
