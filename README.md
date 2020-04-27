# BBDN-Collab-Postman-REST
This repository contains a postman collection for testing the Collaborate REST APIs. In order to use this repository, you will need a key and secret. For more information on this API and how to obtain the key and secret, visit the [Blackboard Collaborate Developer Community](https://community.blackboard.com/community/developers/collaborate).

## Usage
To use this repository, you must have Postman installed. From the UI, click the import button and follow the on-screen prompts. The Collab endpoint is already configured to use https://techpreview.bbcollab.com/collab/api/csa. 

The easiest way to use this collection is to have Postman generate the JWT token before requesting an authorization token from the Collab Web Service. To do this:

1. Execute `INIT: Load Crypto Library for HS256` to load the library into your postman globals
2. Update the collection variables with the following:
	- `JWT_sub` - Your Collaborate REST API Key
	- `JWT_iss` - Your Collaborate REST API Key
	- `JWT_secret` - Your Collaborate REST API Secret
3. Execute "Token"
4. Execute other Collaborate Calls as desired

The Pre-Request script on token will generate a JWT token for use during the TOKEN request.  Once a valid authorization token is returned, the Test will assign this token to a variable so it can be re-used in future calls.  Tokens are requested with a valid period of 1h
