# BBDN-Collab-Postman-REST
This repository contains a postman collection for testing the Collaborate REST APIs. In order to use this repository, you will need a key and secret. For more information on this API and how to obtain the key and secret, visit the [Blackboard Collaborate Developer Community](https://community.blackboard.com/community/developers/collaborate).

## Usage
To use this repository, you must have Postman installed. From the UI, click the import button and follow the on-screen prompts. The Collab endpoint is already configured, so all you need to do is:

1. Ensure you call the ```GET INIT: Load Crypto Library for RS256``` endpoint first.
2. Call the ```GET Token``` enpoint next, ensuring that you add your key and secret to the Query Parameters.
3. You include your token in subsequent calls.