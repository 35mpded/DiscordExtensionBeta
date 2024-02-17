## Features

* Add Commands For Players / Admins to use to see connected players in discord
* The command will return an embed with up to 25 connected players each. Buttons are added to the embed to sort and page through all connected players
* Support for multiple commands to customize how you want the embed to look and feel.
* Support for permanent messages that are updated on a set interval

### /players Default Embed
![](https://i.postimg.cc/m2Wzsnm8/image.png)

### /playersadmin Default Embed
![](https://i.postimg.cc/WpYTvYTx/image.png)

## Discord Commands

* `/players` -- returns a list of all the connected players
* `/playersadmin` -- returns a list of all the connected players

**Note:** Commands can be customized in the config

### Discord Command Configuration
You can read how to configure discord command channels and permissions [Here](https://discord.com/blog/slash-commands-permissions-discord-apps-bots)

## Getting Your Bot Token
[Click Here to learn how to get an Discord Bot Token](https://umod.org/extensions/discord#getting-your-api-key)

## Configuration

```json
{
  "Discord Bot Token": "",
  "Command Messages": [
    {
      "Command Name (Must Be Unique)": "players",
      "Allow Command In Direct Messages": true,
      "Display Admins In The Player List": true,
      "Players Per Embed (0 - 25)": 25
    },
    {
      "Command Name (Must Be Unique)": "playersadmin",
      "Allow Command In Direct Messages": true,
      "Display Admins In The Player List": true,
      "Players Per Embed (0 - 25)": 25
    }
  ],
  "Permanent Messages": [
    {
      "Enabled": true,
      "Template Name (Must Be Unique)": "Permanent",
      "Permanent Message Channel ID": "599037479487799316",
      "Update Rate (Minutes)": 1.0,
      "Display Admins In The Player List": true,
      "Players Per Embed (0 - 25)": 25
    },
    {
      "Enabled": true,
      "Template Name (Must Be Unique)": "PermanentAdmin",
      "Permanent Message Channel ID": "927657602094092338",
      "Update Rate (Minutes)": 1.0,
      "Display Admins In The Player List": true,
      "Players Per Embed (0 - 25)": 25
    }
  ],
  "Discord Extension Log Level (Verbose, Debug, Info, Warning, Error, Exception, Off)": "Info"
}
```

### Discord Message Configuration
You can configure Discord Message, Discord Embed, and Discord Command in the following directory
`oxide\discord\DiscordPlayers`

## Localization
```json
{
  "SortByEnumName": "Name",
  "SortByEnumTime": "Time"
}
```