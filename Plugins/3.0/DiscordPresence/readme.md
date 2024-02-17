## Features

* Updates the bots status message on the discord server with text from the list at a set interval.

## Getting Your Bot Token
[Click Here to learn how to get an Discord Bot Token](https://umod.org/extensions/discord#getting-your-api-key)

## Configuration

```json
{
  "Discord Application Bot Token": "",
  "Enable Sending Message Per Update Rate": true,
  "Enable Sending Message On Player Leave/Join": true,
  "Enable Sending Server Loading Message": true,
  "Update Rate (Seconds)": 15.0,
  "Status Messages": [
    {
      "Message": "{server.name}",
      "Type": "Custom"
    },
    {
      "Message": "{server.players}/{server.players.max} Players",
      "Type": "Custom"
    },
    {
      "Message": "{server.players.sleepers} Sleepers",
      "Type": "Custom"
    },
    {
      "Message": "{server.players.stored} Total Players",
      "Type": "Custom"
    },
    {
      "Message": "Server FPS {server.fps}",
      "Type": "Custom"
    },
    {
      "Message": "{server.entities} Entities",
      "Type": "Custom"
    },
    {
      "Message": "{server.players.total} Lifetime Players",
      "Type": "Custom"
    },
    {
      "Message": "{server.players.queued} Queued",
      "Type": "Custom"
    },
    {
      "Message": "{server.players.loading} Joining",
      "Type": "Custom"
    },
    {
      "Message": "Wiped: {server.map.wipe.last!local}",
      "Type": "Custom"
    },
    {
      "Message": "Size: {world.size} Seed: {world.seed}",
      "Type": "Custom"
    }
  ],
  "Server Loading Message": {
    "Message": "Server is booting",
    "Type": "Custom"
  },
  "Discord Extension Log Level (Verbose, Debug, Info, Warning, Error, Exception, Off)": "Info"
}
```

### Valid Types;
`Custom` - "{name}"  
`Game` - "Playing {name}"  
`Streaming` - "Streaming {name}"  
`Listening` - "Listening {name}"  
`Watching` - "Watching {name}"  
`Competing` - " Competing in {name}"

### Available Placeholders;

To see the list of available Discord Extension placeholders you can use console command `de.placeholders.list`  
To see the list of available PlaceholderAPI placeholders you can use console command `placeholderapi.list`

#### PlaceholderAPI
PlaceholderAPI is not a required plugin but if you wish to include game specific placeholders it will is required


