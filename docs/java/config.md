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
> MockMVC with CustomMessageConverters- Unit Test cases
```
 Mockmvc mockmvc = MockMVCBuilders.standaloneSetup(EmployeeController.class)
                        .setMessageConverters(jackson2HttpMessageConverter()).build();

public MappingJackson2HttpMessageConverter jackson2HttpMessageConverter(){
    ObjectMapper mapper = new ObjectMapper();
    mapper.configure(SerializationFeature.WRITE_DATES_AS_TIMESTAMPS, false);
    mapper.configure(SerializationFeature.WRITE_DATES_TIMESTAMPS_AS_NANOSECONDS, true);
    mapper.setSerializationInclusion(JsonInclude.Include.NON_NULL);
    
    mapper.registerModule(new JavaTimeModule());

    return new MappingJackson2HttpMessageConverter(objectMapper);    
}
```



> # Hibernate Configuration for SQL Statement in Console logs - Spring boot app
``` 
logging.level.org.hibernate.SQL= DEBUG
logging.level.org.hibernate.type.descriptor.sql.BasicBinder=TRACE
```

