# Accessing Filtered Aid Index For Single Topic Single Bucket

Description: The client needs to display a filtered index of aid items for all 

Requirements:
- [ ] Filter keys ````GET /aid/keys/filter/{topicID}```` [Filter Keys Endpoint Readme](/api-aid/endpoints/filter_keys_keys_filter_topicID.md)

## Sequence

- [ ] Retreive filter options from endpoints for filter keys ````GET /aid/keys/filter/{topicID}```` [Filter Keys Endpoint Readme](/api-aid/endpoints/filter_keys_keys_filter_topicID.md) and clusters ````GET /aid-clusters```` [Aid Clusters Endpoint Readme](/api-aid/endpoints/aid_clusters_aidID_clusters.md).
- [ ] Retrieve the filtered Aid Index from ````POST /aid```` [Filtered Index Endpoint Readme](/api-aid/endpoints/aid_index_aid_filter_post.md).  Provide desired filter options retrieve page 1 of filtered aid items index.
- [ ] If there are more than one "page" of aid item results and the client needs to access more filtered aid items use the ````POST /aid```` with the same filter options except page which should be itterated by 1.

![Alt text](/api-aid/assets/user-story-index-2.png?raw=true)

````
sequenceDiagram
    participant Client
    participant POST /aid
    participant DONE
    Client->>POST /aid: POST for First Page Of Filtered Aid Index
    Note right of POST /aid: See  <br/>aid_index_aid_post.md
    Client->> POST /aid: [ NEXT PAGE? ] Need To Display More Filtered Aid Items?
    loop NEXT PAGE Yes
         POST /aid->> POST /aid: Get next page of filtered aid index
    end
     POST /aid-->>DONE: [ NEXT PAGE No ]
````
