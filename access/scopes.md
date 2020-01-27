# Client Access Scopes        

Definition:  These are the availible access scopes for intoCareers servcies api.  Clients will be given individual scopes per their negotiated access level.

Omni Scope: These special scopes are meta scopes that will, when used by the client at JWT creation time, grant all availible scopes under the related scope type.


## Admin Scopes

### Client Admin
Description:  Grants scoped access to the client admin level related endpoints.  Some of these include bulk access to user input.
````
        {
            "authorized" : true, 
            "type" : "admin", 
            "permission" : "admin:read"
        } 
````

## Information / Content Scopes
Description These scopes allow access to content related APIs

### Aid
Description:  Grants scoped access to the aid assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "aid:read"
        }
````

### Industry
Description:  Grants scoped access to the industry api endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "industry:read"
        } 
````

### Occupations
Description:  Grants scoped access to the occupations api endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "occupations:read"
        },
````

### Occupation Details
Description:  Grants scoped access to the occupation detailed endpoint.  Some clients do not have full access to our occupation data.  Generally used by the occupation library and assessments.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "occDetails:read"
        },
````

### Schools
Description:  Grants scoped access to the schools api endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "schools:read"
        },
````

### Programs
Description:  Grants scoped access to the programs api endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "programs:read"
        } 
````

## Assessment Scopes

### Assessments OMNI Scope
Description:  Grants scoped access to all assessment scopes availible to the client.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "assessments:read"
        } 
````

### Ability Explorer
Description:  Grants scoped access to the ae assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "ae:read"
        } 
````

### Career Cluster Inventory Adult
Description:  Grants scoped access to the cciAdult assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "cciAdult:read"
        } 
````



### Career Cluster Inventory Quick Pick
Description:  Grants scoped access to the cciQuick assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "cciQuick:read"
        } 
````

### Reality Check
Description:  Grants scoped access to the realityCheck assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "realityCheck:read"
        } 
````

### Interest Profiler
Description:  Grants scoped access to the interestprofiler assessment endpoints.
````
        {
            "authorized" : true, 
            "type" : "information", 
            "permission" : "interestprofiler:read"
        } 
````

## Other Scopes

### Course Planner
Description:  Grants scoped access to the course planner tool endpoints.
````
        {
            "authorized" : true, 
            "type" : "assessment", 
            "permission" : "courseplanner:read"
        } 
````

