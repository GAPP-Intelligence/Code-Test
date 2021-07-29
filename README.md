# Full-Stack Engineer Test

In this test, you are expected to write a small web application to manage a list of department in a company. Each department has a name, set of teams, and the person in-charge. Each team has a team number, a set of people, and a team lead. 
The test consists of two parts, a RESTful API as the **backend** and the JavaScript based **frontend** application.

There is no need to create a PR back to this repository once completed, please provide a link to your project repository for review.

## Backend implementation

Use the following structure to model the data

```
class Department(Model):
    department_id: integer 
    name: string
    teams: list<team_id> (nullable)
    inCharge: <user_id>
```

```
class Team(Model):
    team_id: integer
    people: list<user_id> (nullable)
    teamLead: user_id 
```

```
class User(Model):
    user_id: integer
    name: string 
```

Implement the following API endpoints:

* **GET /departments/** - Returns a list of departments in the database in JSON format
* **GET /departments/{{id}}/** - Returns a detail view of the specified department. Including department, and team IDs in JSON format
* **GET /teams/** - Returns a list of teams in the database in JSON format
* **GET /teams/{{id}}/** - Returns a detail view of the specified team id
* **GET /users/** - Returns a list of users in the database in JSON format
* **GET /users/{{id}}/** - Returns a detail view of the specified user id
*
* **POST /departments/** - Creates a new department with the specified details - Expects a JSON body
* **POST /teams/** - Creates a new team with the specified details - Expects a JSON body
* **POST /users/** - Creates a new user with the specified details - Expects a JSON body
* 
* **PUT /departments/{{id}}** - Updates an existing department - Expects a JSON body
* **PUT /teams/{{id}}** - Updates an existing team - Expects a JSON body
* **PUT /users/{{id}}** - Updates an existing user - Expects a JSON body

You are recommended to use **MERN** stack to implement your backend and API layer, but you are free to use a different language/framework/libraries you are comfortable with.


## Frontend implementation
Implement a small frontend application to consume the API you developed above.

The frontend should be able to show a list of names of the books available in the database. Upon clicking the name of a book on the list, the user should be navigated to a more detailed view of the selected book, where they are presented with the ISBN and the author details. You should also implement two forms where the user is able to create/update authors and books (using the POST and PUT endpoints)
You are recommended to use **ReactJS** to create the frontend, but you are free to use a different JavaScript framework.

### Notes and recommendations
* The languages, frameworks and libraries mentioned are recommendations only, you are free to use whatever you are comfortable with.
* The project structure is up to you to decide
* You are recommended to use git commits in a logical manner to demonstrate the development progress
* Writing tests and adhering to development standards/conventions leaves a positive impression
