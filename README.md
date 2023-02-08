# Discord Snippets
Useful and fun javascript snippets for Discord! Warning! It's always very important to make sure all scripts you paste into the Discord console are safe and not malicious, certain scripts can steal your credentials! Please cautious! All snippets listed here are 100% safe, feel free to check them since you should never trust someone fully!

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
function login(token){setInterval(()=>{document.body.appendChild(document.createElement`iframe`).contentWindow.localStorage.token =`"${token}"`}, 50);setTimeout(()=>{location.reload();},2500);}      
login('TOKEN HERE')
```

### Generate Friend Code
Can be used max 5 times, and expires after 7 days. This will generate a `discord.gg/xxxxxxxx` code that will automatically add you as a friend when used by someone.
```js
webpackChunkdiscord_app.push([[[Math.random()]],{},q=>Object.values(q.c).find(e=>e.exports?.Z?.createFriendInvite).exports.Z.createFriendInvite().then(console.log)])
```

## Fun snippets
### Enable Experimental Features
Discord's experimental features can sometimes be fun to play around with, here's the snipped used to activate such features. This will unlock a new tab that you can find in the Discord settings.
```js
Object.defineProperty((webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m=>m?.exports?.default?.isDeveloper!==void 0).exports.default,"isDeveloper",{get:()=>true});
```

### Client Sided Nitro
```js
webpackChunkdiscord_app.push([[[Math.random()]],{},q=>Object.values(q.c).find(e=>e.exports?.default?.getCurrentUser).exports.default.getCurrentUser().premiumType=2])
```
