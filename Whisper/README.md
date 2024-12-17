# Whisper Command
> A way to talk to anyone privately, without Direct Messageing (DMing) them.
- [Jump To Installation](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/tree/main/Whisper#installation) or Just Scroll Down.
> P.S. English isn't my First Language.
### Brief Description:
Let's say User-A wants to tell User-B something privately, but they don't have enough time to send a direct message. So, User-A can use the command `-whisper @User-B || Private message ||`. The bot will delete User-A's message and will send its own message with a button. If User-B clicks on the button, they can see the private text. However, if someone else, like User-C, clicks the button, the bot will prevent them from seeing the message and will show a message saying "This message is not for you." Also, the private message will expire 15 minutes later, whether User-B has seen it or not.


## Installation
### Needs
- Channel-ID・*Optional* ]
- Duration in Seconds・*Optional*
### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper/Code%20Files/Command.yag) and copy the code.
  - Create a New Custom command with:
    - Trigger Type: `Command`
    - Trigger: `whisper`
  - If don't want to send whisper message in the same channel, You can edit the `{{$Channel := .Channel.ID}` variable and replace `.Channel.ID` with your desired Channel-ID.
  - If you want to edit the expiry of whisper message you can edit the `{{$Expire := 900}}` variable adn replace `900` with your desired duration.
    - NOTE: This should be in seconds.
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Whisper/Code%20Files/Component.yag) and copy the code.
  - Create a New Custom command with:
    - Trigger Type: `Message Component`
    - Trigger: `whisper_`

### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
- 
