# 🤖 Mini Jarvis Backend — AI Hackathon 2025

Backend service that powers the Mini Jarvis automation system, including Google Calendar integration, email automation, and Twitter/X assistant.

> **Project:** AI Creation Hackathon 2025  
> **Status:** Active Development  
> **Visibility:** Public Fork  
> **Created:** November 10, 2025 | **Last Updated:** November 21, 2025

---

## 📋 Executive Summary

Mini Jarvis is an intelligent automation backend service that leverages multiple AI APIs and integrations to create a cohesive system for:

- **📅 Calendar Intelligence** — Automated Google Calendar management
- **📧 Smart Communications** — AI-powered email automation  
- **𝕏 Social Media Presence** — Twitter/X bot integration
- **🧠 Content Generation** — Natural language processing for intelligent task execution

This is a Node.js-based Express server designed as a hackathon submission combining multiple APIs (Google, Twitter, GROQ AI, Prisma ORM) into a unified automation platform.

---

## 🚀 How to Start

### Installation
```bash
npm install
```

### Run Application
```bash
node ./src/app.js
```

The server will start on `PORT 3000` (configurable via environment variables).

---

## ⚙️ Environment Variables

Create a `.env` file inside the root directory with the following configuration:

```env
# Server Config
SERVER_HOST=smtp.gmail.com
SERVER_EMAIL=your-email@gmail.com
SERVER_PASSWORD=your-app-password
ADMINISTRATOR_1=admin@email.com
PORT=3000

# Google OAuth & Service Account (for Calendar & Email)
GOOGLE_CLIENT_ID=your-client-id
GOOGLE_CLIENT_SECRET=your-client-secret
GOOGLE_REDIRECT_URI=your-google-redirect-uri
GOOGLE_REFRESH_TOKEN=your-google-refresh-token
GOOGLE_SERVICE_ACCOUNT_KEY=path/to/service-account.json

# Twitter / X API
TWITTER_APP_KEY=your-twitter-api-key
TWITTER_APP_SECRET=your-twitter-secret
TWITTER_ACCESS_TOKEN=your-access-token
TWITTER_REFRESH_TOKEN=your-refresh-token

# GROQ
GROQ_API_KEY=your-groq-api-key

# Database
DATABASE_URL="postgresql://postgres:aaa@103.197.191.148:5432/appdb?schema=public"
```

> **⚠️ IMPORTANT:** Never expose your credentials publicly. Use environment variables and secure vaults instead.

---

## 📦 Features

- ✅ **Google Calendar Automation** — OAuth2 authentication, event management, service account integration
- ✅ **Smart Email Automation** — Gmail SMTP integration, Nodemailer for reliable delivery
- ✅ **Twitter/X Bot Integration** — API v2 support, automated posting, real-time management
- ✅ **Natural Language Intent Processing** — GROQ API-powered AI responses, GPT-OSS-120B backend
- ✅ **Activity Scheduler** — Cron-based task scheduling, periodic automation, background execution

---

## 🔧 Technology Stack

### Backend Framework
- **Express.js** v5.1.0 — Web server framework
- **Node.js** — Runtime environment

### Database & ORM
- **PostgreSQL** — Relational database
- **Prisma** v6.19.0 — Database ORM and schema management

### AI & Language Models
- **GROQ SDK** v0.34.0 — AI/LLM integration (GPT-OSS-120B)

### Integrations & APIs
- **Google APIs** v165.0.0 — Calendar and Gmail automation
- **Twitter API v2** v1.27.0 — Social media integration
- **SerpAPI** v2.2.1 — Web search capabilities

### Utilities & Tools
- **Nodemailer** v7.0.10 — SMTP email service
- **Node Cron** v4.2.1 — Task scheduling
- **Luxon** v3.7.2 — Date/time utilities
- **EJS** v3.1.10 — Template engine
- **CORS** v2.8.5 — Cross-origin resource sharing
- **Dotenv** v17.2.3 — Environment variable management

### Language Composition
- **JavaScript:** 55.9%
- **Jupyter Notebook:** 31.1% (AI Media Factory experiments)
- **EJS:** 13%

---

## 📁 Project Structure

```
smartaihackathonlocalgpt/
├── src/
│   ├── app.js                 # Main Express application entry point
│   ├── routes/
│   │   └── web.routes.js      # Route definitions
│   ├── services/
│   │   └── scheduler.service.js  # Cron-based activity scheduler
│   ├── helpers/               # Utility functions
│   ├── middleware/            # Express middleware
│   └── views/                 # EJS templates
├── prisma/
│   └── schema.prisma          # Database schema
├── public/                    # Static assets
├── package.json              # Dependencies and metadata
├── package-lock.json         # Locked dependency versions
├── README.md                 # This file
├── Mission3.ipynb            # AI Media Factory Jupyter Notebook
├── wahh.js                   # Additional script
├── .gitignore                # Git ignore rules
└── .env                      # Environment configuration (not in repo)
```

---

## 🧠 Credentials Required

