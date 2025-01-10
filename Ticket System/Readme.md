# Interactive Ticket System 
> This is a Ticket system but, it uses Buttons, Select Menus & Modals. This ticket system also has feature to close & re-open ticket without deleting the channel (like Ticket Tool bot).
- [Jump To Installation](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System#Installation) or Just Scroll Down.
> P.S. English isn't my First Language.

## Features
- ✅ Feature 1 - Is Interactive. Uses Buttons, Select Menus & Modals for almost everything.
- ✅ Feature 2 - You can customize, what permissions you want to give to the ticket-owner (e.g. creator of the ticket):
  - `{{$PClose:= true}}`: Permission For Closing the ticket. *Default=True*
    - It removes Ticket-Owner from ticket. If users were added, it'll remove them too.
  - `{{$POpen := true}}`: Permission For Re-Opening the ticket. *Default=True*
    - Added just for my own satisfaction but, can be good in some cases *maybe*.
  - `{{$PAddUser := false}}`: Permission For adding new users to the ticket. *Default=False*
  - `{{$PRemoveUser := false}}`: Permission For removing users from the ticket. *Default=False*
  - `{{$PRename := true}}`: Permission For Renaming the ticket, also edits the Subject & Compose of Top-Message. *Default=True*
  - `{{$PAdminOnly := true}}`: Permission For if Ticket-Owner can convert ticket to AdminOnly or not. *Default=True*
  - `{{$PUseSettings := true}}`: Permission For using the “⚙️ Settings” button. *Default=True*
  - `{{$PDelete := false}}`: Permission For deleting the ticket. *Default=False*

  > NOTE:
    - These permissions only overrides the permissions for Buttons, Select Menus & Modals. Ticket-Owner *or others* can still use inbuilt `-ticket` commands.
    - "DELETE" Means Deleting the Ticket-Channel & "CLOSE" Means just removing the Ticket-Owner and Added Users from the Ticket-Channel.
- ✅ Featere 3 - Additional features:
  - If you want to Pin the Top-Message (e.g. First message that was Sent by bot.) of the Ticket. *Default=True*
  - If you want to Ping Staff role or not. *Default=True*
  - Ticket-Creator can add a Compose/Explanation for making ticket.
  - Sends a Embed on ticket deletation to Log-Channel with details like:
    - Subject of the Ticket as Embed title.
    - Compose of the Ticket as Embed Description.
    - Channel ID of the ticket in the Info Field of embed.
    - Mention of Ticket Owner in the Info Field of embed.
    - Mention of user, who deleted the ticket.
  - More Features Coming Soon...

---

## Demo
<details>
<summary>Setup</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_194902.png" alt="Setup Screenshot" width="600">
</details>

<details>
<summary>Creating a Ticket</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195303.png" alt="Creating a Ticket Screenshot" width="600">
</details>

<details>
<summary>Bot message in the newly created ticket channel</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195345.png" alt="New Ticket Channel Screenshot" width="600">
</details>

<details>
<summary>Interface of the “⚙️ Settings” button</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195434.png" alt="Settings Button Screenshot" width="600">
</details>

<details>
<summary>Bot message when you click on “🔒 Close” button</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195452.png" alt="Close Button Screenshot" width="600">
</details>

<details>
<summary>Form / Modal when you click on “⛔ Delete" button</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195700.png" alt="Delete Modal Screenshot" width="600">
</details>

<details>
<summary>Embed & an attachment *With White Embed.Color*, with information about the deleted ticket</summary>
<img src="https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195740.png" alt="Deleted Ticket Info Screenshot" width="600">
</details>

---

## Installation

### Needs
- A dedicated Moderator-Role (Or Ticket-Moderator Role?)
- A channel, for logging the ticket - *post ticket-deletation logs*

### Setup
- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Code%20Files/Ticket.yag) and copy the code.
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

> ○ Add an Info button in Settings.
### Support
- For any assistance regarding my code, You can contact me in my testing Discord Server [Qwerty](https://discord.com/invite/2gjARJxh9V).
- For any assistance regarding YAGPDB.xyz Bot, You can contact their support team at their Official Discord Server [YAGPDB Community & Support](https://discord.com/invite/Yagpdb).
