# LIST

## Description
Retrieve all assessments taken for the given user.

### DELETED ANSWERS
Only answers that have not been "deleted" is be returned in this answer set.

### INCOMPLETE ANSWERS
However, incomplete answer sets will display.

### DISPLAY ORDER
The display order is based on the updatedTimeStamp, not the answerSet number.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/History/get_api_v1_assessment_ae_list


## Example list

```javascript
  [
    {
      "answerSet": 118,
      "answers": "5,5,5,5,4,4,4,4,3,3,3,4,4,4,2,2,3,4,4,3,3,3,3,3,3,3,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4,4,4,5,5,5,5,5,5,5,5,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4",
      "done": true,
      "status": 1,
      "userNotes": "notes to be recorded.",
      "restoreKey": "5d287cd1a99c4e002364b219",
      "createdAt": "2019-07-12T12:28:01.154Z",
      "updatedTimeStamp": "2020-08-27T07:58:05.189Z"
    },
    ...
  ]
```

------------
#### answerSet
Description: This is an atomic number assigned to a number set.  Even when answer sets are "delete" this number will stay the same for the answer set.

------------
#### answers:
Description: A comma seperate string value of the answers stored in this answer set.

------------
#### done:
Description: A boolean value that indicates if the answer set was "scored".

------------
#### status:
Description: Status represents the deleted status in the database.

Values:
````
1 -- Active
0 -- Deleted (this will never be returned by the API, just stored in the database)
````
------------
#### userNotes:
Description: The notes provided by the user when saving the assessment.

------------
#### restoreKey:
Description: See [See restore-key](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/user-input/restore-key.md)

------------
#### createdAt:
Description: When this answer set was originally saved.

------------
#### updatedTimeStamp:
Description: Last time the answer set was saved over.
