## Environment:
- Java version: 1.8
- Maven version: 3.*
- Spring Boot version: 2.2.1.RELEASE

## Read-Only Files:
- src/test/*

## Data:
Sample example of JSON data object:
```json
{
   "id": 1,
   "name": "Foo Bar",
   "mobile": "987465238",
}
```

## Requirements:
There is a tiny `Contact Management System` and for this problem its scope is limited to just maintaining person name and mobile number into database.
Following architectural components for this application have already been provide as a standard Java classes:

* `ContactController`: controller class where you have to define REST endpoints for POST and GET methods
* `ContactService`: service class expected to be used by controller class to save/retrieve contacts to/from repository
* `ContactRepository`: repository class expected to be used by service class to save/retrieve contacts to/from database
* `Person`: Model class to hold the contact information

Your task is:
1. Annotate these classes using appropriate spring boot stereotypes
2. Define following 2 REST endpoints in controller class

`POST` request to `/contact/save`
* expects a valid person data object as its body payload, except that it does not have an id property; you can assume that the given object is always valid
* adds the given object to the database and assigns a unique integer id to it
* the response code is 201 and the response body is the created record, including its unique id

`GET` request to `/contact/retrieve/{id}`
* the response code is 200 and the response body is the matching object
* expect that the requested id exists in the database

Here you need to complete the given project so that it passes all the test cases when running the provided unit tests. The project by default supports the use of the H2 database.





