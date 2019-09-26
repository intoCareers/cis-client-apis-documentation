# Accessing Aid Index

Description: The client needs to display the aid index on page render.

## Sequence

- [] Retrieve the first "page" of the Aid Index. [Index Endpoint Readme](/aid-api/endpoints/aid_index_aid_get.md).
    - [] Use the base GET /aid get request to retrieve first 25 items
- [] If the client needs to access more aid items use the GET /aid/{page}

![Alt text](/aid-api/assets/user-story-index-1.png?raw=true)

````
sequenceDiagram
    participant Client
    participant GET /aid
    participant GET /aid/{page}
    participant DONE
    Client->>GET /aid: Get First Page Of Aid Index
    Note right of GET /aid: See  <br/>aid_index_aid_get.md
    Client->>GET /aid/{page}: [ NEXT PAGE? ] Need To Display More Aid Items?
    loop NEXT PAGE Yes
        GET /aid/{page}->>GET /aid/{page}: Get next page of aid index
    end
    GET /aid/{page}-->>DONE: [ NEXT PAGE No ]
````
