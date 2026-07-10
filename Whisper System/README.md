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
- Let's say User-A wants to tell User-B something privately, but they don't have enough time to send a direct message. So, User-A can use the command `-whisper @User-B || Private message ||`. The bot will delete User-A's message and will send its own message with a button. If User-B clicks on the button, they can see the private text. However, if someone else, like User-C, clicks the button, the bot will prevent them from seeing the message and will show a message saying "This message is not for you." Also, the private message will expire 15 minutes later, whether User-B has seen it or not.


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
```go
{{/*
	Expiry         — Default whisper duration
	ChannelID      — Target channel to send whispers in
	RemoveInvites  — Strip Discord invite links from whisper content
	MaxViews       — Per-recipient view limit (unlimited for sender)
	Anonymous
		Roles      — Roles allowed to whisper anonymously
		Perms      — Permissions allowed to whisper anonymously
	Logs
		Channel    — Channel ID to send logs to
		Log        — Log filter: "Anonymous", "Unanonymous", or "All"
*/}}
```
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper%20System/Version%204%3A%20CodeFiles/Component.yag) and copy the `Component` code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whisper_`

### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
