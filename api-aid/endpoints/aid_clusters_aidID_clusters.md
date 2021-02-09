# Aid Item Cluster

## Description
Provides an array of cluster ids for the given aid item.

## Swagger Link
https://services.intocareers.net/swagger/aid#/Copy_Text/get_api_v1_aid_copytext__aidID_

## State Scoping

The response is scoped to the state(s) used at JWT creation time.  Because the aid id is provided, only aid items that are scoped to the state in the JWT will be returned.  Requesting an aid item from another state will return an empty response.

## Example Aid Item Clusters Element

```javascript
  {
    "clusterID": [
      800000,
      799068,
      799072
    ]
  }
```

------------
#### clusterID
Description:  This is an array of the clusterIDs associated with the given aidID.