a noflo server, with [noflo-rsf](https://github.com/rapid-sensemaking-framework/noflo-rsf) components pre-installed on it.

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


## Environment Variables

Expects environment variables to be set:

```
# BOT_CONFIG should include configurations which make the config expected by rsf-telegramable,
# rsf-mattermostable, and rsf-smsable, keyed by `mattermostable`, `telegramable`, and `smsable`
BOT_CONFIG='{"mattermostable":"https://chat.xx@@email@email.com@@userpass@@@https://chat.yy@@user@email.com@@userpass","telegramable":{"socketUrl":"ws://localhost:3002"},"smsable":{"socketUrl":"ws://localhost:3003"}}'

# the host ip address
HOST=127.0.0.1

# the port on which to run the websocket server.
PORT=3001

# an arbitrary secret which will provide a layer of authentication between
# a noflo client, such as flowhub or noflo-rsf-client, and the server
TOP_SECRET=123jkad9s
