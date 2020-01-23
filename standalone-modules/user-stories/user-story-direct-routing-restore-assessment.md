# Direct Routing -- Restoring An Assessment

## Example diect routing to assessment
https://apps.intocareers.net/init/app/AbilityExplorer/$$JWT$$?moduleroute={YOUR_URL_SAFE_ROUTE}
 
There is some complexity in creating the YOUR_URL_SAFE_ROUTE component of the above url to restore assessments.  Complete and Incomplete assessment end up having different routes as completed assessments take you to a result page, but incomplete assessments take you to the next question you need to answer.
 
This means as the assessment list is being looping through to create a url href to directly route to a previously taken assessment, to you will need to check if it is a complete or incomplete assessment and create a link url (href) based on the following structure.  Remember, you’ll also have to url safe encode the module route as it is being passed as query param.
 
### Restore Routes -- Non-URL Safe Version
- incomplete -- /assessment?restoreKey=5ce5b78efe0bfa00211c7589
- completed -- /result/5ce783b462947e003d870129
 
### Restore Routes (same as above) -- URL Safe version
- incomplete -- %2Fassessment%3FrestoreKey%3D5ce5b78efe0bfa00211c7589
- completed -- %2Fresult%2F5ce783b462947e003d870129
 
An example final link for the incomplete assessment 3D5ce5b78efe0bfa00211c7589 would be:
 
https://apps.intocareers.net/init/app/AbilityExplorer/$$JWT$$?moduleroute=%2Fassessment%3FrestoreKey%3D5ce5b78efe0bfa00211c7589