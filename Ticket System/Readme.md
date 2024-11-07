# Interactive Ticket System 

> This is a Ticket system but, it uses Buttons, Select Menus & Modals. This ticket system also has feature to close & re-open ticket without deleting the channel (like Ticket Tool bot).

## Features
- ✅ Feature 1 - Is Interactive. Uses Buttons, Select Menus & Modals for almost everything.
- ✅ Feature 2 - You can customize, what permissions you want to give to the ticket-owner (e.g. creator of the ticket):
  - `{{$PClose:= true}}`: Permission For Closing the ticket. *Default=True*
    - It removes Ticket-Owner from ticket. If users were added *with Select-Menu*, it'll remove them too.
  - `{{$POpen := true}}`: Permission For Re-Opening the ticket. *Default=True*
    - Added just for my own satisfaction but, can be good in some cases *maybe*.
  - `{{$PAddUser := false}}`: Permission For adding new users to the ticket. *Default=False*
  - `{{$PRemoveUser := false}}`: Permission For removing users from the ticket. *Default=False*
  - `{{$PRename := true}}`: Permission For Renaming the ticket, also edits the Subject & Compose of Top-Message. *Default=True*
  - `{{$PAdminOnly := true}}`: Permission For if Ticket-Owner can convert ticket to AdminOnly or not. *Default=True*
  - `{{$PUseSettings := true}}`: Permission For using the “⚙️ Settings” button. *Default=True*
  - `{{$PDelete := false}}`: Permission For deleting the ticket. *Default=False*
  - > NOTE: Here, "DELETE" Means Deleting the Ticket-Channel & "CLOSE" Means just removing the Ticket-Owner and Added Users from the Ticket-Channel.
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
#### Setup:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_194902.png)

#### Creating a Ticket:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195303.png)

#### Bot message in the newly created ticket channel:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195345.png)

#### Interface of the “⚙️ Settings” button:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195434.png)

#### Bot message when you clicks on “🔒 Close” button:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195452.png)

#### Form / Modal, when you clicks on “⛔ Delete" button:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195700.png)

#### Embed & an attachment *With White Embed.Color*, Have information about the deleted ticket:
![IMAGE](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Assets/Screenshot_2024_1107_195740.png)
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

- [Click Here](https://github.com/YourFriendSub/YAGPDB.xyz-CCs/blob/main/Ticket%20System/Code%20Files/Modal.yag) and copy the code.
  - Create a New Custom command with and paste the code:
    - Trigger Type: `Modal Submission`
    - Trigger: `cticket_`
  - Replace the `00000` in `{{$LogsChannel := 00000}}` variable with ID of your Logs-Channel
    - *Don't know how to copy Channel-ID? You shouldn't own a server.* Just kidding, you can ask this in official support server or just google it.

---
### TODO
> ○ Add an Info button in Settings
