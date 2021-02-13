# Direct Routing -- Restoring An Assessment


- [ ] Navigate to https://qa.services.intocareers.net/
- [ ] Select an API
- [ ] Select the /auth/token/create endpoint.  For Ability Explorer that would be https://qa.services.intocareers.net/swagger/assessments-ability-explorer#/auth/post_auth_token_create
- [ ] Select ‘try out’, then ‘edit’ and enter in your request body explained below.
- [ ] Select ‘execute’ and observe the JWT will be returned.
- [ ] Note: When implementing this for stand-alone modules, the JWT will be created using the same endpoint route.   The request sent to the create endpoint will need to be mirrored on the backed of your server using your credentials to create the url described below.