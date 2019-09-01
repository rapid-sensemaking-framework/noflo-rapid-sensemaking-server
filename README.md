a noflo server, with rsf components pre-installed on it. Ready for use with Heroku

# Usage

First time:

`npm install`

`npm run init`

Following times:

`npm start`


Expects environment variables to be set:
`PORT`: the port on which to run the websocket server.
`TOP_SECRET`: an arbitray secret which will provide a layer of authentication between a noflo client, such as flowhub or noflo-rsf-client, and the server.