To run this project, you'll need credentials for:

1. **Google OAuth Credentials**
   - Client ID
   - Client Secret
   - Redirect URI

2. **Google Service Account**
   - JSON key file (for Calendar & Gmail automation)
   - Refresh Token

3. **Twitter/X App Credentials**
   - API Key
   - API Secret
   - Access Token
   - Refresh Token

4. **GROQ API Key**
   - For GPT-OSS-120B model access

5. **Gmail App Password**
   - For SMTP-based email automation

6. **Database Access**
   - PostgreSQL connection string with credentials

---

## 📔 Mission 3: AI Media Factory

The repository includes **Mission3.ipynb**, a comprehensive Jupyter Notebook demonstrating an AI-powered content generation and automation pipeline:

### Workflow:
1. **Trend Discovery** — Fetches trending topics from ReddAPI/Reddit
2. **AI Script Generation** — Uses GROQ API to create captions and creative scripts
3. **Image Generation** — Pollinations AI for AI-generated images
4. **Video Generation** — Replicate API for AI video with fallback to local MP4 creation
5. **Content Hosting** — File.io/GoFile.io for media upload and CDN
6. **Circlo Integration** — Automated posting to Circlo platform

### Key Capabilities:
- ✨ Automated trending topic discovery and analysis
- 🧠 Creative AI-generated captions and scripts (60-second content)
- 🎨 Dynamic image generation from natural language prompts
- 🎬 Local MP4 video creation with PIL image overlays and text
- 🕐 Periodic or manual content posting modes
- 🔄 Intelligent fallback mechanisms for API failures

### Libraries Used:
- **MoviePy** — Video generation and editing
- **PIL/Pillow** — Image manipulation and text rendering
- **Replicate SDK** — AI video model access
- **Requests** — HTTP requests and API communication

---

## 🎯 Use Cases

1. **Marketing Automation** — Automated social media posting and email campaigns
2. **Calendar Assistant** — Intelligent calendar event management and reminders
3. **Content Creation** — AI-powered content generation and multi-platform publishing
4. **Task Automation** — Natural language-driven automation workflows
5. **Bot Development** — Twitter/X bot for engagement, outreach, and monitoring

---

## 🔐 Security Considerations

⚠️ **Critical Security Notes:**

- ✅ Never expose credentials publicly in code
- ✅ All sensitive data must be stored in `.env` file (excluded from git)
- ✅ Service account keys should be encrypted and stored securely
- ✅ API tokens require secure vault management
- ✅ Database credentials use environment variables only
- ✅ Implement rate limiting for API endpoints
- ✅ Use HTTPS in production
- ✅ Validate and sanitize all user inputs

---

## 📊 Repository Information

| Metric | Value |
|--------|-------|
| **Repository Size** | 52 KB |
| **Forks** | 0 |
| **Stars** | 0 |
| **Watchers** | 0 |
| **Open Issues** | 0 |
| **Type** | Public Fork |
| **Parent Repo** | [taufikkurniawan060305/smartaihackathonlocalgpt](https://github.com/taufikkurniawan060305/smartaihackathonlocalgpt) |
| **License** | Private - Internal Project |

---

## 🚀 Key Features at a Glance

| Feature | Service | Status |
|---------|---------|--------|
| Calendar Management | Google Calendar API | ✅ Integrated |
| Email Automation | Gmail + Nodemailer | ✅ Integrated |
| Social Media Bot | Twitter API v2 | ✅ Integrated |
| AI Responses | GROQ (GPT-OSS-120B) | ✅ Integrated |
| Task Scheduling | Node Cron | ✅ Integrated |
| Content Generation | Multiple AI APIs | ✅ Notebook Demo |
| Video Generation | Replicate + Local | ✅ Notebook Demo |
| Database ORM | Prisma + PostgreSQL | ✅ Configured |

---

## 📝 Notes

- **Project Type:** Hackathon submission for AI Creation Hackathon 2025
- **Development Status:** Active development
- **Repository Source:** Forked from original Smart AI Hackathon project
- **Contribution Level:** Full admin permissions on this fork
- **Access Level:** Private internal project (code available publicly)

---

## 📚 Documentation Links

- [GitHub Repository](https://github.com/farrelta/smartaihackathonlocalgpt)
- [Notion Page Summary](https://github.com/farrelta/smartaihackathonlocalgpt) ← Comprehensive overview
- [Express.js Documentation](https://expressjs.com/)
- [Prisma Documentation](https://www.prisma.io/docs/)
- [GROQ API Docs](https://console.groq.com/docs/speech-text)
- [Google APIs Documentation](https://developers.google.com/apis-explorer)
- [Twitter API v2 Documentation](https://developer.twitter.com/en/docs/twitter-api)

---

## 📧 Support & Contact

For issues, questions, or contributions related to this project, please refer to the main repository or contact the project maintainers.

---

**Last Updated:** November 21, 2025  
**Repository:** https://github.com/farrelta/smartaihackathonlocalgpt
