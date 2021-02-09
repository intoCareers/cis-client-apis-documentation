# Filter Keys

## Description
Filter keys are objects used to provide the desriptors related availible topic filters for the aid items in order to filter items that are members of the desired topic "bucket".

## Swagger Link
https://services.intocareers.net/swagger/aid#/Filter_Keys/get_api_v1_aid_keys_filter__topicID_

## State Scoping

The response is scoped to the state(s) used at JWT creation time.  A states base filter keys "extend" the base intoCareers keys.  Due to this extending, providing multiple states with your JWT will result in keys that effectively are duplicated between states.

## Example filter keys

### Topic Not Specified Key

All filter keys will have an "omit" option to represent the Not Specified "Bucket".  This key conveys the intention to include items that have no specified filter key for the topic.  For example, the object below is the Not Specified key for Gender topic.  This would return all aid items that have not been specified as male or female for the gender topic.

```javascript
  "keys": [
    {
      "language": "en",
      "stateAbbr": "UT",
      "sequenceKey": 0,
      "topicID": 1,
      "topicKey": "omit1",
      "topicLabel": "Gender (excluded)"
    },
    ...
  ]
```

### Topic Filter Keys

All other keys are used to filter for the aid items that match the desired "bucket".  For example, here are the keys for men and women "buckets" under the gender topic.
```javascript
  {
    "language": "en",
    "stateAbbr": "UT",
    "sequenceKey": 10,
    "topicID": 1,
    "topicKey": "men",
    "topicLabel": "Men"
  },
  {
    "language": "en",
    "stateAbbr": "UT",
    "sequenceKey": 20,
    "topicID": 1,
    "topicKey": "women",
    "topicLabel": "Women"
  }
]
```