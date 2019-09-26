# Render Aid Index

Description: The client needs to display the aid index on page render.

- [] Start by requesting the first "page" of the Aid Index (aid_index_aid_get.md).
    - [] Use the base /aid get request to retrieve first 25 items
- [] If the client needs to access more aid items use the /aid/{page}


sequenceDiagram
    participant Client
    participant aid_index_aid_get
    participant aid_index_aid_page_get
    participant Finished
    Client->>aid_index_aid_get: Get First Page Of Aid Index
    Note right of aid_index_aid_get: See  <br/>aid_index_aid_get.md
    Client->>aid_index_aid_page_get: [ NEXT PAGE? ] Need To Display More Aid Items?
    loop NEXT PAGE Yes
        aid_index_aid_page_get->>aid_index_aid_page_get: Get next page of aid index
    end
    aid_index_aid_page_get-->>Finished: [ NEXT PAGE No ]

