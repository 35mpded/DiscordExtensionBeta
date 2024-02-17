## Features

* Allows players to private message each other even if they're not connected to the rust server
* The players must have linked their discord and game accounts first
* All discord private messages will be send by the bot in a private message

## Discord Link
This plugin supports Discord Link provided by the Discord Extension.
This plugin will work with any plugin that provides linked player data through Discord Link.

## Chat Commands

* `/pm MJSU Hi` -- will send a private message to MJSU wit the text Hi
* `/r Hi` -- Will reply to the last received message with the text Hi

## Discord Commands

* `/pm MJSU Hi` -- will send a private message to MJSU wit the text Hi
* `/r Hi` -- Will reply to the last received message with the text Hi

### Discord Command Configuration
You can read how to configure discord command channels and permissions [Here](https://discord.com/blog/slash-commands-permissions-discord-apps-bots)

## Getting Your Bot Token
[Click Here to learn how to get an Discord Bot Token](https://umod.org/extensions/discord#getting-your-api-key)

## Configuration

```json
{
  "Discord Bot Token": "",
  "Allow Discord Commands In Direct Messages": true,
  "Enable Effect Notification": true,
  "Notification Effect": "assets/prefabs/tools/pager/effects/vibrate.prefab",
  "Log Settings": {
    "Log To Console": true,
    "Log To File": false,
    "Log To Channel ID": ""
  },
  "Discord Extension Log Level (Verbose, Debug, Info, Warning, Error, Exception, Off)": "Info"
}
```

### Discord Message Configuration
You can configure Discord Message, Discord Embed, and Discord Command in the following directory
`oxide\discord\DiscordPM`

## Localization
```json
{
  "V3.Chat": "[#BEBEBE][[#de8732]Discord PM[/#]] {discordpm.chat}[/#]",
  "V3.ToFormat": "[#BEBEBE][#de8732]PM to {target.player.name:clan}:[/#] {discordpm.message}[/#]",
  "V3.FromFormat": "[#BEBEBE][#de8732]PM from {player.name:clan}:[/#] {discordpm.message}[/#]",
  "V3.LogFormat": "{player.name:clan} -> {target.player.name:clan}: {discordpm.message}",
  "V3.InvalidPmSyntax": "Invalid Syntax. Type [#de8732]/{plugin.lang:V3.Commands.Chat.PM} MJSU Hi![/#]",
  "V3.InvalidReplySyntax": "Invalid Syntax. Ex: [#de8732]/{plugin.lang:V3.Commands.Chat.Reply} Hi![/#]",
  "V3.NoPreviousPm": "You do not have any previous discord PM's. Please use /{plugin.lang:V3.Commands.Chat.PM} to be able to use this command.",
  "V3.NoPlayersFound": "No players found with the name '{discordpm.player.notfound}'",
  "V3.MultiplePlayersFound": "Multiple players found with the name '{discordpm.player.notfound}'.",
  "V3.Commands.Chat.PM": "pm",
  "V3.Commands.Chat.Reply": "r"
}
```