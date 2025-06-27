# youtubeautomation-n8n

# 🎬 YouTube Shorts Automation with n8n

This repository contains a fully automated n8n workflow to upload short-form videos (reels) to YouTube Shorts. It uses Google Drive for video storage, OpenRouter for AI metadata generation, and Google Sheets to track uploads — all with zero cost services.

---

## 🚀 Features

- 🎥 Automatically picks a **random unused `.mp4`** video from Google Drive
- 🧠 Generates **YouTube title, description, and tags** using OpenRouter AI
- 📤 Uploads the video to **YouTube Shorts**
- 📊 Logs the upload to **Google Sheets**
- 🗑️ Deletes the video from Drive after upload
- 🔁 Repeats 3 times a day using a scheduled trigger
- ✅ Skips previously uploaded videos using deduplication logic

---

## 🔧 Requirements

- [n8n](https://n8n.io/) (self-hosted or cloud)
- Google account with:
  - ✅ Google Drive folder with `.mp4` files
  - ✅ Google Sheet for logging (columns: `File Name`, `YouTube Link`, `Status`)
- YouTube account + OAuth setup
- OpenRouter API key (free) → https://openrouter.ai

---

## 🔐 Environment Variables

```env
GOOGLE_SHEET_ID=your_google_sheet_id
GOOGLE_DRIVE_FOLDER_ID=1ad_-H9yzjgbVL1PrLOKaKqvYNqgNMGFx
OPENROUTER_API_KEY=your_openrouter_api_key
