# r6info.js

A simple wrapper for the Rainbow Six Siege API that allows you to easily retrieve information about maps, operators, ranks, and service status.

## Installation

```sh
npm install r6info.js
```

## Getting an Access Token

Before making requests to the API, you need to obtain an access token. You can do this using the `getToken()` function:

```javascript
const { getToken } = require('r6info.js');

async function main() {
  try {
    const { token, expiresIn, callDateTime, callId, APIVersion } = await getToken();
    console.log('Token:', token);
    console.log('Expires In:', expiresIn);
    console.log('Call Date Time:', callDateTime);
    console.log('Call ID:', callId);
    console.log('API Version:', APIVersion);
  } catch (error) {
    console.error('Error during token request:', error.message);
  }
}

main();
```
