# The Client Needs To Display The Questions And Responses

Description: The client needs to get the Questions and the Options(Responses) from API by using JWT.

## Sequence

- [ ] At First client need to get the Questions from ````GET /api/v1/assessment/ae/questions```` endpoint.
- [ ] In Parallal client need to hit ````GET /api/v1/assessment/ae/responses```` to get the Responses(Options of Question).
- [ ] In Parallal client need to hit ````GET /api/v1/assessment/ae/pageText```` to get the All pages text.
- [ ] Above two API results will be mapped respectively in UI.



````
sequenceDiagram
    
    participant Client
    participant GET /ae/pageText
    participant GET /ae/questions
    participant GET /ae/responses
    Client->>GET /ae/pageText: Request for All pages text    
    GET /ae/pageText-->> Client: Get all the texts to display in screen
    Client->>GET /ae/questions: Request for the Questions List
    GET /ae/questions-->>Client:Get the List of questions
    Client->>GET /ae/responses: Request for the Response texts.
    GET /ae/responses-->>Client:Get Responses(Question's Options)
    
    [ NEXT PAGE ]
````
