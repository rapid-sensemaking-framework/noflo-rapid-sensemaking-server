a noflo server, with [noflo-rsf](https://github.com/rapid-sensemaking-framework/noflo-rsf) components pre-installed on it. Ready for use with Heroku.

All noflo component libraries currently installed: 
- noflo-core
- noflo-filesystem
- [noflo-rsf](https://github.com/rapid-sensemaking-framework/noflo-rsf)
- noflo-strings

# Usage

First time:

`npm install`

Production:

`npm start`

Local (secured):

`npm run startlocal`

Local (insecure):

`npm run startinsecure`


Expects environment variables to be set:

`PORT`: the port on which to run the websocket server.

`TOP_SECRET`: an arbitrary secret which will provide a layer of authentication between a noflo client, such as flowhub or noflo-rsf-client, and the server.
