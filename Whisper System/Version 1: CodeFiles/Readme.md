# Whisper System — README Headers

Pick one header per version. Each section has 3 different styles to choose from.

---
---

## ═══ VERSION 1 ═══

---

### ▶ Option A — Centered + Badges

```md
<div align="center">

# 🔒 Whisper System

![Version](https://img.shields.io/badge/Version-1-7F77DD?style=flat-square)
![Recipients](https://img.shields.io/badge/Recipients-1-gray?style=flat-square)
![Files](https://img.shields.io/badge/Files-2_.yag-gray?style=flat-square)
![Expiry](https://img.shields.io/badge/Expiry-15%20min-orange?style=flat-square)

**A private messaging system for Discord — no DMs required.**

Send a secret message to any user. A button appears in chat — only *they* can reveal it. Everyone else gets blocked. Message self-destructs after 15 minutes.

</div>

---
```

---

### ▶ Option B — Minimal with command preview

```md
# 🔒 Whisper System `v1`

> Send a private message to any user — without ever opening DMs.
> Only the intended recipient can reveal it. Expires in 15 minutes.

```
-whisper @User Your private message here
```

| | |
|---|---|
| 👤 **Recipients** | 1 user per whisper |
| 🔘 **Reveal** | Ephemeral button click |
| ⏰ **Expiry** | 15 min · configurable |
| 🗑️ **Trigger** | Auto-deleted |
| 📁 **Files** | `Command.yag` · `Component.yag` |
```

---

### ▶ Option C — Feature list with accent

```md
# 💬 Whisper System
### Version 1 — Basic

A one-to-one private messaging custom command for YAGPDB.xyz.
The sender's message is deleted, replaced by a button — only the chosen user can see what's inside.

**Features**
- 👤 Single-recipient whisper
- 🔘 Button-reveal (ephemeral — only recipient sees it)
- 🙅 Access control — others get "This message isn't for you"
- ⏰ Auto-expires after 15 minutes *(configurable)*
- 🗑️ Trigger message auto-deleted on send
- 🎨 Random color embed per whisper
- 📁 2 files: `Command.yag` + `Component.yag`

---
```

---
---

## ═══ VERSION 2 ═══

---

### ▶ Option A — Centered + Badges

```md
<div align="center">

# 🔒 Whisper System

![Version](https://img.shields.io/badge/Version-2-1D9E75?style=flat-square)
![Recipients](https://img.shields.io/badge/Recipients-Multiple-green?style=flat-square)
![Files](https://img.shields.io/badge/Files-2_.yag-gray?style=flat-square)
![Expiry](https://img.shields.io/badge/Expiry-Live%20countdown-orange?style=flat-square)
![New](https://img.shields.io/badge/New-Multi--user-brightgreen?style=flat-square)

**Whisper to multiple users at once — with a live expiry countdown in the embed.**

</div>

---
```

---

### ▶ Option B — Minimal with command preview

```md
# 🔒 Whisper System `v2` — Multi-user

> Send one whisper to multiple users at the same time.
> A live countdown shows exactly when the message expires.

```
-whisper @User1 @User2 & Your private message here
```

| | |
|---|---|
| 👥 **Recipients** | Multiple users per whisper |
| 🔘 **Reveal** | Ephemeral button click |
| ⏰ **Expiry** | Configurable · displayed as live countdown |
| 🆕 **New in v2** | Multi-recipient · expiry timestamp · improved errors |
| 📁 **Files** | `Command.yag` · `Component.yag` |
```

---

### ▶ Option C — Feature list with accent

```md
# 💬 Whisper System
### Version 2 — Multi-recipient

Upgraded from v1. Send a single whisper to multiple users at once — and let them see a live countdown timer ticking toward expiry right inside the embed.

**What's new in v2**
- 👥 **Multi-recipient** — mention as many users as you want
- ⏰ **Live expiry timer** — shows `<t:timestamp:R>` relative countdown
- 🆕 **New syntax** — `@User1 @User2 & message` using `&` as separator
- 🛡️ **Improved error handling** — cleaner `try/catch` with user-facing errors
- 📁 2 files: `Command.yag` + `Component.yag`

---
```

---
---

## ═══ VERSION 3 ═══

---

### ▶ Option A — Centered + Badges

```md
<div align="center">

# 🔒 Whisper System

![Version](https://img.shields.io/badge/Version-3-185FA5?style=flat-square)
![Recommended](https://img.shields.io/badge/-Recommended-185FA5?style=flat-square)
![Recipients](https://img.shields.io/badge/Recipients-Up%20to%205-green?style=flat-square)
![Input](https://img.shields.io/badge/Input-Modal%20%28mod--proof%29-blueviolet?style=flat-square)
![Files](https://img.shields.io/badge/Files-3_.yag-gray?style=flat-square)
![Views](https://img.shields.io/badge/Max%20Views-Configurable-orange?style=flat-square)

**The most advanced version — modal-powered, mod-proof, and fully configurable.**

> ⭐ Use this version. People with modded Discord clients **cannot** intercept the message, because it's sent through a modal — never typed in chat.

</div>

---
```

---

### ▶ Option B — Minimal with flow

```md
# 🔒 Whisper System `v3` ⭐ Recommended

> The full redesign. Input goes through a Discord modal, so it's invisible even to modded clients.
> Select up to 5 recipients from a dropdown, configure expiry, set max views, and attach media links.

**How it works**

`Select users` → `Fill modal` → `Whisper delivered` → `Recipient reveals` → `Expires`

| | |
|---|---|
| 👥 **Recipients** | Up to 5 via select menu |
| 🔒 **Input** | Discord modal *(mod-proof)* |
| ⏰ **Expiry** | Custom duration e.g. `03h27m9s` |
| 👁️ **Max views** | Configurable *(default: 100)* |
| 🔗 **Media links** | Up to 4 per whisper |
| 🛡️ **Invite filter** | Auto-strips Discord invites |
| 📁 **Files** | `Command.yag` · `Component.yag` · `Modal.yag` |
```

---

### ▶ Option C — Feature list with accent

```md
# 💬 Whisper System
### Version 3 — Full Redesign ⭐ Recommended

A complete overhaul of the whisper system. The message is entered through a **Discord modal** — it never appears in chat at all, making it invisible to even modded Discord clients. Choose up to 5 recipients from a dropdown, customize expiry and view limits, and attach media links.

**Features**
- 🔒 **Modal input** — text never typed in chat; mod-proof by design
- 👥 **Up to 5 recipients** — chosen from a user select menu
- ⏰ **Custom expiry** — set any duration (e.g. `1h30m`, `03h27m9s`)
- 👁️ **Max views** — limit how many times the whisper can be read *(default: 100)*
- 🔗 **Media links** — attach up to 4 links per whisper
- 🛡️ **Invite link filter** — optionally strips Discord invite links from messages
- 📁 3 files: `Command.yag` + `Component.yag` + `Modal.yag`

---
```
