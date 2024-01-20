Syncs players between game & Discord.
This plugin uses a Game > Discord direction, so if you were to sync names, it would make their Discord name match their Steam name.

The bot will ONLY sync roles that are lower priority than it, unless the bot has Admin permissions on Discord.

**Note:** Oct. 2020 changes to the Discord API may result in this plugin not working if your bot doesn't have proper settings. "SERVER MEMBERS INTENT" must be enabled in your [Application Dashboard](https://discord.com/developers/applications/) under the Bot section.

## Configuration

```json
{
  "Discord Bot Token": "",
  "Discord Server ID (Optional if bot only in 1 guild)": "",
  "Update Interval (Minutes)": 10,
  "Enable Nick Syncing": false,
  "Enable Ban Syncing": false,
  "Enable Role Syncing": true,
  "Role Setup": [
    {
      "Oxide Group": "default",
      "Discord Role": "Member"
    },
    {
      "Oxide Group": "vip",
      "Discord Role": "Donator"
    }
  ],
  "Discord Extension Log Level (Verbose, Debug, Info, Warning, Error, Exception, Off)": "Info"
}
```

## Features

* Enforce **username** matching from in-game to your Discord server.
* Enforce **bans** on your discord server when someone is banned In-game.
* Assign **roles** on your discord server based on oxide groups.