<div align="center">

# 🏆 NOTIFY

### _Never Miss Another Contest — The Ultimate CP Enthusiast's Companion_

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-notify--snowy.vercel.app-6C63FF?style=for-the-badge)](https://notify-snowy.vercel.app/)
[![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)](https://web.dev/progressive-web-apps/)

<br/>

> _"In competitive programming, timing is everything. Notify ensures you never miss your shot at glory."_

**[🚀 Try Live Demo](https://notify-snowy.vercel.app/)** · **[📱 Install as PWA](https://notify-snowy.vercel.app/sign-in)** · **[🐛 Report a Bug](https://github.com/Himaanshuuuu04/Notify/issues)** · **[✨ Request a Feature](https://github.com/Himaanshuuuu04/Notify/issues)**

</div>

---

## 📖 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Tech Stack](#️-tech-stack)
- [Architecture](#-architecture)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [API Reference](#-api-reference)
- [Cron Jobs](#-cron-jobs)
- [Docker](#-docker)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Team](#-team)

---

## 🎯 About

**Notify** is a full-stack Progressive Web App built for competitive programmers who want to stay ahead of every contest across **CodeChef**, **Codeforces**, and **LeetCode** — all from a single, elegant dashboard.

Notify solves the real frustration of:
- Scattered contest schedules across multiple platforms
- Forgetting to register for contests at the last minute
- Having no single view for tracking your friends' performance

With Notify, you get a personalized, notification-driven experience that keeps you focused on what matters — **solving problems, not missing contests**.

---

## ✨ Features

### 🔔 Smart Notification System
- **Email Reminders** — Receive alerts 30–60 minutes and 24 hours before a contest starts
- **Browser Push Notifications** — Get notified even when the app isn't open (PWA-powered)
- **One-click Unsubscribe** — Secure token-based unsubscribe from any email
- **Customizable Per-Platform** — Toggle reminders for LeetCode, Codeforces, and CodeChef independently

### 📊 Multi-Platform Contest Dashboard
| Platform | Coverage |
|----------|----------|
| **LeetCode** | Weekly & Biweekly Contests |
| **Codeforces** | Div 1, Div 2, Div 3, Educational, Global Rounds |
| **CodeChef** | Long Challenges, Cook-offs, Starters |
| **Coming Soon** | AtCoder, TopCoder, HackerRank |

### 🕵️ Friend Stalker
- Add friends by their platform handle (LeetCode / Codeforces)
- Track their ratings, ranks, and contest history
- Powered by [Tashif Khan's Stats APIs](https://github.com/Tashifkhan)

### 🔐 Full Auth System
- Email/password sign-up with **OTP-based email verification**
- **Forgot password** flow with secure reset codes
- JWT session management via **NextAuth**
- Route protection via Next.js middleware

### ⚡ PWA Superpowers
- **Install on any device** — desktop or mobile, from any browser
- **Offline-first** with service worker caching
- **Native app feel** — no address bar, smooth transitions

---

## 🛠️ Tech Stack

### Frontend
![Next.js](https://img.shields.io/badge/-Next.js_15-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/-React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/-Tailwind_CSS_v4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Framer Motion](https://img.shields.io/badge/-Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![Radix UI](https://img.shields.io/badge/-Radix_UI-161618?style=flat-square&logo=radix-ui&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/-shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)
![PWA](https://img.shields.io/badge/-PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)

### Backend & Data
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/-Mongoose-880000?style=flat-square&logo=mongoose&logoColor=white)
![NextAuth](https://img.shields.io/badge/-NextAuth.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Nodemailer](https://img.shields.io/badge/-Nodemailer-009DFF?style=flat-square&logo=gmail&logoColor=white)
![React Email](https://img.shields.io/badge/-React_Email-000000?style=flat-square&logo=react&logoColor=white)

### Forms & Validation
![React Hook Form](https://img.shields.io/badge/-React_Hook_Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white)
![Zod](https://img.shields.io/badge/-Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)

### Dev & Infra
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Turbopack](https://img.shields.io/badge/-Turbopack-000000?style=flat-square&logo=next.js&logoColor=white)

---

## 🏗️ Architecture

```
notify/
├── src/
│   ├── app/
│   │   ├── (auth)/              # Sign-in, Sign-up, Verify pages
│   │   ├── (pages)/             # Protected: Dashboard, Contests, Settings, About
│   │   │   ├── dashboard/
│   │   │   ├── contests/
│   │   │   ├── settings/
│   │   │   └── guest-dashboard/
│   │   ├── api/
│   │   │   ├── auth/            # NextAuth [...nextauth] handler
│   │   │   ├── sign-up/         # User registration + OTP dispatch
│   │   │   ├── verify-code/     # OTP verification
│   │   │   ├── forgot-pass/     # Password reset code dispatch
│   │   │   ├── reset-pass/      # Password reset handler
│   │   │   ├── get-contests/    # Fetch contests from DB
│   │   │   ├── update-contest/  # [CRON] Sync contests from platforms
│   │   │   ├── send-reminders/  # [CRON] Dispatch email/push reminders
│   │   │   ├── set-reminder/    # User reminder preferences
│   │   │   ├── get-reminders/   # Fetch user's active reminders
│   │   │   ├── change-settings/ # Update notification preferences
│   │   │   ├── add-friend/      # Add a platform friend
│   │   │   ├── get-friends/     # Fetch friends list
│   │   │   ├── remove-friend/   # Remove a friend
│   │   │   ├── check-friend/    # Check if friend exists
│   │   │   ├── check-username-unique/
│   │   │   └── unsubscribe/     # Token-based email unsubscribe
│   │   └── unsubscribed/        # Unsubscribe success/error pages
│   ├── components/              # Reusable UI components
│   │   ├── contest-card.tsx
│   │   ├── friend-stalker.tsx
│   │   ├── contest-filters.tsx
│   │   └── ...
│   ├── model/
│   │   ├── User.ts              # User schema (auth, preferences, friends)
│   │   ├── Contest.ts           # Contest schema
│   │   └── Reminder.ts         # Reminder schema
│   ├── helpers/
│   │   └── sendVerificationEmail.ts
│   ├── schemas/                 # Zod validation schemas
│   ├── hooks/                   # Custom React hooks
│   ├── context/                 # React context providers
│   ├── types/                   # Shared TypeScript types
│   └── middleware.ts            # Auth-based route protection
├── emails/                      # React Email templates
├── scripts/
│   ├── send-announcement.mjs    # Bulk announcement mailer
│   └── migrate-unsubscribe-tokens.mjs
├── Dockerfile
└── public/                      # Static assets + PWA manifest
```

### Data Flow

```
Browser → Next.js Middleware (JWT check)
              ↓
        Next.js API Routes
              ↓
        Mongoose → MongoDB Atlas
              ↓
    Nodemailer (Gmail SMTP) → User Inbox

Cron Scheduler → /api/update-contest → Fetch platforms → Store in MongoDB
Cron Scheduler → /api/send-reminders → Query upcoming contests → Send emails/push
```

---

## 🚀 Getting Started

### Prerequisites

```
✅ Node.js 18+
✅ A MongoDB instance (Atlas free tier works great)
✅ A Gmail account with an App Password
✅ A modern browser with PWA support
```

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Himaanshuuuu04/Notify.git
cd Notify
```

### 2️⃣ Install dependencies

```bash
# npm (recommended)
npm install

# or bun (faster)
bun install
```

### 3️⃣ Set up environment variables

Create a `.env.local` file in the project root:

```bash
# MongoDB
MONGODB_URI=mongodb+srv://<user>:<password>@cluster.mongodb.net/notify

# NextAuth — generate with: openssl rand -base64 32
NEXTAUTH_SECRET=your_strong_random_secret
NEXTAUTH_URL=http://localhost:3000

# Nodemailer (Gmail)
NODEMAILER_EMAIL=your_gmail_address@gmail.com
NODEMAILER_PASS=your_gmail_app_password
```

> **Note:** For `NODEMAILER_PASS`, create a [Google App Password](https://myaccount.google.com/apppasswords) — do not use your regular Gmail password.
> Never commit `.env.local` to version control.

### 4️⃣ Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. The app uses **Turbopack** for fast HMR.

### 5️⃣ Build for production

```bash
npm run build
npm start
```

---

## 🔑 Environment Variables

| Variable | Required | Description |
|---|---|---|
| `MONGODB_URI` | ✅ | MongoDB connection string |
| `NEXTAUTH_SECRET` | ✅ | Secret for JWT signing & encryption |
| `NEXTAUTH_URL` | ✅ | Canonical URL of your deployment |
| `NODEMAILER_EMAIL` | ✅ | Gmail address used as the sender |
| `NODEMAILER_PASS` | ✅ | Gmail App Password for the sender account |

---

## 📡 API Reference

All routes are under `/api/`. Protected routes require a valid NextAuth session.

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/api/sign-up` | Public | Register a new user & send OTP |
| `POST` | `/api/verify-code` | Public | Verify email OTP |
| `POST` | `/api/forgot-pass` | Public | Send password reset code |
| `POST` | `/api/reset-pass` | Public | Reset password with code |
| `GET` | `/api/get-contests` | 🔒 | Fetch contests from DB |
| `GET` | `/api/update-contest` | Cron | Sync latest contests from platforms |
| `GET` | `/api/send-reminders` | Cron | Send email/push reminders |
| `POST` | `/api/set-reminder` | 🔒 | Set reminder for a contest |
| `GET` | `/api/get-reminders` | 🔒 | Get user's active reminders |
| `POST` | `/api/change-settings` | 🔒 | Update notification preferences |
| `POST` | `/api/add-friend` | 🔒 | Add a friend by platform handle |
| `GET` | `/api/get-friends` | 🔒 | Fetch friends list |
| `DELETE` | `/api/remove-friend` | 🔒 | Remove a friend |
| `GET` | `/api/check-username-unique` | Public | Check username availability |
| `GET` | `/api/unsubscribe` | Token | Unsubscribe from email notifications |

---

## ⏰ Cron Jobs

Notify uses two automated API endpoints that should be hit on a schedule:

### `/api/update-contest` — Contest Sync
- Fetches latest contests from CodeChef, Codeforces, and LeetCode
- Detects newly added contests
- Dispatches contest announcement emails to subscribed users
- **Recommended schedule:** Every 6 hours — `0 */6 * * *`

### `/api/send-reminders` — Reminder Dispatch
- Sends reminders for contests starting in the **next 30–60 minutes**
- Sends 24-hour advance reminders for contests starting in **23h30m–24h**
- **Recommended schedule:** Every 30 minutes — `*/30 * * * *`

### Vercel Cron (vercel.json)

```json
{
  "crons": [
    { "path": "/api/send-reminders", "schedule": "*/30 * * * *" },
    { "path": "/api/update-contest",  "schedule": "0 */6 * * *"  }
  ]
}
```

### Other Schedulers

Any HTTP GET to these endpoints will trigger the job. Works with:
- **GitHub Actions** scheduled workflows
- **Cron-job.org** (free tier available)
- **UptimeRobot** monitor pings
- **EasyCron**, **Render Cron Jobs**, etc.

---

## 🐳 Docker

Run Notify without installing Node.js locally.

### Prerequisites
- [Docker](https://www.docker.com/get-started) installed

### 1️⃣ Prepare environment

Create a `.env` file in the project root with your secrets (see [Environment Variables](#-environment-variables)).

### 2️⃣ Build the image

```bash
docker build -t notify-app .
```

### 3️⃣ Run the container

```bash
docker run -p 3000:3000 --env-file .env notify-app
```

App will be available at [http://localhost:3000](http://localhost:3000).

### 4️⃣ Docker Compose (optional)

```yaml
version: "3.8"
services:
  app:
    build: .
    ports:
      - "3000:3000"
    env_file:
      - .env
    environment:
      - NODE_ENV=production
    restart: unless-stopped
```

```bash
docker-compose up -d
```

---

## 🔮 Roadmap

### ✅ Phase 1 — Current
- [x] CodeChef, Codeforces, LeetCode integration
- [x] OTP-based email verification
- [x] Email & browser push notifications
- [x] Friend stalker (LeetCode + Codeforces)
- [x] PWA with offline support
- [x] Cron job automation
- [x] Docker support
- [x] Secure token-based unsubscribe

### 🔄 Phase 2 — In Progress
- [ ] AtCoder & TopCoder integration
- [ ] Contest performance analytics
- [ ] Social features — follow friends, share results

### 🎯 Phase 3 — Future
- [ ] AI-powered contest recommendations
- [ ] Mobile app (React Native)
- [ ] Team contest coordination
- [ ] Live contest tracking dashboard
- [ ] IDE plugin integrations

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place. Any contributions you make are **greatly appreciated**.

1. Fork the repository
2. Create your feature branch: `git checkout -b feat/amazing-feature`
3. Commit your changes: `git commit -m 'feat: add some amazing feature'`
4. Push to the branch: `git push origin feat/amazing-feature`
5. Open a Pull Request

Please follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages.

### Areas We'd Love Help With
- 🌐 New platform integrations (AtCoder, TopCoder, HackerRank)
- 🐛 Bug reports and fixes
- 📖 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Tests

---

## 🙏 Special Thanks

A huge shoutout to [**Tashif Khan**](https://github.com/Tashifkhan) for generously providing the APIs that power contest data fetching and friend stalking features:

- [LeetCode Stats API](https://leetcode-stats.tashif.codes/)
- [Codeforces Stats API](https://codeforces-stats.tashif.codes/)

---

## 👥 Team

Built with 💻 by three competitive programmers who got tired of missing contests:

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/vansh1233">
        <img src="https://github.com/vansh1233.png" width="80px;" alt="Vansh"/><br/>
        <sub><b>Vansh</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Himaanshuuuu04">
        <img src="https://github.com/Himaanshuuuu04.png" width="80px;" alt="Himanshu"/><br/>
        <sub><b>Himanshu</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/ShauryaRahlon">
        <img src="https://github.com/ShauryaRahlon.png" width="80px;" alt="Shaurya"/><br/>
        <sub><b>Shaurya</b></sub>
      </a>
    </td>
  </tr>
</table>

---

<div align="center">

**⭐ Star this repo if Notify saves you from missing a contest!**

[![GitHub stars](https://img.shields.io/github/stars/Himaanshuuuu04/Notify?style=social)](https://github.com/Himaanshuuuu04/Notify/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Himaanshuuuu04/Notify?style=social)](https://github.com/Himaanshuuuu04/Notify/network/members)

_Helping competitive programmers focus on what matters most — solving problems, not missing contests._

</div>
