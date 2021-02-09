# Accessing Aid Item With Copy Text And Clusters

Description: As in [aid item user story 1](/aid_api/user-story-aid-item-1), The client needs to display an aid item including the Clusters related to this aid item.

Requirements:
- [ ] Aid Item ID

## Sequence:
- [ ] Retrieve Copy Text sections for the given aid item element from ````GET /aid/copytext/{aidID}````. [Copy Text Endpoint Readme](/aid-api/endpoints/copy_text_copytext_aidID.md).
- [ ] Retrieve Sort Type sections for the given aid item element from ````GET /aid/copytext/{aidID}````. [Copy Text Endpoint Readme](/aid-api/endpoints/copy_text_copytext_aidID.md).

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
