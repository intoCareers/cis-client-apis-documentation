The JWT (JSON Web Token) is an generated access token for 3rd party clients organizations to use the client apis.  Generally, the JWT will be passed in each request to the APIs in the request header.  In standalone application, the JWT is passed in via the URL used to "load" the application.

# Manually Creating A JWT

- [ ] Navigate to https://qa.services.intocareers.net/
- [ ] Select an API
- [ ] Select the /auth/token/create endpoint.  For Ability Explorer that would be https://qa.services.intocareers.net/swagger/assessments-ability-explorer#/auth/post_auth_token_create
- [ ] Select ‘try out’, then ‘edit’ and enter in your request body explained below.
- [ ] Select ‘execute’ and observe the JWT will be returned.
- [ ] Note: When implementing this for stand-alone modules, the JWT will be created using the same endpoint route.   The request sent to the create endpoint will need to be mirrored on the backed of your server using your credentials to create the url described below.


## Example Create Request:

````
  "client_id": "YOUR_ID"
  "client_secret": "YOUR_SECRET"
  "stateAbbr": "IC"
  "tokenTime": 30,
  "ipaddress": "string",
  "scope": 
    "programs:read",
    "schools:read",
    "occupations:read",
    "industry:read",
    "assessment:all"
  ],
  "user": {
    orgId,
    orgName,
    id: res.locals.jwt.clientUserId,
  }
````

### client_id
    type: String
    description: The client id is provided to your orginization by intocareers to uniquly identify your org.
### client_secret
    type: String
    description: The client secret is provided to your organization by intocarers as a guarded secret so other clients may access the cis apis with your credentials.  This must not be exposed in the front end application.
### stateAbbr
    type: String
    description: Scopes the responses to the state provided.  Only states scoped to a client will be allowed.
### tokenTime
    type: number
    description: TTL for the token.
### ipdadress
    type: String
    description: ipaddress used for tracking purposes
### scope
    type: Array<String>
    description:  Array of access scopes used to give access to specific api modules.  See Scopes.md for mor inforatmion.
    example values:
        "programs:read", -- Used to request access to programs api.
        "schools:read",  --  Used to request access to programs api.
        "occupations:read",  --  Used to request access to programs api.
        "industry:read",  --  Used to request access to programs api.
        "abilityexplorer:read", --  Used to request access to AE assessment api.
        "assessment:all"  --  Used to request access to all assessment apis to which the client has been given access.

### user
    type: Object
    description: Used by the client to link assessments with users from "their system".  See Client User for more information.
