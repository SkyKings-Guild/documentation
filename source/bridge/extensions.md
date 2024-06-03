# Extensions

Our bridge bots allow you to write your own extensions to add-on to the bridge bot, using the discord.py extension system.

We also have a few built-in extensions that you can use, such as the `.mutesync` extension.

## Built-in Extensions

### MuteSync

Allows you to sync guild mutes with a role in your Discord server to 
prevent people from talking in the bridge channel while muted in-game.

This extension required a Hypixel API key, as well as a SkyKings API key.

Add this extension by adding `.mutesync` to the `extensions` list in the `config.json` file.

#### Configuration

```json
{
    "mute_role": "role ID",
    "hypixel_api_key": "key",
    "skykings_api_key": "key"
}
```
Hypixel API keys can be obtained at [developer.hypixel.net/](https://developer.hypixel.net/).

You can view information on SkyKings API keys at [skykings.net/api](https://skykings.net/api/#section/Authentication).

## Adding Extensions

To add an extension, add the extension path to the `extensions` list in the `config.json` file.

```js
{
    "extensions": [
        ".mutesync",
        ".myextension.extension" // would refer to extensions/myextension/extension.py
    ]
}
```

```{warning}
Extensions are executed as Python code on your machine. 
They are not sandboxed by the bridge bot in any way, 
and will have access to your config file and anything 
else the user that ran the program has access to.

Use caution when running extensions from untrusted sources.
```

## Custom Extensions

Developers can write their own extensions as Python modules.

You can view more information on how to write your own extensions [here](/bridge/developer/index).

