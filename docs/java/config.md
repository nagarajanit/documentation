> # Jackson Configuration for LocalDateTime DataType
```
Maven Dependency
<dependency>
    <groupId>com.fasterxml.jackson.datatype</groupId>
    <artifactId>jackson.datatype-jsr310</artifactId>
</dependency>

Below is the code for ObjectMapper
ObjectMapper mapper = new ObjectMapper()
mapper.findAndRegisterModules()
```

> # Hibernate Configuration for SQL Statement in Console logs - Spring boot app
``` 
logging.level.org.hibernate.SQL= DEBUG
logging.level.org.hibernate.type.descriptor.sql.BasicBinder=TRACE
```

