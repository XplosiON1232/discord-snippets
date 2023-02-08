# All snippets
Raw snippets, no explanation.

### Enable Developer Tools
```json
"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true
```

### Get Account Token
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m=>m?.exports?.default?.getToken!==void 0).exports.default.getToken()
```

### Login Using Token
```js
function login(token){setInterval(()=>{document.body.appendChild(document.createElement`iframe`).contentWindow.localStorage.token =`"${token}"`}, 50);setTimeout(()=>{location.reload();},2500);}      
login('TOKEN HERE')
```

### Generate Friend Code
```js
webpackChunkdiscord_app.push([[[Math.random()]],{},q=>Object.values(q.c).find(e=>e.exports?.Z?.createFriendInvite).exports.Z.createFriendInvite().then(console.log)])
```

### Enable Experimental Features
```js
webpackChunkdiscord_app.push([["wp_isdev_patch"], {}, r => cache=Object.values(r.c)]);var UserStore = cache.find(m =>m?.exports?.default?.getCurrentUser).exports.default;var actions = UserStore._dispatcher._actionHandlers._orderedActionHandlers["CONNECTION_OPEN"];var user=UserStore.getCurrentUser();actions.find(n => n.name === "ExperimentStore").actionHandler({type: "CONNECTION_OPEN", user: {flags: user.flags |= 1}, experiments:[],});actions.find(n => n.name === "DeveloperExperimentStore").actionHandler();webpackChunkdiscord_app.pop(); user.flags &= ~1; "done";
```

### Client Sided Nitro
```js
webpackChunkdiscord_app.push([[[Math.random()]],{},q=>Object.values(q.c).find(e=>e.exports?.default?.getCurrentUser).exports.default.getCurrentUser().premiumType=2])
```

### Fake Mute/Deafen
```js
var text=new TextDecoder("utf-8");WebSocket.prototype.original=WebSocket.prototype.send;WebSocket.prototype.send=function(data){if(Object.prototype.toString.call(data)==="[object ArrayBuffer]"){if(text.decode(data).includes("self_deaf")){data=data.replace('"self_mute":false',"cherry")}}WebSocket.prototype.original.apply(this,[data])};
```
