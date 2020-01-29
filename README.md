a noflo server, with [noflo-rsf](https://github.com/rapid-sensemaking-framework/noflo-rsf) components pre-installed on it.

All noflo component libraries currently installed: 
- noflo-core
- noflo-filesystem
- [noflo-rsf](https://github.com/rapid-sensemaking-framework/noflo-rsf)
- noflo-strings

Good for connections from clients such as [flowhub](https://app.flowhub.io/) and [rsf-electron](https://github.com/rapid-sensemaking-framework/rsf-electron).

# Usage

First time:

`npm install`

Local (insecure):

`npm run startinsecure`

Production (secure)

[set up TLS](https://github.com/noflo/noflo-nodejs#securing-the-runtime-connection) using the `openssl` steps documented here... note that this just generates a self-signed certificate, and this can come with its own challenges. Connecting to it both in the browser, or from nodejs requires overriding default security settings.
> see the NODE_TLS_REJECT_UNAUTHORIZED comments [here](https://github.com/rapid-sensemaking-framework/rsf-electron#noflo-runtime)
> if trying to use flowhub... navigate directly to the site of the 'insecure' websocket and then authorize it. if you don't do this, it will reject the connections

Modify the environment variables in `./start` script file, according to the section below.

Then, you can run `npm startscript`, or simply `./start`.


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
