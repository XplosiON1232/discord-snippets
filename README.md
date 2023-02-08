# Discord Snippets
Useful and fun javascript snippets for Discord

### Enable Developer Tools
Developer tools are enable on Discord's Beta clients, such as Canary, but if you want to enable developer tools in the normal client, you can add this key-value pair to your `settings.json` file located at `%appdata%/discord/settings.json`. Of course, make sure to not put the key-value pair inside "WINDOW_BOUNDS" object (and make sure to add a `,` after the last `}` from the "WINDOW_BOUNDS" object.
```json
"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true
```
### Generate Friend Code
Can be used max 5 times, and expires after 7 days.
