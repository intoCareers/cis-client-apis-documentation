# SAVE NOTES TO

## Description
An endpoint used to directly save user notes when not in the context of the assessment.

### Other Context
There was a 3rd party request to have an endpoint to save notes when viewing their assessments when not in the assessment.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/History/post_api_v1_assessment_ae_save_notes_to__restoreKey_


## Example Delete

```javascript
{
  "restoreKey": "5d287cd1a99c4e002364b219",
  "userNotes": "notes to be recorded.",
  "txCount": 130
}
```

------------
#### restoreKey:
Description: See [See restore-key](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/user-input/restore-key.md)

------------
#### userNotes:
Description: The notes the user sent with the request that has now been saved in the database.

------------
#### txCount:
Description: This represents the number of times a "transaction" event has happened for the client.

