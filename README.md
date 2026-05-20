[README.md](https://github.com/user-attachments/files/28066992/README.md)
# 🗺️ Treasure Hunt — Phil's 30th Birthday Hunt

A mobile-first scavenger hunt app built as a single HTML file. Three groups start at different locations across East London and follow a series of digital clues to find Phil.

## Live App

Hosted on GitHub Pages — share this URL with your groups on the day:
```
https://[yourusername].github.io/treasure-hunt
```

## How It Works

- **Players** open the URL on their phone, select their route and enter the password
- **Clues** unlock one at a time across 8 different formats (Instagram, Hacker terminal, iMessage, Safari article, Voicemail, Reddit, Time Machine, Gig Poster)
- **Messages** from story characters arrive between clues, advancing the narrative and requiring a keyword reply to unlock the next clue
- **Progress** is saved automatically — if the phone closes or the tab refreshes, the hunt picks up exactly where it left off
- **Leaderboard** updates live across all three phones so every group can see how the others are doing

## Admin Panel

Access via the lock screen → **Admin panel** button. Password is set in Admin → Settings.

From the admin panel you can:
- Edit all clue content (questions, answers, hints, images, audio)
- Set up story messages per route with custom senders, reply keywords and help text
- Edit the group chat messages per route
- Set the hunt start time (teams see a countdown until it begins)
- Send live broadcasts to all teams
- Monitor all three routes' progress in real time
- Reset routes before the hunt starts
- Approve or reject extra hint requests

All admin changes save to Firebase automatically and are live across all devices instantly.

## Technical

- **Single HTML file** — no build step, no dependencies to install
- **Firebase Realtime Database** — admin config and player progress synced live across all devices
- **localStorage** — fast local backup so progress survives tab closure even without signal
- **Works on** — iPhone Safari, Android Chrome, any modern mobile browser

## Firebase

Data is stored at:
```
treasure-hunt-f74b7-default-rtdb.europe-west1.firebasedatabase.app
```
```
admin/          ← all admin config (routes, clues, story messages, settings)
broadcasts/     ← live broadcasts sent to all teams
progress/       ← per-route player progress (clues solved, hints, replies)
```

## Before the Hunt

1. Open the live URL and log into admin
2. Fill in all clue content, story messages, and group chats per route
3. Set the hunt start time in Admin → Settings
4. Turn Demo Mode off in Admin → Settings
5. On the day: reset all three routes from Admin → Overview
6. Share the URL and route passwords with your groups

## Route Passwords (defaults — change in admin)

| Route | Password |
|-------|----------|
| Route A | routeA2026 |
| Route B | routeB2026 |
| Route C | routeC2026 |
| Admin | TreasureAdmin2026! |

> ⚠️ Change all passwords in Admin → Settings before the event.
