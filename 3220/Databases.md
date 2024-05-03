## Client Vs. Server
###Client
- MySql
- MySQL Workbench
- Adminer 

### Server
- where the databases are located


### interaction
- in order to interact with the databases, a library is needed

![image](https://github.com/Joshua-Soteras/Website-/assets/100913169/116deb77-bbc5-4321-87f0-e453bbb04b0e)


## Java Database Connectivity (JDBC) 
- The library that allows us to connect to the databases

### The components
- JDBC -> JDBC Driver -> Server

### Example of JDBC
```
String sql = "
select * from employees";
Connection c = DriverManager.getConnection( url );
Statement stmt = c.createStatement();
ResultSet rs = stmt.executeQuery( sql );
List<Employee> employees = new ArrayList<Employee>();
while( rs.next() ){
  employees.add(new Employee( rs.getInt("id"),
  rs.getString("first_name"), rs.getString("last_name"),
  rs.getInt("supervisor_id")
  );
}
``` 

### mistmatch between 00 Class Design and Relationaal Schema
- an employe object cannot be stored in a relational databases 
- Must Reference using ID
- tedious code to conver btween objects and schema


## Object-Relational Mapping (ORM) Approach (Better Approach/Method) 
### Breaking it down
![image](https://github.com/Joshua-Soteras/Website-/assets/100913169/d834f3f6-a3ad-45b1-828a-a257a426d8bb)

- ORM Library sits between the application and relational databases
- allows us to deal with the objects without having to worry about how the objects are stored

  ### Java Persistance API
  - Annotations for object-relational mapping
  - Data Access API
 
## Using JPA within the given Lab
Steps and process in order to 
1. Install Dependencies
2. Applicaiton Properties
3. Mapping (Using Annotations) 

### Install Dependencies (When creating a new project) 
1. Apache Freemarker
2. Spring Boot DevTools
3. Spring Web Validation
5. MySQL Driver
6. Spring Data JPA

```
<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-freemarker</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>com.mysql</groupId>
			<artifactId>mysql-connector-j</artifactId>
			<scope>runtime</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
```

### Application Properties 

```
pring.datasource.url=jdbc:mysql://<hostname>/<dbname>
spring.datasource.username=<username>
spring.datasource.password=<password>
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.show-sql=true
spring.jpa.generate-ddl=true
```

### Mapping 
- @Entity
  - This goes above the class data model
  - will be stored in data based
  - 
  - most of the controller classes have nothing to do with databases
- @Id
  - Annotation within @Entity
  - needs an ID
  - jakarta.persistence
-@GeneratedValue
  - this annotation: want to generate values for the Id field
  - 

### (Creating a new project) 
- New
- Project
- Spring start
-  install dependencies



   
