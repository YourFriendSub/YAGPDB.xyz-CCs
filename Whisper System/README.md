# Whisper System

> A way to talk to anyone privately, without Direct Messageing (DMing) them.
> Jump To Installation For,
- [Verion: 1](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/README.md#installation).
- [Verion: 2](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/README.md#installation).
- [Verion: 3](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/README.md#installation).
- [Verion: 4](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/README.md#installation).
or Just Scroll Down

There are Four Versions for now, i'd suggest to use the the 4th version, because people with modded discord apps will not be able to see the message since it'll be sent via slash.

### Brief Description:
## Version 1:
Let's say `User-A` wants to tell `User-B` something privately, but they don't have enough time to send a direct message. So, `User-A` can use the command `-whisper @User-B || Private message ||`. The bot will delete `User-A`'s message and will send its own message with a button. If `User-B` clicks on the button, they can see the private text. However, if someone else, like `User-C`, clicks the button, the bot will prevent them from seeing the message and will show a message saying `"This message is not for you."` Also, the private message will expire `900` seconds later, whether `User-B` has seen it or not.


### Installation
**Needs**
- Channel-ID・*Optional*
- Duration in Seconds・*Optional*
### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%202%3A%20CodeFiles/Component.yag) and copy the `Command` code.
  - Create a New Custom command with:
    - Trigger Type: `Command`
    - Trigger: `whisper`
  - If don't want to send whisper message in the same channel, You can edit the `{{$Channel := .Channel.ID}}` variable and replace `.Channel.ID` with your desired Channel-ID.
  - If you want to edit the expiry of whisper message you can edit the `{{$Expire := 900}}` variable adn replace `900` with your desired duration.
    - NOTE: This should be in seconds.
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%202%3A%20CodeFiles/Component.yag) and copy the `Component` code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whisper_`

## Version 2:
Let's say `User-A` wants to tell `User-B`, `User-C`, `User-D` and/or `User-E` something privately, but they don't have enough time to send a direct message. So, `User-A` can use the command `-whisper @User-B User-B User-C User-D User-E & || Private message ||`. The bot will delete `User-A`'s message and will send its own message with a button. If `User-B` clicks on the button, they can see the private text. However, if someone else, like `User-F` or `User-G`, clicks the button, the bot will prevent them from seeing the message and will show a message saying `"This message is not for you."` Also, the private message will expire `900` seconds later, whether `User-B`, `User-C`, `User-D` or `User-E` has seen it or not.


### Installation
**Needs**
- Channel-ID・*Optional*
- Duration in Seconds・*Optional*
### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%202%3A%20CodeFiles/Command.yag) and copy the `Command` code.
  - Create a New Custom command with:
    - Trigger Type: `Command`
    - Trigger: `whisper`
  - If don't want to send whisper message in the same channel, You can edit the `{{$Channel := .Channel.ID}}` variable and replace `.Channel.ID` with your desired Channel-ID.
  - If you want to edit the expiry of whisper message you can edit the `{{$Expire := 900}}` variable adn replace `900` with your desired duration.
    - NOTE: This should be in seconds.
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%202%3A%20CodeFiles/Component.yag) and copy the `Component` code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whisper_`

## Version 3:
Let's say `User-A` wants to tell `User-B`, `User-C`, `User-D` and/or `User-E` something privately, but they don't have enough time to send a direct message. So, `User-A` can use the `whisperpanel` in which, `User-A` selects the all the people they want to whisper to from a select-menu. then the bot sends a modal to them asking for:
- Text: Message you want to show in whisper.
- MediaLink: Upto 10 Links could be atted and shown in whisper, should be Direct Image/Video links.
 - If not given or in the case of wrong value, it does not show the media in whisper message.
- MaxViews: Max amount of times, each receiver User can see the Whisper. When User uses all their views for that whisper, bot will not let them see the whisper anymore.
  - Effects indivisually, for each User.
  - If not given or in the case of wrong value, uses default values set on Custom Command code by guild managers.
- Expiry: Duration for the whisper to expire after. Requires real durations e.g. `1h23m19s`.
  - Effects all the users.
  - If not given or in the case of wrong value, uses default values set on Custom Command code by guild managers.
> In modal, only the `Text` is a required value. Other values `MediaLink`, `MaxViews` & `Expiry` are optinal.

Afer giving all the values, `User-A` can click the submit button in modal. On clicking the submit button, bot sends a message mentioning all the users that `User-A` chose in select menu with and Button to see the whisper message. If users mentined in message click on the button, they can see the private text. However, if someone else, that is not mentioned on the message clicks the button, the bot will prevent them from seeing the message and will show a message saying `"This message is not for you."` Also, the private message will expire based on the duration given, whether mentioned users have seen it or not. it also deletes the last whisperpanel and sends a new one so the whisperpanel stays on the bottom for better UX.


### Installation
**Needs**
- Channel-ID・*Optional*
- Duration in Seconds・*Optional*
### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%203%3A%20CodeFiles/Command.yag) and copy the `COmmand` code.
  - Create a New Custom command with:
    - Trigger Type: `Command`
    - Trigger: `whispersystem`
  - `{{$MaxSelections}}`: How many users could be selected by sender.
  - `{{$WritingTime := 900}}`: How much seconds can user take to write the text on Modal. [Not that important]
  - `{{$Expiry := "15m"}}`: Default expiration duration for a whisper.
  - `{{$ChannelID := .Channel.ID}}`: ID of the channel where all the whispers should go in.
  - `{{$CCID := 0}}:` Custom Command ID of [Command](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%203%3A%20CodeFiles/Command.yag), trigger type command.
  - `{{$RemoveInvites := true}}:` Whether to remove Discord invite links from text given in modal or not.
  - `{{$MaxViews := 100}}`: Default maximum views allowed per message, per user.
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%203%3A%20CodeFiles/Component.yag) and copy the `Component` code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whispersystem_`
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%203%3A%20CodeFiles/Modal.yag) and copy the `Modal` code.
  - Create a New Custom command with:
    - Trigger Type: `Modal`
    - Trigger: `whispersystem_`

## Version 4:
Let's say `User-A` wants to tell up to 5 users something privately, but they don't have enough time to send a direct message. So, `User-A` can use the slash command `/whisper`, giving:

- `users`: The users to whisper to. *(Upto 5 mentions.)*
- `message`: The private text to show in the whisper.
- `medialinks`: Upto 10 Direct Image/Video links to show in the whisper.
  - If not given or in the case of a wrong value, it does not show media in the whisper message.
- `maxviews`: Max amount of times, each receiver User can see the Whisper. When a User uses all their views for that whisper, the bot will not let them see the whisper anymore.
  - Effects individually, for each User.
  - If not given, uses the default value set on the Custom Command code by guild managers.
- `expiry`: Duration for the whisper to expire after. Requires real durations e.g. `1h23m19s`.
  - Effects all the users.
  - If not given, uses the default value set on the Custom Command code by guild managers.
- `anonymous`: Whether to hide `User-A`'s identity from whisper recipients.
  - Only works if `User-A` has a Role/Permission allowlisted by guild managers, otherwise it's ignored.
- `channel`: Which channel to send the whisper in.
  - If not given, uses the default channel set on the Custom Command code by guild managers.

> Only `users` and `message` are required values. Other values `medialinks`, `maxviews`, `expiry`, `anonymous` & `channel` are optional.

On running the command, the bot sends a message mentioning all the users `User-A` chose, with a button to see the whisper message, and gives `User-A` an ephemeral confirmation showing the whisper's settings and a jump link to it. If a mentioned user clicks the button, they can see the private text (and media, if any) — but each time they view it, one of their `maxviews` is used up; once they run out, the bot tells them they have no views left. However, if someone not mentioned, like `User-F`, clicks the button, the bot prevents them from seeing the message and shows `"This message is not for you."` `User-A` themself has unlimited views and is always shown as the sender, and unless `anonymous` was used successfully, everyone else who views it sees who sent it too. `User-A` can also press a second button to delete the whisper early, which removes it for everyone regardless of expiry. Otherwise, the whisper expires based on the duration given, whether recipients have seen it or not. Optionally, all of this can be logged to a channel set by guild managers.

### Installation
**Needs**
- Channel-ID・*Optional*
- Duration in Seconds・*Optional*
### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%204%3A%20CodeFiles/SlashCommand.yag) and copy the `SlashCommand` code.
  - Create a New Custom command with:
    - Trigger Type: `Slash`
    - Trigger: `whisper`
  - Then add these options:
    - 1
      - Name: `users`
      - Type: `Text`
      - Description: `Users to Whisper (Roles & Text will be removed)`
      - Required: `true`
      - MinLength: [Leave enpty if you want]
      - MaxLength: `110` [It'll cap it to max 5 mentions]
    - 2
      - Name: `message`
      - Type: `Text`
      - Description: `Message; Max: 3200 [Letter]`
      - Required: `true`
      - MinLength: `1` or [Leave enpty if you want]
      - MaxLength: `3200` [Don't go more than this, could start giving errors.]
    - 3
      - Name: `medialinks`
      - Type: `Text`
      - Description: `MediaLink; Max: 10 [Link]`
      - Required: `false`
      - MinLength: [Leave enpty]
      - MaxLength: [Leave enpty]
    - 4
      - Name: `maxviews`
      - Type: `Integer`
      - Description: `MaxViews; Min: 1 [Int]`
      - Required: `false`
      - MinLength: `1`
      - MaxLength: [Leave enpty]
    - 5
      - Name: `expiry`
      - Type: `Text`
      - Description: `Expiry; In: Humanize [Duration]`
      - Required: `false`
      - MinLength: [Leave enpty]
      - MaxLength: `32`
    - 6
      - Name: `anonymous`
      - Type: `True/False`
      - Description: `Show my username to whispered users; (Specials* Only)`
      - Required: `false`
    - 7
      - Name: `channel`
      - Type: `Channel`
      - Description: `Channel to send Whispers in`
      - Required: `false`
  - In the code, you can configure more if you want:
    - `{{$Expiry := "15m"}}`: Default whisper duration, used if the `expiry` option isn't given.
    - `{{$ChannelID := .Channel.ID}}`: Default channel to send whispers in, used if the `channel` option isn't given.
    - `{{$RemoveInvites := true}}`: Whether to strip Discord invite links out of the `message` option's text or not.
    - `{{$MaxViews := 100}}`: Default maximum views allowed per whisper, per recipient, used if the `maxviews` option isn't given. *(Sender always has unlimited views.)*
    - `{{$Anonymous := sdict ...}}`: Who's allowed to use the `anonymous` option.
      - `"Roles" (cslice ... ... ...)`: Role-IDs allowed to whisper anonymously. [Leave empty if you don't want role-based access]
      - `"Permissions"`: Permissions allowed to whisper anonymously. *(Defaults to `Administrator` or `Manage Server`.)*
    - `{{$Logs := sdict ...}}`: Where and what to log.
      - `"Channel" 0`: Channel-ID to send whisper logs to. [set to `0` to disable logging]
      - `"Log" "All"`: Which whispers get logged — `"All"`, `"Anonymous"` *(only anonymous ones)*, or `"Unanonymous"` *(only non-anonymous ones)*.
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%204%3A%20CodeFiles/Component.yag) and copy the `Component` code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whisper_`

### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
