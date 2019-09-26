# Aid Index GET

## Description
Aid index provides an unfiltered paginated array of aid items with meta information about the pagination and total records availible.

## Swagger Link
https://services.intocareers.net/swagger/aid#/Aid_Index/get_api_v1_aid
https://services.intocareers.net/swagger/aid#/Aid_Index/get_api_v1_aid__page_

## State Scoping

The response is scoped to the state(s) used at JWT creation time with the base intoCareers appended after all state specific aid items.  A states base aid items DO NOT "extend" the base intoCareers keys.  Due to this, providing multiple states with your JWT WILL NOT result in duplicated aid items.

## Example Aid Index

```javascript
  "nextUrl": "/aid/2",
  "lastUrl": "/aid/113/",
  "nextPage": true,
  "totalRecords": 2805,
  "data": [
    {
      "stateAbbr": "UT",
      "aidID": 111170,
      "title": "Alpine Recovery Lodge Bi-Annual Scholarship"
    },
  ...
  ]
```

------------
#### nextUrl
Description: Meta information indicating the url needed to request the next page of aid items.
------------
#### lastUrl
Description: Meta information indicating the url needed to request the previous page of aid items.
------------
#### nextPage
Description: Meta information boolean value indicating if there is another page of aid items.
------------
#### totalRecords
Description:   Meta information raw count value indicating the total number of 
------------
#### data
Description:  This is an array of possible descriptors for the cluster.  Currently this is limited to the flyover element.
Properties:
````
type = string; // This is a suggested display type for the descriptor.
text = string; // This is the descriptive copy text for the aid cluster
````