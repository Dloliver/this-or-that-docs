# 💬 Slash Commands

This page documents **all available slash commands** for the **This or That** Discord bot.

All commands start with:

/tot

pgsql
Copy code

Some commands are available to everyone. Others require admin permissions or Premium access.

---

## 🔍 Command Overview

| Command | Description | Access |
|------|------------|-------|
| `/tot post` | Post a TOT now | Everyone |
| `/tot channel` | Set the channel for TOT posts | Admin |
| `/tot schedule` | Set when TOT posts (daily or weekly) | Admin |
| `/tot categories` | Manage enabled categories (set/add/remove/view) | Admin |
| `/tot toggle` | Toggle a single category on/off (quick) | Admin |
| `/tot mode` | Set question selection mode | Admin |
| `/tot pack` | Manage custom packs (create/list/activate/deactivate/delete) | Premium |
| `/tot question` | Add/remove/list questions in your custom packs | Premium |
| `/tot theme` | Manage Theme Days (mon..sun → theme tag) | Premium |

---

## 🆚 `/tot post`

Posts a question immediately.

### Usage
/tot post

yaml
Copy code

### Notes
- Uses your current server settings (mode/categories/packs/theme days)
- Posts in the configured channel

---

## 📢 `/tot channel` (Admin)

Sets the channel where TOT questions are posted.

### Usage
/tot channel

yaml
Copy code

### Notes
- Required for scheduled posting
- Also used by `/tot post`

---

## ⏰ `/tot schedule` (Admin)

Controls how often the bot posts automatically.

### Usage
/tot schedule

yaml
Copy code

### Notes
- Configure daily or weekly posting
- Scheduled posts go to the channel set by `/tot channel`

---

## 🗂️ `/tot categories` (Admin)

Manage which categories are enabled for your server.

### Usage
/tot categories

yaml
Copy code

### Notes
- Use this for full category management (set/add/remove/view)
- Affects both scheduled posts and manual `/tot post`

---

## ⚡ `/tot toggle` (Admin)

Quickly enable/disable a single category.

### Usage
/tot toggle

yaml
Copy code

### Notes
- Faster than `/tot categories` when you only need to flip one category

---

## 🎯 `/tot mode` (Admin)

Sets how questions are selected.

### Usage
/tot mode

yaml
Copy code

### Notes
- Determines how the bot chooses questions from enabled sources
- Applies to both scheduled posts and manual `/tot post`

---

## 📦 `/tot pack` (Premium)

Manage custom question packs.

### Usage
/tot pack

yaml
Copy code

### Notes
- Create, list, activate/deactivate, and delete packs
- Packs let you run fully custom question sets for your community

---

## ✏️ `/tot question` (Premium)

Manage questions inside your custom packs.

### Usage
/tot question

yaml
Copy code

### Notes
- Add/remove/list questions for a pack
- Best paired with `/tot pack`

---

## 🎨 `/tot theme` (Premium)

Manage Theme Days (Mon–Sun → theme tag).

### Usage
/tot theme

yaml
Copy code

### Notes
- Assign a theme to specific days
- Scheduled posts will follow the day’s theme when configured

---

## 🧠 How the Bot Chooses a Question

When posting, the bot typically follows this order:

1. Uses the configured posting channel
2. Applies Theme Day rules (if Premium and configured)
3. Filters by enabled categories
4. Includes active custom packs (if Premium)
5. Chooses a question using the configured mode
6. Posts it with reactions
