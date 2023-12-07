# spring-liquibase
Using Liquibase Maven Plugin with Spring Boot

# run command
1. Check Liquibase project directory to store all Liquibase files.
2. Update a Liquibase properties file or use the existing liquibase.properties file included with the Liquibase installation package.
3. Update a XML file called db-common-changelog-master.xml or use the changelog file from the database directory. Liquibase also supports the .sql, .yaml, or .json changelog formats.
4. Specify the changelog file in pom.xml or the Liquibase properties file, as follows:
	pom.xml: <changeLogFile>your/path/to/db-common-changelog-master.xml</changeLogFile>
		 <liquibase.propertyFile>your/path/to/liquibase.properties</liquibase.propertyFile>
5. Run the following command to compile and test your Spring Boot application code:
	mvn compile package
6. Run the update-sql goal to inspect the SQL before applying changes to your database:
	mvn liquibase:update-sql
7. Deploy your changes by using the update goal:
	mvn liquibase:update
		 
