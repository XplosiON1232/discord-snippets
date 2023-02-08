# Discord Snippets
Useful and fun javascript snippets for Discord! Warning! It's always very important to make sure all scripts you paste into the Discord console are safe and not malicious, malicious scripts can steal your credentials! Please cautious! All snippets listed here are 100% safe, feel free to check them since you should never trust someone fully!

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
webpackChunkdiscord_app.push([["wp_isdev_patch"], {}, r => cache=Object.values(r.c)]);var UserStore = cache.find(m =>m?.exports?.default?.getCurrentUser).exports.default;var actions = UserStore._dispatcher._actionHandlers._orderedActionHandlers["CONNECTION_OPEN"];var user=UserStore.getCurrentUser();actions.find(n => n.name === "ExperimentStore").actionHandler({type: "CONNECTION_OPEN", user: {flags: user.flags |= 1}, experiments:[],});actions.find(n => n.name === "DeveloperExperimentStore").actionHandler();webpackChunkdiscord_app.pop(); user.flags &= ~1; "done";
```

### Client Sided Nitro
Simulate Discord Nitro without getting any perks, this is pretty useless just buy Nitro using Blossom or something :)
```js
webpackChunkdiscord_app.push([[[Math.random()]],{},q=>Object.values(q.c).find(e=>e.exports?.default?.getCurrentUser).exports.default.getCurrentUser().premiumType=2])
```

### Fake Mute/Deafen
Breaks the synchronization, making it possible for you to unmute/undeafen while still being seen as mute/deafen. Make sure you're already muted/deafened when executing this script. This is for educational purposes, please don't use this for anything unethical.
```js
var text=new TextDecoder("utf-8");WebSocket.prototype.original=WebSocket.prototype.send;WebSocket.prototype.send=function(data){if(Object.prototype.toString.call(data)==="[object ArrayBuffer]"){if(text.decode(data).includes("self_deaf")){data=data.replace('"self_mute":false',"cherry")}}WebSocket.prototype.original.apply(this,[data])};
```
#### More?
Lmk if there's any more good snippets I could add :)

XplosiON#0001
