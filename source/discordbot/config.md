# Configuration

SkyKings' configuration allows you to customize the bot's behavior in your own server.

There are various different types of configuration settings.

## General & Verification Configuration

The general configuration for the bot contains various automatic annoucements and other things, and can be edited using the `/config edit` command.

```{table}
:width: 100%
:widths: auto
:align: center

| Name                        | Description                                                                                            | Type          |
|-----------------------------|--------------------------------------------------------------------------------------------------------|---------------|
| Autoreply Enabled           | Replies to certain messages that have a specific pattern in them.                                      | Boolean       |
| Hypixel Status Ping         | The role to ping for Hypixel status updates.                                                           | Role          |
| Hypixel Status Channel      | The channel to send Hypixel status updates to.                                                         | Channel       |
| Hypixel News Ping           | The role to ping for Hypixel announcements.                                                            | Role          |
| Hypixel News Channel        | The channel to send Hypixel announcements to.                                                          | Channel       |
| SkyBlock Patchnotes Ping    | The role to ping for Hypixel Skyblock patchnotes.                                                      | Role          |
| SkyBlock Patchnotes Channel | The channel to send Hypixel Skyblock patchnotes to.                                                    | Channel       |
| Fetchur Ping                | The role to ping for Daily Fetchur items.                                                              | Role          |
| Fetchur Channel             | The channel to send Daily Fetchur items to.                                                            | Channel       |
| Global Event Ping           | The role to ping when a global event is started.                                                       | Role          |
| Global Event Channel        | The channel to send global event messages to.                                                          | Channel       |
| SkyBlock Date               | The channel to update with the Hypixel Skyblock date.                                                  | Channel       |
| SkyBlock Event Channel      | The channel to send Skyblock events too. See [Skyblock Events](#skyblock-events) for more information. | Channel       |
| Scammer Log Channel         | The channel to send actions that bot has taken against Scammers, IRL traders, ratters, and macroers.   | Channel       |
| Scammer Action              | The action to take against scammers.                                                                   | Role/Kick/Ban |
| IRL Trader Action           | The action to take against IRL traders.                                                                | Role/Kick/Ban |
| Ratter Action               | The action to take against ratters.                                                                    | Role/Kick/Ban |
| Macroer Action              | The action to take against macroers.                                                                   | Role/Kick/Ban |
```

There are also configuration settings relating to verification:

```{table}
:width: 100%
:widths: auto
:align: center

| Name                 | Description                                                     | Type    |
|----------------------|-----------------------------------------------------------------|---------|
| Verification Enabled | Whether verification is enabled or not.                         | Boolean |
| Verified             | The role to give to verified users.                             | Role    |
| VIP                  | The role to give to players with the VIP rank in Hypixel.       | Role    |
| VIP+                 | The role to give to players with the VIP+ rank in Hypixel.      | Role    |
| MVP                  | The role to give to players with the MVP rank in Hypixel.       | Role    |
| MVP+                 | The role to give to players with the MVP+ rank in Hypixel.      | Role    |
| MVP++                | The role to give to players with the MVP++ rank in Hypixel.     | Role    |
| YouTube              | The role to give to players with the YouTube rank in Hypixel.   | Role    |
| Hypixel Staff        | The role to give to Hypixel staff members.                      | Role    |
| Nickname             | The nickname to give to verified users. [See Below](#nicknames) | String  |
```

### Nicknames

The nickname configuration setting allows you to set a nickname for verified users. This is useful for servers that have a nickname format, such as `Username [Rank]`.

The nickname can be set using the following placeholders:

- `{name}`: The user's Discord username.
- `{ign}`: The user's Minecraft username.
- `{rank}`: The user's Hypixel rank.
- `{network_level}`: The user's network level.
- `{cata_level}`: The user's Catacombs level.
- `{skyblock_level}`: The user's Skyblock level.
- `{skill_avg}`: The user's skill average.
- `{lily_weight}`: The user's lily weight.
- `{senither_weight}`: The user's senither weight.

For example, if you wanted to set the nickname to be `[ADMIN] hypixel`, you would set the nickname to be `[{rank}] {ign}`.


## Guild Linking

Guild linking allows you to link your guild to your Discord server, allowing you to sync roles based on guild membership and rank.

To link your guild, you must first have the `Manage Server` permission. Then, you can use the `/config guilds add-guild` command to link your guild.

To view the configuration for your guild, you can use the `/config guilds view` command.

### General Guild Settings

The guild's general settings can be edited using the `/config guilds edit-guild` command.

```{table}
:width: 100%
:widths: auto
:align: center

| Name                | Description                                                                                   | Type    |
|---------------------|-----------------------------------------------------------------------------------------------|---------|
| Membercount Channel | The channel to update with the guild's membercount. [SkyKings Premium](/premium) is required. | Channel |
| Membercount Format  | The format to use for the membercount. [See Below](#membercount-formatting).                  | String  |
| Role                | The role to give to guild members.                                                            | Boolean |
```

#### Membercount Formatting

The membercount format can be set using the following placeholders:

- `{count}`: The guild's membercount.

For example, if you wanted to set the membercount to be `Guild Members: 100`, you would set the membercount format to be `Guild Members: {count}`.


### Guild Ranks

Guild ranks can be added using the `/config guilds add-rank` command. They only have one possible setting, `Role`.

You can update the role for a rank using the `/config guilds edit-rank` command.


## Skyblock Events
