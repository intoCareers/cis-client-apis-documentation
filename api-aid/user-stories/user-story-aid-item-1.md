# Accessing Aid Item With Copy Text Sections

Description: The client needs to display an aid item.  Generally the client will access this via an index table.

Requirements:
- [ ] Aid Item ID

## Sequence:
- [ ] Retrieve copy text sections for the given aid item element from ````GET /aid/copytext/{aidID}````. [Copy Text Endpoint Readme](/api-aid/endpoints/copy_text_copytext_aidID.md).

![Alt text](/api-aid/assets/user-story-aid-item-1.png?raw=true)

````
sequenceDiagram
    participant Client
    participant GET /aid/copytext/{aidID}
    participant DONE
    Client->>GET /aid/copytext/{aidID}: Get Copy Text Sections Of Aid Item
    Note right of GET /aid/copytext/{aidID}: See  <br/>aid_index_aid_get.md
    GET /aid/copytext/{aidID}-->>DONE: [ NEXT PAGE No ]
````
