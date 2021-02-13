# RESTORE FROM

## Description
Retrieve the answers for a previously taken assessment.

### TX Event
This is not a TX event causing request.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/Scoring/get_api_v1_assessment_ae_restore_from__restoreKey_


## Example Delete

```javascript
{
  "answers": "5,5,5,5,4,4,4,4,3,3,3,4,4,4,2,2,3,4,4,3,3,3,3,3,3,3,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4,4,4,5,5,5,5,5,5,5,5,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4",
  "completed": true,
  "txCount": 131
}
```

------------
#### answers:
Description: A comma seperate string value of the answers stored in this answer set.

------------
#### completed:
Description: Same as done in the list endpoint.  There may have been a reason why it was named completed here for a client reason.

------------
#### txCount:
Description: This represents the number of times a "transaction" event has happened for the client.

