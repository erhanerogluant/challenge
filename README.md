# challenge
# CRUD Web Service with Spring Boot
This is a simple REST web service built in Java using Spring Boot to ingest spreadsheet documents into a database and perform basic CRUD operations on the created records. The web service returns the ingested records as JSON objects.

### Technology Stack
* Java 8 or higher
* Spring Boot (version 2+)
* Apache POI for spreadsheet operations
* h2 database
* Maven as project management tool
### Installation
1. Clone the repository to your local machine using the following command:

' git clone https://github.com/erhanerogluant/challenge.git'

2. Navigate to the cloned repository directory:

``` 
cd challenge
```

3. Build the project using Maven:
```
mvn clean install 
```

4. Run the application:

```
mvn spring-boot:run'
```

### Usage
The REST API provides 4 methods for basic CRUD functionality for Employee entities:

### POST createRecord
This method takes the byte content of the spreadsheet, parses it, and inserts each row into the database as a new record.

Request

'POST /employee'

Body
```
{
	"name": "John",
	"surname": "Doe",
	"age": 33,
	"salary": 10000,
	"workYears": 5,
	"title": "System Administrator"
}
```
Response
'200 OK'
### POST updateRecord
This method takes a JSON object representing a record in the database and updates the record whose ID matches the id in the JSON object.

Request

'POST /employee/{id}'

Body
```
{
	"name": "Jane",
	"surname": "Doe",
	"age": 33,
	"salary": 10000,
	"workYears": 5,
	"title": "System Administrator"
}
```
Response
'200 OK'

### POST deleteRecord
Endpoint: /api/employee/{id}
Method: DELETE
This method takes an ID as an integer and deletes the record from the database with the matching ID.

### GET readRecord
''' Endpoint: /api/employee/{id}
Method: GET
This method takes an ID as an integer and fetches the record from the database with the matching ID.
'''

### Functionality and Limitations:

* The API is designed to handle basic CRUD operations on employee records stored in a database. 

* The API is designed to accept spreadsheet documents and parse the data to insert records into the database.

* The API is limited to processing spreadsheets in the .xlsx format.

* The API does not handle multiple spreadsheets in a single request.

* The API does not handle invalid data in the spreadsheet, such as incorrect column names, missing data, etc.

### Discuss potential improvements:

* Provide advanced functionality for searching and filtering records.
* Add support for multiple types of records, such as Customer records or Order records.
* Add the ability to import and parse other types of documents, such as CSV or XML files.
* Improve error handling and provide more detailed error messages in case of failure.
* Add security features, such as authentication and authorization, to secure access to the web service.
* 
### Conclusion:

In conclusion, the simple CRUD web service with Spring Boot provides a basic framework for managing Employee records by conducting basic CRUD operations on a database. Although the service has some limitations, it provides a foundation for further development and improvements. With the implementation of additional functionality and improvements, the service could be further enhanced to meet the requirements of a more complex use case.

### Deployment:

To deploy the web service, you can follow the steps below:

1. Clone the repository to your local machine.
2. Navigate to the project directory using a terminal or command prompt.
3. Run the command "mvn clean install" to build the project.
4. Run the command "java -jar target/SimpleCrudService-0.0.1-SNAPSHOT.jar" to start the web service.
5. Use a tool like Postman to test the API by sending REST requests to the endpoint.

Note: Before deploying the web service, make sure to have Java 8 or higher installed on your machine and that the h2 database is properly configured.

### Contributing

Contributions are welcome. Feel free to submit a pull request.

![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)
