# Interactive Ticket System 

> This is a Ticket system but, it uses Buttons, Select Menus & Modals. This ticket system also has feature to close ticket without deleting (like Ticket Tool bot).

## Features
- ✅ Feature 1 - Is Interactive. Uses Buttons, Select Menus & Modals for almost everything.
- ✅ Feature 2 - You can customize, what permissions you want to give to the ticket-owner (e.g. creator of the ticket).
  - `{{$PClose:= true}}`: Permission For Closing the ticket. *Default=True*
    - It removes Ticket-Owner from ticket. If users were added *with Select-Menu*, it'll remove them too.
  - `{{$POpen := true}}`: Permission For Re-Opening the ticket. *Default=True*
    - Added just for my own satisfaction but, can be good in some cases *maybe*.
  - `{{$PAddUser := false}}`: Permission For adding new users to the ticket. *Default=False*
  - `{{$PRemoveUser := false}}`: Permission For removing users from the ticket. *Default=False*
  - `{{$PRename := true}}`: Permission For Renaming the ticket. *Default=True*
  - `{{$PAdminOnly := true}}`: Permission For if Ticket-Owner can convert ticket to AdminOnly or not. *Default=True*
  - `{{$PUseSettings := true}}`: Permission For using the “⚙️ Settings” button. *Default=True*
  - `{{$PDelete := false}}`: Permission For deleting the ticket. *Default=False*
  - > NOTE: Here, "DELETE" Means Deleting the Ticket Channel & "CLOSE" Means just removing Ticket-Owner and Added Users.
- ✅ Featere 3 - Additional feature, if any
- 📈 Analytics or specific metrics related to this project

---

## Demo
![Demo](https://user-images.githubusercontent.com/yourusername/demo.gif)
> You can include a GIF or image showcasing the project here.

---

## Installation

### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version >= 14)
- [Git](https://git-scm.com/)
- Any other dependencies or tools

### Clone the Repository
```bash
git clone https://github.com/yourusername/your-repository.git
cd your-repository
