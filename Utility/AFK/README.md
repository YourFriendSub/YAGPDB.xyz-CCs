# AFK Command
> This is an AFK Command that i wrote from scratch. I've added a bunch of features that i saw in different bots and the features that the AFK command on the YAGPDB.xyz bot's CC repository was missing.
- [Jump To Installation](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK#Installation) or Just Scroll Down.

## Features
- ✅ Feature 1 - You can add a duration for how long you're going to be AFK.
- ✅ Feature 2 - Shows how long it's been for you when you went AFK, and when will you arrive. If you added a duration, it'll show the rest of duration in humanize format and if you didn't add any duration, it'll show "indefinitely".
  - [Click here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK#Demo) to jump to demo Images or just scroll down.
- ✅ Feature 3 - Command has a bunch of Variables to customisation configure from.
  - `{{$Command := "-afk"}}`: To choose what you want as the AFK trigger.
    - If you want, you could also use `-mydogatemyhomeworkandnowihavenothingtoshowtheteacher` as your prefix and command.
  - `{{$RemoveOnM := true}}`: If you want to Remove AFK on message or not.
    - If set `true`, AFK will be removed on any message, weather it's just a images, sticker, or a simple text.
    - If set `false`, AFK will only be remove when you send `-afk` [or what you set for the `$Command` variable].
    - NOTE: No matter how you remove/add your AFK, if you'll use `-AFK + (REASON) or (SEPARATOR + DURATION) or (REASON + SEPARATOR + DURATION)` your afk will be updated in each case.
  - `{{$ByeR := "👋"}}`: If you want bot to react on your AFK add trigger message.
    - If emoji is given, it'll react to trigger message.
    - If no emoji is given [just a empty string (`""`)], it'll not add the reaction on your trigger message.
  - `{{$ByeM := true}}`: If you want bot to send a message and reply on your AFK add trigger message.
    - If `true`, it'll send a message & reply to your trigger message about AFK add.
    - If `false`, it'll NOT send a message on your trigger message about AFK add.
  - `{{$NickAFK := "[AFK] "}}`: To add a `[AFK] ` at the starting of the member nickname.
    - If you don't want to bot to rename the user on AFK Set, just remove the text and make it a empty string, e.g. `""`.
  - `{{$WelcomeR := "🙌"}}`: If you want bot to react on your AFK remove trigger message.
    - If emoji is given, it'll react to trigger message.
    - If no emoji is given [just a empty string (`""`)], it'll not add the reaction on your trigger message.
  - `{{$WelcomeM := true}}`: If you want bot to send a message and reply on your AFK remove trigger message.
    - If `true`, it'll send a message & reply to your trigger message about AFK remove.
    - If `false`, it'll NOT send a message on your trigger message about AFK remove.
  - `{{$Separator := "&&& "}}`: To separator `AFK Message` and `Duration`.
    - Some people also like to use `-d `.

  > NOTE:
    - If your AFK trigger for setting the AFK isn't right or you didn't give any, it'll just use a inner variable `No AFK Message.` as your AFK.

---

## Demo
**NOTE**: In this demo, all the possible Variables are `true` or filled with correct data.

<details>
<summary>1</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Assets/20251107_112925.jpg" alt="1" width="400">
</details>

<details>
<summary>2</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Assets/20251107_105205.jpg" alt="2" width="400">
</details>

<details>
<summary>3</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Assets/20251107_110313.jpg" alt="3" width="400">
</details>

<details>
<summary>4</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Assets/20251107_111403.jpg" alt="4" width="400">
</details>

<details>
<summary>5</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Assets/20251107_111716.jpg" alt="5" width="400">
</details>

---

## Installation

### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Code%20Files/Command.yag) and copy the code.
  - Create a New Custom command with:
    - Trigger Type: `regex`
    - Trigger: `\A` or `.*` [So it could trigger on every possible message in server]
  - If you want to configure your AFK settings, do them as well from the variables under `{{/* Configuration */}}` comments.
  - I personally recommend you to also add `Redirect errors to selected channel` or disable the `Output errors as command response`, because it's a command that'll run on every single message on the server. If chat is fast, and bot ping goes high. it may flood chat with `Gave up trying to execute custom command #N after 1 minute because there is already one or more instances of it being executed.` error.

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Utility/AFK/Code%20Files/LeaveFeed.yag) and copy the code.
  - Paste it under the `Notifiactions & Feed > General > User Leave Feed`.
    - It'll delete the AFK of server members who'll leave your server.

---
### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
