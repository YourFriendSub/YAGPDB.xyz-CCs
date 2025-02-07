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
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System/Code%20Files/Command.yag) and copy the code.
  - Create a New Custom command and paste the code:
    - Trigger Type: `Command`
    - Trigger: `quiz`
  - Replace the `00000` in `{{$ModeratorRoleID := 00000}}` variable with ID of your Moderator-Role / Quiz-MOD role.
    - If someone will have this role, They'll be able to Create, End, Delete, See Stats, See Info and do anything related to the Quiz-System.
  - Replace the `"Digit"` in `{{$DefaultEmoji := "Digit"}}` variable with your preferred Emoji-Pack.
    - There are three Emoji-Packs in This Quiz System. `Digit`, `Dot`, `Star`.
  - Replace the `""` in `{{$PingQuiz := ""}}` variable with ID of your PingQuiz role.
    - This is the role that'll be pinged when you click on Send-Quiz button in Quiz-Builder. It's Optional.
  - Replace the `""` in `{{$YesQuiz := ""}}` variable with ID of your YesQuiz role.
    - If user **DON'T HAVE** this role, they **WILL NOT** be able to participate in the quiz, also the stats wouldn't increase.
  - Replace the `""` in `{{$NoQuiz := ""}}` variable with ID of your NoQuiz role.
    - If user **HAVE** this role, they **WILL NOT** be able to participate in the quiz, also the stats wouldn't increase.
> [!CAUTION]
> Do not give arguments to both `{{$YesQuiz := ""}}` & `{{$NoQuiz := ""}}`. One must be empty, else it could produce unwanted errors.

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System/Code%20Files/Component-1.yag) and copy the code.
  - Create a New Custom command and paste the code:
    - Trigger Type: `Message Component`
    - Trigger: `quiz_`

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System/Code%20Files/Component-2.yag) and copy the code.
  - Create a New Custom command and paste the code:
    - Trigger Type: `Message Component`
    - Trigger: `quiz_`

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Quiz%20System/Code%20Files/Modal.yag) and copy the code.
  - Create a New Custom command and paste the code:
    - Trigger Type: `Modal Submission`
    - Trigger: `quiz_`

> [!INFO]
> Now, use the command `-quiz setup` to create a Database for this Quiz-System's "Strings" without this... Why the heck am i even writing this line!!!
---
### TODO
> ● All Completed!

### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
