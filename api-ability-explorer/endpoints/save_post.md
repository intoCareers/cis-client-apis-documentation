# SAVE

## Description
Save a set of answers before the assessment has been completed.  Oftentimes the user will wish to save mid-assessment.

### TX Event
This is not a TX event causing request.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/Scoring/post_api_v1_assessment_ae_save_to__restoreKey_


## Example Save

```javascript
{
  "restoreKey": "602727b1126a1600309e2fb7",
  "txCount": 1
}
```

------------
#### restoreKey:
Description: See [See restore-key](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/user-input/restore-key.md)

This restoreKey is used to use this answerSet to score or save over again.

------------
#### txCount:
Description: This represents the number of times a "transaction" event has happened for the client.

