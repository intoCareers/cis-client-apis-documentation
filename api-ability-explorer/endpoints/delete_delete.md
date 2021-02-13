# DELETE

## Description
Delete Request that removes the answer set from being returned to the front-end when viewing the list

### DELETED ANSWERS
In the database the status for the answer set is changed to 0.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/History/delete_api_v1_assessment_ae_delete_from__restoreKey_


## Example Delete

```javascript
{
  "restoreKey": "5d287cd1a99c4e002364b219",
  "txCount": 130
}
```

------------
#### restoreKey:
Description: See [See restore-key](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/user-input/restore-key.md)

------------
#### txCount:
Description: This represents the number of times a "transaction" event has happened for the client.

