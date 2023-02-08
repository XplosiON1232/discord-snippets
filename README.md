# Discord Snippets
Useful and fun javascript snippets for Discord

## Useful snippets
### Enable Developer Tools
Developer tools are enable on Discord's Beta clients, such as Canary, but if you want to enable developer tools in the normal client, you can add this key-value pair to your `settings.json` file located at `%appdata%/discord/settings.json`. Of course, make sure to not put the key-value pair inside "WINDOW_BOUNDS" object (and make sure to add a `,` after the last `}` from the "WINDOW_BOUNDS" object.
```json
"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true
```
### Get Account Token
Use this script to get your Discord account token!
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m=>m?.exports?.default?.getToken!==void 0).exports.default.getToken()
```

### Login Using Token
To login using a discord token, use this script!
```js
function login(token) {   setInterval(() => {   document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`   }, 50);   setTimeout(() => {   location.reload();   }, 2500);   }      login('TOKEN HERE')
```

### Generate Friend Code
Can be used max 5 times, and expires after 7 days.
