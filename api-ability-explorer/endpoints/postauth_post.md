# JWT Create

## Description
If the request header has an "authenticated" JWT before then endpoint will return an authorized CLIENT API JWT.
The header JWT may or may not be a CIS CLIENT JWT. If it is a CIS CLIENT JWT then the postauth call will simply 
reflect back the jwt. If it is not a CIS CLIENT JWT (i.e. a CIS360 JWT) then postauth will return a federated 
JWT that has both the CIS CLIENT JWT and CIS360 JWT.

## Swagger Link
https://services.intocareers.net/swagger/assessments-ability-explorer#/auth/post_auth_token_postauth

## Scopes

[See Scopes](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/scopes.md)

## Example JWT

[See JWT](https://github.com/intoCareers/cis-client-apis-documentation/tree/master/access/jwt.md)
