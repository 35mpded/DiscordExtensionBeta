# Welcome

Welcome to the Discord Extension Beta. 
This is were all testing for the Discord Extension V3.0.0 will take place. 
You can view the Discord Extension Documentation [Here](Extension).
You can download the Discord Extension [Here](https://github.com/dassjosh/DiscordExtensionBeta/raw/main/Extension/Oxide.Ext.Discord.dll).
Plugins that have been updated to support 3.0 can be found here [Here](Plugins/2.0).

## Major Changes

### Framework
The dotnet framework version used by the extension has been bumped from 3.5 to 4.8.
This allows the extension to use newer features available and has enabled us to drop websocketsharp in favor of System.Net.WebSockets

### Rewrites
The API and Websocket handling have been rewritten from scratch.
The API now supports concurrent requests per bucket.
API bucket handling has been vastly improved and implemented according to Discord specifications.
API error handling has changed so error messages are only displayed if the final request attempt fails.
This will reduce the error message spam.
Plugins can now hide API error messages.

Websockets have been redesign to use System.Net.WebSockets.
Rate limiting for websockets has been improved to prevent the websocket being forced to reconnect.
Plugins sending too many websocket messages will display a warning.
Websockets are contained within their own thread and don't cross into the main server thread.

### Promises
The extension now provides it's own promise library for plugins to use in place of async code.
Plugins can subscribe to the result / error / finally of the promise.
Discord API calls are now using promises and is one of the changes plugins will need to make during their upgrade to 3.0.

### Placeholders
The extension now has built in placeholder support.
Placeholders allow for far greater message customization.
The extension comes with many server and discord related placeholders built in.
Plugins can easily add their own custom placeholders.
Plugins can override extension default placeholders.
Placeholders also support formats for types that support it.
Discord Extension Placeholders are also compatible with PlaceholderAPI plugin.

### Templates
Discord Templates are multiple new libraries that are being added.
These libraries perform a similar function to the oxide lang api and is applied to multiple discord entity types.
This allows messages to be localized to a Discord User or Server Player.
This also supports Application Command Localization and Auto Complete Localization
Plugins can register templates and server admins can edit these templates to customize the message how they wish.
Discord currently supports the following types as templates:
- Messages
- Embeds
- Embed Fields
- Components
- Modal
- Application Commands
- Auto Complete

### Application Commands
`DiscordAppCommand` is a new library and the recommend way to do command handling going forward.
This library handles the callbacks for Application Commands, Auto Complete, Message Component, and Modal Submit events.
There is a new type `ApplicationCommandBuilder` that is available to make it easier to build out commands.
After building the command localizations can be generated and applied to the command before registration.

### Pooling
Object Pooling is now used throughout the extension.
Pooling is available to plugins to use.
If a pool is being used improperly by a plugin or the extension warnings will be displayed to indicate there is a misuse of the pool.

### Hooks
Discord Extension will now cache the hooks that are used by Discord Extension plugins and will not call or perform any memory allocations unless the hook is registered in a plugin.

### Logging
Logging has had many improvements.
Logging is now designed to not have any memory allocations unless the log actually needs to be created.
File logging is now an option.
File and Console logging can be at separate log levels.
File and Console logging can be changed at runtime or through the discord.config.json config file.

### Locale
DiscordLocale is a new library that allows converting between Discord Locale and Oxide Lang for Discord users and server players.

### Trie
Ukkonen Trie is a new type used by the extension for high performance auto complete.
This is used by the AutoCompleteBuilder for player name auto completion in application commands.
This is also made accessible to plugins who wish to use auto completion for other purposes.

### Preprocessor Directives
The Discord Extension now registers preprocessor directives. The following directives are registered:  
`DiscordExt`  
`DiscordExt3_0`

## Changes

## Deprecations
`DiscordCommand` is now deprecated. Plugins should upgrade to the new DiscordAppCommand which uses Discord Application Commands.