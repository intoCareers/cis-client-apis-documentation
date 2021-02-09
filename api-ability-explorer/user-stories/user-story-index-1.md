# The Client Needs To Display The Questions And Responses

Description: The client needs to get the Questions and the Options(Responses) from API by using JWT.

## Sequence

- [ ] At First client need to get the Questions from ````GET /api/v1/assessment/ae/questions```` endpoint.
- [ ] In Parallal client need to hit ````GET /api/v1/assessment/ae/responses```` to get the Responses(Options of Question).
- [ ] In Parallal client need to hit ````GET /api/v1/assessment/ae/pageText```` to get the All pages text.
- [ ] Above two API results will be mapped respectively in UI.

![Alt text](/api-aid/assets/user-story-index-1.png?raw=true)

````
sequenceDiagram
    participant Client
    participant GET /aid
    participant GET /aid/{page}
    participant DONE
    Client->>GET /aid: Get First Page Of Aid Index
    Note right of GET /aid: See  <br/>aid_index_aid_get.md
    Client->>GET /aid/{page}: [ NEXT PAGE ] Need To Display More Aid Items?
    loop NEXT PAGE Yes
        GET /aid/{page}->>GET /aid/{page}: Get next page of aid index
    end
    GET /aid/{page}-->>DONE: [ NEXT PAGE No ]
````
