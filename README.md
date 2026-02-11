# Telegram Auto Chat with Gemini AI

A simple yet powerful **Telegram user script** (userbot) built with **Telethon** that automatically sends casual, natural-looking chat messages in a Telegram group. It uses **Google Gemini AI** (gemini-1.5-flash) to generate fresh Hindi-English mix messages, with fallback to a large list of predefined casual phrases if API fails.

**Note:** This is a **user account script** (not a bot), so it uses your real Telegram account. Use responsibly – excessive use can lead to **Telegram flood bans** or account restrictions. Designed for educational/testing purposes only.

## Features
- **AI-Powered Messages**: Gemini generates unique, casual messages every time (Hindi-English mix, emojis, daily topics like mood, weather, food, time pass).
- **Fallback List**: 200+ ready-made simple chatting messages (your provided list) if Gemini quota hits or error occurs.
- **Fast Sending**: Messages every 5-10 seconds (random delay) – **very aggressive**, flood wait handled automatically.
- **24/7 Ready**: Infinite loop – run on server/VPS/PythonAnywhere for continuous operation.
- **Flood Protection**: Catches Telegram's `FloodWaitError` and waits as instructed.
- **Simple Setup**: Only needs API ID/Hash, phone, and Gemini API key.

**Warning**: Telegram strictly detects automated activity on user accounts. Short intervals (5-10 sec) will trigger bans quickly. For long-term use, increase wait to 30-120 seconds.

## Requirements
- Python 3.8+
- Telethon library (`pip install telethon`)
- Google Generative AI (`pip install google-generativeai`)

## Setup Instructions

1. **Get Telegram API Credentials**
   - Go to https://my.telegram.org
   - Login with your phone number
   - Create new application → Get `api_id` and `api_hash`

2. **Get Google Gemini API Key**
   - Go to https://aistudio.google.com/app/apikey
   - Create new key → Copy it (starts with `AIzaSy...`)

3. **Clone / Create Repository**
   ```bash
   git clone https://github.com/yourusername/telegram-auto-chat-gemini.git
   cd telegram-auto-chat-gemini
