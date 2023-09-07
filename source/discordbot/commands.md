# Commands

This page outlines the commands the bot has, and how to use them.

```{note}
Options surrounded in (parentheses) are required, while options surrounded by [brackets] are optional.
```

```{note}
Options with the `player` type will accept both a 
Minecraft username or the Discord user ID of a verified player.

If optional and not provided, they will use the command author's verified account if one is linked.
```


## Skyblock

### `/lookup player [player]`

Checks if a Minecraft player is flagged as a scammer, IRL trader, macroer, or ratter in our database.

This will also check their Discord account if they are verified.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description          | Type   |
| ------ | -------------------- | ------ |
| player | The player to check. | Player |
```

### `/lookup user [user]`

Checks if Discord user is flagged as a scammer, IRL trader, macroer, or ratter in our database.

This will also check their Minecraft account if they are verified.

```{table}
:width: 100%
:widths: auto
:align: center

| Name | Description        | Type |
| ---- | ------------------ | ---- |
| user | The user to check. | User |
```

### `/lookup guild [guild]`

Checks through a whole guild to see if its members are flagged as 
scammers, IRL traders, macroers, or ratters in our database.

This will also check their Discord account if they are verified.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description         | Type  |
| ----- | ------------------- | ----- |
| guild | The guild to check. | Guild |
```

### `/report`

Sends a link for you to report a scammer, IRL trader, macroer, or ratter.

### `/xpbottles`

Provides a list of experience bottles that give the most experience per coin.

### `/fetchur`

Provides you with today's Fetchur item.

### `/bestcrop`

Provides a list of crops that sell for the most on the bazaar.

### `/baz-to-npc`

Provides a list of items that can be bought from the Bazaar and sold to NPCs for profit.

### `/npc-to-baz`

Provides a list of items that can be bought from NPCs and sold to the Bazaar for profit.

### `/bazaar (item)`

Views an item on the Bazaar.

