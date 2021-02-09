# Accessing Aid Item With Copy Text And Sort Type Sections

Description: As in [aid item user story 1](/aid_api/user-story-aid-item-1), The client needs to display an aid item including all of the meta information related to the sectional "buckets" to which the aid item belongs.

Requirements:
- [ ] Aid Item ID

## Sequence:
- [ ] Retrieve Copy Text sections for the given aid item element from ````GET /aid/copytext/{aidID}````. [Copy Text Endpoint Readme](/api-aid/endpoints/copy_text_copytext_aidID.md).
- [ ] Retrieve Sort Type sections for the given aid item element from ````GET /aid/sections/{aidID}````. [Copy Text Endpoint Readme](/api-aid/endpoints/copy_text_sections_aidID.md).

![Alt text](/api-aid/assets/user-story-aid-item-2.png?raw=true)

````
sequenceDiagram
    participant Client
    participant GET /aid/copytext/{aidID}
    participant GET /aid/sections/{aidID}
    participant DONE
    Client->>GET /aid/copytext/{aidID}: Get Copy Text Sections Of Aid Item
    Note right of GET /aid/copytext/{aidID}: See  <br/>aid_index_aid_get.md
    Client->>GET /aid/sections/{aidID}: Get Sort Type Sections Of Aid Item
    Note right of GET /aid/sections/{aidID}: See  <br/>aid_index_aid_get.md
    GET /aid/sections/{aidID}-->>DONE: [ DONE ]
````
