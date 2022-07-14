Step 4: Adding test class 
=============

For using Testcontainers , you need to annotate test class with `@Testcontainers`.
Add the following to the body in the test class:
```
@Container
public PostgreSQLContainer<?> postgresDB = new PostgreSQLContainer<>("postgres:13.2")
                                            .withDatabaseName("yourDatabaseName");
```
In case you use Jnuit 4 then replace `@Container` with `@ClassRule`. 
The `@Container / @ClassRule` annotation tells JUnit to notify this field about various events in the test lifecycle.

```
@SpringBootTest(webEnvironment = WebEnvironment.RANDOM_PORT)
@Testcontainers
@DirtiesContext
public  class ContainerBaseIT {
	
	@Autowired
	protected TestRestTemplate testRestTemplate ;

	@Container
	public static PostgreSQLContainer<?> postgresDB = new PostgreSQLContainer<>                
                                                             ("postgres:13.2")
			                                     .withDatabaseName("yourDatabaseName")
                                                             .withUsername("postgres")
                                                             .withPassword("postgres")
			                                     .withInitScript("ddl.sql");


	@DynamicPropertySource
	public static void properties(DynamicPropertyRegistry registry) {
		registry.add("spring.datasource.url",postgresDB::getJdbcUrl);
		registry.add("spring.datasource.username", postgresDB::getUsername);
		registry.add("spring.datasource.password", postgresDB::getPassword);

	}
}

```


