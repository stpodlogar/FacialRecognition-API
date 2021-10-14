# FacialRecognition API
Server for the FacialRecognition app.

### ***This is the backend portion.*** The frontend can be found [here](https://github.com/stpodlogar/facial-recognition).

### Built with
  - Nodejs runtime is required. It can be downloaded [here](https://nodejs.org/en/)
  - [Express](https://expressjs.com/)
  - Encryption with [bcrypt-nodejs](https://www.npmjs.com/package/bcrypt-nodejs)

## Instructions
1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. You must add your own API Key in the `controllers/image.js` file to connect to the Clarifai API:
``` javascript
  const app = new Clarifai.App({
    apiKey: 'YOUR_API_KEY' //<-- HERE
  });
```
5. Add your own database credentials to `server.js` like so:
``` javascript
const db = knex({
  client: 'pg',
  connection: {
    host : '127.0.0.1',
    user : 'YOUR_USERNAME',
    password : 'YOUR_PASSWORD',
    database : 'smart-brain'
  }
});
```


You can grab your own Clarifai API Key [here](https://www.clarifai.com/)

** Make sure you use postgreSQL instead of mySQL for this codebase.

