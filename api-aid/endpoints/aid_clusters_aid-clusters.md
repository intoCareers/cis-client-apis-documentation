# Aid Clusters

## Description
Aid clusters provides an index of cluster descriptions.  Clusters are grouping of Aid Items based on specified criteria such as Aid Based on Academics, Aid Based on Leadership, ect.

## Swagger Link
https://services.intocareers.net/swagger/aid#/Aid_Clusters/get_api_v1_aid_clusters

## State Scoping

The response is scoped to the state(s) used at JWT creation time.  A states base filter keys "extend" the base intoCareers keys.  Due to this extending, providing multiple states with your JWT will result in keys that effectively are duplicated between states.

## Example Aid Cluster

```javascript
  {
    "subSections": [
      {
        "type": "flyover",
        "text": "These scholarships are based on your hobbies, talents, or interests."
      }
    ],
    "clusterId": 799001,
    "title": "Aid Based on Hobbies, Talents, and Interests"
  }
```

------------
#### subSections
Description:  This is an array of possible descriptors for the cluster.  Currently this is limited to the flyover element.
Properties:
````
type = string; // This is a suggested display type for the descriptor.
text = string; // This is the descriptive copy text for the aid cluster
````
------------
#### clusterId
Description: Unique id for the cluster.
------------
#### title
Description: Copy text for the cluster