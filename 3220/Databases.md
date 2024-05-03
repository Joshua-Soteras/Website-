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
- 
