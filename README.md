# starlog 🛰️

> a voice logger for remote teams. sixty seconds to stay in sync.

Starlog is a mobile app that reimagines the daily standup as a voice-first, async experience. Team members record a 60-second voice update each day — it gets auto-transcribed, organized, and made searchable. No meetings. No noise. Just signal.

---

## the idea

Daily standups exist for two reasons — accountability and visibility. But text-based tools make them feel like chores. Starlog makes it as easy as leaving a voice note. Your team hears your update. Your manager sees the blockers. Everyone stays in sync.

---

## features

- 🎙️ **Voice recording** — 60-second daily standup prompted by three questions
- 📝 **Auto-transcription** — powered by AssemblyAI Universal-2
- 🔍 **Searchable history** — find any update by person, date, or keyword
- 🚨 **Blocker detection** — blockers are surfaced and flagged automatically
- 👥 **Team feeds** — see your whole team's updates organized by day
- 🔔 **Notifications** — daily reminders to keep your team on track
- 💬 **Slack integration** — updates posted directly to your team channel

---

## tech stack

| Layer | Technology |
|-------|-----------|
| Framework | Flutter |
| State Management | GetX |
| Backend | deepspace (NestJS) |
| Auth | OTP via email |

---

## screens

- Onboarding & account creation
- Create or join a team via invite code
- Home — daily recorder with team toggle
- Team feed — updates by person and date
- Search — full-text search across all standups
- Settings — profile, notifications, linked accounts

---

## roles

| Role | Description |
|------|-------------|
| **Poster** | Records and submits daily voice updates |
| **Watcher** | Reviews team updates and monitors blockers |

> Every user can be both — role is determined per team, not per account.

---

## getting started

### prerequisites
- Flutter SDK `>=3.0.0`
- Dart `>=3.0.0`
- A running instance of [deepspace](https://github.com/Lukas-io/deepspace)

### setup

```bash
# clone the repo
git clone https://github.com/Lukas-io/starlog.git
cd starlog

# install dependencies
flutter pub get

# set up environment
cp .env.example .env
# fill in your deepspace API URL

# run the app
flutter run
```

---

## environment variables

```env
API_BASE_URL=http://localhost:3000
SLACK_REDIRECT_URI=your_slack_redirect_uri
```

---

## project structure

```
lib/
├── core/           # constants, theme, utils
├── data/           # models, repositories, API clients
├── modules/        # feature modules (GetX structure)
│   ├── auth/
│   ├── home/
│   ├── recording/
│   ├── team/
│   └── settings/
└── main.dart
```

---

## companion

This app is powered by **deepspace** — the NestJS backend that handles transcription, storage, team management, and Slack integration.

→ [deepspace repository](https://github.com/Lukas-io/deepspace)

---

## status

🚧 Active development — portfolio project by [@Lukas-io](https://github.com/Lukas-io)