# GPS Route Logic — DriveLogicAI

> **📦 This repository has been consolidated.**  
> All development now happens in the canonical monorepo:
>
> **→ [GPS-Route-Logic/DriveLogicAI_chat_V2](https://github.com/GPS-Route-Logic/DriveLogicAI_chat_V2)**

---

## About DriveLogicAI

DriveLogicAI is an AI-powered vehicle diagnostics and trip-logging Progressive Web App + Android app.

**Features:**
- 🔌 Real-time OBD-II Bluetooth diagnostics
- 🗺️ GPS route tracking with Google Maps
- 🧠 Gemini AI diagnosis & voice assistant
- 🎙️ Live voice-activated AI Co-pilot
- 📊 Damage/g-force scoring
- 🔧 Maintenance scheduler
- ☁️ Google Drive cloud backup
- 💳 Subscription tiers (Standard / Pro / Elite)
- 📱 AdMob monetization
- 🌤️ Real-time weather overlay

**Package:** `com.DriveLogicAI_chat`  
**Platform:** Android (Capacitor 8) + Web (React 19 + Vite)  
**Backend:** Firebase Firestore + Google Auth  
**AI:** Google Gemini API (`@google/genai`)

## ⚙️ CI/CD

Automated builds and Play Store publishing are handled via GitHub Actions in the canonical repo:
- Push to `main` → builds signed AAB, auto-publishes to Play Store **Internal Track**
- Push tag `v*.*.*` → promotes to **Production Track**
- Pull Requests → TypeScript lint check

## Required GitHub Secrets (in canonical repo)

| Secret | Description |
|--------|-------------|
| `KEYSTORE_BASE64` | Base64-encoded `release-key.jks` |
| `KEY_STORE_PASSWORD` | Keystore password |
| `KEY_ALIAS` | Key alias (`drivelogicai_key`) |
| `KEY_PASSWORD` | Key password |
| `PLAY_SERVICE_ACCOUNT_JSON` | Google Play API service account JSON |
| `GEMINI_API_KEY` | Gemini API key |
| `GOOGLE_MAPS_API_KEY` | Google Maps Platform key |
