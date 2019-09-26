# Accessing Aid Item With Copy Text And Sort Type Sections

Description: As in [aid item user story 1](/aid_api/user-story-aid-item-1), The client needs to display an aid item including all of the meta information related to the "buckets" to which the aid item belongs.

Requirements:
- [] Aid Item ID

## Sequence:
- [] Retrieve copy text for the given aid item element from GET /aid/copytext/{aidID}. [Copy Text Endpoint Readme](/aid_api/copy_test_copytext_aidID.md).
    - [] Use the base GET /aid get request to retrieve first 25 items
- [] If filterable meta information requested then use 

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
