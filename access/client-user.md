# Client User

A "client user" can be provided at with the JWT creation to enable a client to link user input to their user internal accounts such as answer sets, favorite occs, ect.

User input can be retrieved using the User Input related endpoint provided by the respective modules API.  For example, Ability Explorer:

https://qa.services.intocareers.net/swagger/assessments-ability-explorer#/User_Input



````
  "user": {
    "orgId": "1",
    "orgName": "exampleOr",
    "id": "User1"
  }
````

### orgID
    type: String
    Description: provided by client to identify 2nd degree 3rd parties (clients of the client)
### orgName
    type: String
    Description: provided by client to identify 2nd degree 3rd parties (clients of the client)
### id
    type: String
    Description: A unique reference user id from the client system use to link user input.