For a more detailed and easier to use view, you can visit our [Bazaar Tracker](https://skykings.net/bazaar).

```{table}
:width: 100%
:widths: auto
:align: center

| Name | Description                     | Type |
| ---- | ------------------------------- | ---- |
| item | The item to view on the bazaar. | Text |
```

### `/auctions search (item) [bin]`

Searches the auction house for an item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description                                             | Type    |
| ----- | ------------------------------------------------------- | ------- |
| item  | The item to search for.                                 | Text    |
| bin   | Filters only BIN auctions. Leave blank for all options. | Boolean |
```

### `/auctions player (player)`

Searches the auction house for an item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                      | Type   |
| ------- | -------------------------------- | ------ |
| player  | The player to view auctions for. | Player |
```

### `/auctions lowestbin (item)`

Finds the lowest BIN auction for an item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description                                | Type    |
| ----- | ------------------------------------------ | ------- |
| item  | The item to search for.                    | Text    |
| exact | Match `item` exactly. Defaults to `false`. | Boolean |
```

### `/price (item)`

Finds the lowest BIN auction for an item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description                                | Type |
| ----- | ------------------------------------------ | ---- |
| item  | The item to search for.                    | Text |
```

### `/bits-to-bin`

Provides a list of items that can be bought with bits and sold for profit.

### `/organic-matter`

Provides a list of items that that provide organic matter and can be bought from the Bazaar.

### `/skyblock collections`

Provides a informations on all the Skyblock collections.

### `/skyblock skills`

Provides a informations on all the Skyblock skills.

### `/skyblock item (item)`

Provides information on a Skyblock item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name | Description               | Type |
| ---- | ------------------------- | ---- |
| item | The item to view info on. | Text |
```

### `/skyblock wiki (search)`

Searches for an article on the official [Hypixel Skyblock Wiki](https://wiki.hypixel.net).

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description              | Type |
| ------ | ------------------------ | ---- |
| search | The query to search for. | Text |
```

### `/skyblock time`

Shows the current in-game time.

### `/skyblock mayor`

Shows the current Skyblock mayor, as well as the current election (if active).

### `/skyblock bingo`

Shows the current Skyblock bingo card, if active.

### `/skyblock-events config view`

Displays the server's SkyBlock event notification configuration.

### `/skyblock-events config toggle (event)`

Toggles an event notification on or off.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description          | Type |
| ----- | -------------------- | ---- |
| event | The event to toggle. | Text |
```

### `/skyblock-events config toggle-alert (event) (alert)`

Toggles an alert on or off for an event.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description          | Type |
| ----- | -------------------- | ---- |
| event | The event to toggle. | Text |
| alert | The alert to toggle. | Text |
```

### `/skyblock-events config set-ping (event) [role]`

Sets the ping role for an event notification.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description                                            | Type |
| ----- | ------------------------------------------------------ | ---- |
| event | The event to toggle.                                   | Text |
| role  | The role to set as a ping role. Leave blank to remove. | Role |
```

### `/leaderboard players (leaderboard) [guild]`

Displays the rankings of players from our [Skyblock leaderboard](https://skykings.net/player-leaderboard).

If a guild is provided, only that guild will be shown.

```{table}
:width: 100%
:widths: auto
:align: center

| Name        | Description                                            | Type |
| ----------- | ------------------------------------------------- | ---- |
| leaderboard | The leaderboard to show.                          | Text |
| guild       | The guild to filter by. Leave blank for no guild. | Text |
```

### `/leaderboard add-guild (guild)`

Adds a guild to our [Skyblock leaderboard](https://skykings.net/leaderboard).

The guild must have at least 50 members.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description       | Type |
| ----- | ----------------- | ---- |
| guild | The guild to add. | Text |
```

### `/calculate skill (player) (target_level)`

Calculates how much skill XP you need to get for a certain level.

```{table}
:width: 100%
:widths: auto
:align: center

| Name         | Description                   | Type           |
| ------------ | ----------------------------- | -------------- |
| player       | The player to calculate with. | Text           |
| target_level | The target level.             | Integer (1-60) |
```

### `/calculate slayer (player) (target_level)`

Calculates how much slayer XP you need to get for a certain level.

```{table}
:width: 100%
:widths: auto
:align: center

| Name         | Description                   | Type          |
| ------------ | ----------------------------- | ------------- |
| player       | The player to calculate with. | Text          |
| target_level | The target level.             | Integer (1-9) |
```


## Hypixel

### `/locate [player]`

Locates a player on Hypixel.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description           | Type   |
| ------ | --------------------- | ------ |
| player | The player to locate. | Player |
```

### `/friends [player]`

Lists a player's friends on Hypixel.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description           | Type   |
| ------ | --------------------- | ------ |
| player | The player to locate. | Player |
```

### `/guild info (guild)`

Shows information about a guild in Hypixel.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description           | Type |
| ----- | --------------------- | ---- |
| guild | The guild to display. | Text |
```

### `/guild members (guild)`

Shows a list of members in a guild.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description           | Type |
| ----- | --------------------- | ---- |
| guild | The guild to display. | Text |
```

### `/guild xp (guild) (gexp)`

Shows a list of members in a guild that are under a certain guild XP threshold.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description             | Type   |
| ----- | ----------------------- | ------ |
| guild | The guild to display.   | Text   |
| gexp  | The guild XP threshold. | Number |
```

### `/guild members (guild)`

Shows a list of members in a guild that are either not verified with the bot or not in the DIscord server.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description           | Type |
| ----- | --------------------- | ---- |
| guild | The guild to display. | Text |
```

### `/status`

Displays Hypixel's current server status, as shown on [status.hypixel.net](https://status.hypixel.net).

### `/userinfo (user)`

Shows information about a Discord user.

```{table}
:width: 100%
:widths: auto
:align: center

| Name | Description          | Type |
| ---- | -------------------- | ---- |
| user | The user to display. | User |
```

### `/guildrequirements [player]`

Shows whether or not someone meets the requirements for the Discord server's guilds.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description          | Type   |
| ------ | -------------------- | ------ |
| player | The player to check. | Player |
```


## Stats

### `/player [player]`

Shows information about a player on Hypixel.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/profiles [player]`

Shows a player's Skyblock profiles.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/guildrequirements [player]`

Shows whether or not someone meets the requirements for the Discord server's guilds.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/slayers [player]`

Shows a player's slayer statistics.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/skills [player]`

Shows a player's skills.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/collections [player]`

Shows a player's collections.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/weight [player]`

Shows a player's weight. This can show both Senither and Lily weight.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/networth [player]`

Shows a player's networth.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/dungeons info [player]`

Shows a player's general Dungeon statistics.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/dungeons best-runs (floor) [player]`

Shows the best Dungeon runs for a specific floor from a player.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| floor  | The floor to show.  | Text   |
| player | The player to show. | Player |
```

### `/bank [player]`

Shows a player's bank, including balance and transaction history.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/bingo card [player]`

Shows a player's bingo card.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/bingo stats [player]`

Shows a player's bingo stats.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/bingo card [player]`

Shows a player's bingo card.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/crimson [player]`

Shows a player's Crimson Isle statistics.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/bestiary [player]`

Shows a player's bestiary.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/jacob [player]`

Shows a player's Jacob's Contest statistics.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/accessories [player]`

Shows a player's accessories, including missing accessories and possible upgrades.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/forge profits [player]`

Shows the best items you can forge for a profit.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/forge view [player]`

Shows the items a player is currently forging.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/harp [player]`

Shows a player's harp statistics, such as what songs they have completed.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

### `/museum featured [player]`

Shows a player's featured museum items.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```

## Verification

### `/verify link (player)`

Links your Discord account to your Minecraft account.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description            | Type   |
| ------ | ---------------------- | ------ |
| player | The player to link to. | Player |
```

### `/verify help`

Provides instructions for verifying.


### `/verify sync`

Updates your roles in the current Discord server.


### `/verify unlink`

Unlinks your Discord account from your Minecraft account.


### `/verify button [channel]`

Sends a verification button to the specified channel, or the current one if none is specified.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| channel | The channel to send the button to. | Channel |
```


## Config

### `/config view`

Views the server's configuration settings.


### `/config edit (option) [value]`

Edits the server's configuration settings. Leave `value` blank to reset the option to its default value.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| option  | The option to edit.                | Text    |
| value   | The value to set the option to.    | Any     |
```

### `/config guilds view`

Views the server's linked guilds.


### `/config guilds add-guild (guild)`

Add a Hypixel guild to the server's linked guilds.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild to add.                  | Text    |
```

### `/config guilds remove-guild (guild)`

Remove a Hypixel guild from the server's linked guilds.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild to remove.               | Text    |
```

### `/config guilds edit-guild (guild) (option) [value]`

Edits a guild's settings. Leave `value` blank to reset the option to its default value.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild to edit.                 | Text    |
| option  | The option to edit.                | Text    |
| value   | The value to set the option to.    | Any     |
```

### `/config guilds add-rank (guild) (rank) [role]`

Add a rank to a guild's settings, optionally with a role to add to members with the rank.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild the rank is in.          | Text    |
| rank    | The rank to add.                   | Text    |
| role    | The role to sync the rank with.    | Role    |
```

### `/config guilds edit-rank (guild) (rank) [role]`

Updates a rank's role. Leave `role` blank to remove the role from the rank.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild the rank is in.          | Text    |
| rank    | The rank to edit.                  | Text    |
| role    | The role to sync the rank with.    | Role    |
```

### `/config guilds remove-rank (guild) (rank)`

Remove a rank from a guild's settings.

```{table}
:width: 100%
:widths: auto
:align: center

| Name    | Description                        | Type    |
| ------- | ---------------------------------- | ------- |
| guild   | The guild the rank is in.          | Text    |
| rank    | The rank to remove.                | Text    |
```


## Events

### `/event start (event) (duration) [gvg] [channel] [role] [schedule_event]`

Remove a rank from a guild's settings.

```{table}
:width: 100%
:widths: auto
:align: center

| Name           | Description                                                                                    | Type    |
| -------------- | ---------------------------------------------------------------------------------------------- | ------- |
| event          | The type of event to start.                                                                    | Text    |
| duration       | How long the event should last. Should be in a format similar to `1w 1d`.                      | Text    |
| gvg            | Whether the event should be a Guilds vs Guilds event. [SkyKings Premium](/premium) is required. | Boolean |
| channel        | The channel to send the event message to.                                                      | Channel |
| role           | The role to ping when the event starts.                                                        | Role    |
| schedule_event | Whether the event should be scheduled using Discord's events feature.                          | Boolean |
```

### `/event end`

Ends an event.


### `/event delete`

Deletes the event data.


### `/event join`

Joins an event.


### `/event leave`

Leaves an event.


### `/event position [player]`

Shows a player's position in the current event. Defaults to yourself if `player` is not provided.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| player | The player to show. | Player |
```


### `/event list`

Lists the people in an event.


### `/event guild (guild)`

Shows a guild in the event.

```{table}
:width: 100%
:widths: auto
:align: center

| Name   | Description         | Type   |
| ------ | ------------------- | ------ |
| guild  | The guild to show.  | Text   |
```


## Miscellaneous


### `/premium info`

Shows information about [SkyKings Premium](/premium).


### `/premium status`

Shows current server's premium status.


### `/premium transfer`

Allows you to use a Premium subscription on a server for the duration you have the subscription.


### `/premium redeem`

Redeem a premium code for a server.

```{table}
:width: 100%
:widths: auto
:align: center

| Name | Description          | Type |
| ---- | -------------------- | ---- |
| code | The code to redeem.  | Text |
```


### `/uptime`

Shows the bot's uptime.


### `/invite`

Gives you the bot's invite so you can add it to your own servers.


### `/info`

Shows general system information about the bot.


### `/ping`

Tests if the bot is responding, and shows you the connection latency.


### `/command-usage`

Shows command usage.


### `/votes`

Shows people who have voted for the bot on top.gg. Currently nonfunctional.


### `/api-key`

Generates an API key for use with our [API](/api). Requires [SkyKings Premium](/premium).


### `/help`

Shows a list of commands.
