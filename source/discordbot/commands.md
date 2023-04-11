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

### `/auctions search (item) [bin] [exact]`

Searches the auction house for an item.

```{table}
:width: 100%
:widths: auto
:align: center

| Name  | Description                                             | Type    |
| ----- | ------------------------------------------------------- | ------- |
| item  | The item to search for.                                 | Text    |
| bin   | Filters only BIN auctions. Leave blank for all options. | Boolean |
| exact | Match `item` exactly. Defaults to `false`.              | Boolean |
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

## Hypixel

## Stats

## Verification

## Config

## Events

## Miscellaneous
