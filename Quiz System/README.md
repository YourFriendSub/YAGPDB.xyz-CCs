# Interactive Quiz System
> This is a Quiz system that uses Buttons, Select Menus & Modals to let the Server Administrators make their own Quizzes that suits their community best.
- [Jump To Installation](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System#Installation) or Just Scroll Down.
> Version: 6.5 (6th Rewrite + Some BugFixes & Features Added)
> P.S. English isn't my First Language.

## Features
- ✅ Feature 1 - Is Interactive. Uses Buttons, Select Menus & Modals for almost everything.
- ✅ Feature 2 - You can customize, 5 different types of parameters:
  - `{{$ModeratorRoleID := 00000}}`: RoleID of the staff role that can create, rechange and end the Quiz.
  - `{{$DefaultEmoji := "Digit"}}`: Default Emoji-Pack of the Quiz. *Default=Digit*
    - There're three Emoji-Packs, Digit, Star & Dot.
  - `{{$PingQuizRole := ""}}`: The role you want to ping when sending Quiz.
    - You can select a new for each quiz from Quiz Builder's button, e.g. More.
  - `{{$YesQuiz := ""}}`: If user **DON'T HAVE** this role, he cannot participate in the current quiz.
  - `{{$NoQuiz := ""}}`: If user **HAVE** this role, he cannot participate in the current quiz.
  > NOTE:
    - You are only allowed to use either `$YesQuiz` or `$NoQuiz`. Adding Roles in both variable could result in bugs and errors.
- ✅ Featere 3 - Error Handing for each and every action that staff or user'll do.
- ✅ Featere 4 - See Chart on how dumb your community members are! Just kidding, it gives a chart that shows which option people are clicking most.
- ✅ Featere 5 - Add image into your quiz.
> Ahh, I'm tired, there're just too many features that even i cannot list them all here...

---

## Demo
TO-DO: ADD DEMO IMAGES

---

## Installation

### Needs
- A dedicated Moderator-Role (Or Quiz-Moderator Role?) *REQUIRED*
- Role for when quiz'll be sent to the channel. *OPTIONAL*
- Role for who **WILL BE** able to participate in the quiz. *OPTIONAL*
- Role for who **WILL NOT BE** able to participate in the quiz. *OPTIONAL*

### Setup

**TO-DO:** EDIT THIS SETUP ONE
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System/Code%20Files/Command.yag) and copy the code.
  - Paste the code under your server's dashboard: `Tools & Utilitie > Ticket System`
  - Replace the `00000` in `{{$ModRole := 00000}}` variable with ID of your Moderator-Role
    - *Don't know how to copy Role-ID? You shouldn't own a server.* Just kidding, you can ask this in official support server or just google it.
  - Let `{{$PingModRole := true}}` If you want to ping Moderator role on ticket create.
  - Let `{{$PinTopMessage := true}}` If you want to Pin the first message of the ticket. *Bot should've Manage Messages*
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Code%20Files/Command.yag) and copy the code.
  - Create a New Custom command with:
    - Trigger Type: `Command`
    - Trigger: `cticket`
  > *Don't forget to restrict this command only for your moderator role.*

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Code%20Files/Component.yag) and copy the code.
  - Create a New Custom command with and paste the code:
    - Trigger Type: `Message Component`
    - Trigger: `cticket_`
  - Replace the `00000` in `{{$ModRole := 00000}}` variable with ID of your Moderator-Role
    - Again, *Don't know how to copy Role-ID? You shouldn't own a server.* Just kidding, you can ask this in official support server or just google it.
  - This is the commend, where you can customise the permission of Ticket-Owner. Adjust the variables as your needs.

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Code%20Files/Modal.yag) and copy the code.
  - Create a New Custom command with and paste the code:
    - Trigger Type: `Modal Submission`
    - Trigger: `cticket_`
  - Replace the `00000` in `{{$LogsChannel := 00000}}` variable with ID of your Logs-Channel
    - *Don't know how to copy Channel-ID? You shouldn't own a server.* Just kidding, you can ask this in official support server or just google it.

- Now, use the command `-cticket setup` to send the Ticket Panel. *From where people will create tickets.*
---
### TODO
> ● Make this folder public.

### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
