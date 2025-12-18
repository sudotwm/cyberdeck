# Magnus Cyberdeck - Setup Guide

Welcome to Magnus Cyberdeck! This guide will help you get started in just a few minutes.

---

## 📦 What You Need

- **Windows 10 or 11** (64-bit)
- **An AI API key** (at least one - see options below)
- **5 minutes** of your time

**You do NOT need Node.js, Python, or any other software installed!**

---

## 🚀 Quick Start (2 Steps)

### Step 1: Extract the Files

1. Extract the `win-v.1.0-beta.zip` to any folder you like
   - Example: `C:\Magnus` or `D:\Apps\Magnus`
2. You should see a folder with `Magnus Cyberdeck.exe` inside

### Step 2: Configure Your API Key

1. Open the extracted folder
2. Find the file called `.env`
3. **Right-click** `.env` → **Open with** → **Notepad**
4. Find the AI backend you want to use (see options below)
5. **Remove the `#`** from your chosen API key line
6. **Replace the placeholder** with your actual API key
7. **Save** the file (Ctrl+S)

### Step 3: Run Magnus!

1. Double-click `Magnus Cyberdeck.exe`
2. Wait a few seconds for the window to open
3. Start chatting! 🎉

---

## 🔑 Getting Your API Keys

You need **at least ONE** of these API keys. Choose the one that works best for you:

### Option 1: Google Gemini (Recommended - Free Tier Available)

**Best for:** Fast responses, free tier, easy setup

1. Go to: https://aistudio.google.com/apikey
2. Click **"Get API key"** or **"Create API key"**
3. Sign in with your Google account
4. Click **"Create API key in new project"**
5. Copy the key (starts with `AIza...`)
6. Open your `.env` file and find this line:
   ```
   # GEMINI_API_KEY=your-gemini-api-key-here
   ```
7. Remove the `#` and replace `your-gemini-api-key-here` with your actual key:
   ```
   GEMINI_API_KEY=AIzaSyC_your_actual_key_here
   GEMINI_MODEL=gemini-2.0-flash-exp
   ```
8. Save the file

**Free tier:** 15 requests per minute, 1500 requests per day

---

### Option 2: Groq (Fast & Free)

**Best for:** Super fast responses, generous free tier

1. Go to: https://console.groq.com/
2. Sign up for a free account
3. Go to **API Keys** section
4. Click **"Create API Key"**
5. Copy the key (starts with `gsk_...`)
6. Open your `.env` file and find this line:
   ```
   # GROQ_API_KEY=your-groq-api-key-here
   ```
7. Remove the `#` and replace with your key:
   ```
   GROQ_API_KEY=gsk_your_actual_key_here
   GROQ_MODEL=llama-3.3-70b-versatile
   ```
8. Save the file

**Free tier:** 30 requests per minute, very generous limits

---

### Option 3: Mistral AI

**Best for:** European users, privacy-focused

1. Go to: https://console.mistral.ai/
2. Sign up for an account
3. Go to **API Keys** section
4. Click **"Create new key"**
5. Copy the key
6. Open your `.env` file and find this line:
   ```
   # MISTRAL_API_KEY=your-mistral-api-key-here
   ```
7. Remove the `#` and replace with your key:
   ```
   MISTRAL_API_KEY=your_actual_key_here
   MISTRAL_MODEL=mistral-large-latest
   ```
8. Save the file

---

### Option 4: Ollama (100% Local & Free)

**Best for:** Complete privacy, no internet required, unlimited usage

1. Download Ollama from: https://ollama.com/download
2. Install Ollama on your computer
3. Open **Command Prompt** or **PowerShell**
4. Run this command to download a model:
   ```bash
   ollama pull llama3.2
   ```
5. Wait for the download to complete (might take a few minutes)
6. Open your `.env` file and find these lines:
   ```
   # OLLAMA_URL=http://localhost:11434
   # MODEL=your-ollama-model-name
   ```
7. Remove the `#` and set your model:
   ```
   OLLAMA_URL=http://localhost:11434
   MODEL=llama3.2
   ```
8. Save the file
9. Make sure Ollama is running in the background (it auto-starts after installation)

**Pros:** Free, private, unlimited
**Cons:** Requires download, uses your GPU/CPU

---

## 🎯 Example `.env` File

Here's what your `.env` file should look like after setup (using Gemini as an example):

```env
# AI Backend - Gemini (Google AI)
GEMINI_API_KEY=AIzaSyC_your_actual_key_here
GEMINI_MODEL=gemini-2.0-flash-exp

# Other backends (commented out)
# MISTRAL_API_KEY=your-mistral-api-key-here
# MISTRAL_MODEL=mistral-large-latest

# GROQ_API_KEY=your-groq-api-key-here
# GROQ_MODEL=llama-3.3-70b-versatile

# OLLAMA_URL=http://localhost:11434
# MODEL=llama3.2

# Web Search (Optional)
# BRAVE_API_KEY=your-brave-api-key-here

# Memory Configuration
MAX_HISTORY=15
CONTEXT_TURNS=7
CONTEXT_WINDOW=32768
```

**Important:** Only ONE AI backend needs to be uncommented (without `#`). Magnus will use the first one it finds.

---

## 🔧 Troubleshooting

### "The app won't start"

- Make sure you edited the `.env` file and added your API key
- Check that you removed the `#` from your API key line
- Verify you saved the `.env` file after editing
- Try running as Administrator (right-click → Run as administrator)

### "Windows SmartScreen blocked this app"

- Click **"More info"**
- Click **"Run anyway"**
- This is normal for unsigned apps

### "No response from AI"

- Check your internet connection (except for Ollama)
- Verify your API key is correct
- Make sure you have free tier quota remaining

### "Database errors"

- The `database` folder will be created automatically on first run
- If you see errors, try deleting the `database` folder and restart

---

## 🎨 Features

- **Multi-backend AI support** (Gemini, Groq, Mistral, Ollama)
- **Code editor** with syntax highlighting
- **File management** - Open folders and edit files
- **Browser automation** - Automate web tasks
- **Document generation** - F.R.I.E.N.D. system
- **Context management** - Smart memory system
- **Web search integration** - Search the web from chat
- **Workspace persistence** - Auto-save your work

---

## 📝 Tips

1. **First time?** Try asking: "Hey Magnus, what can you do?"
2. **Open a folder** to start coding - File → Open Folder
3. **Right-click files** in the file tree for quick actions
4. **Use the chat** for coding help, debugging, or general questions
5. **Check the context panel** to see what Magnus knows about

---

## 🆘 Need Help?

- Check the main README.md for detailed documentation

---

## 🎉 You're All Set!

Magnus is ready to help you code, automate, and create. Have fun! 🚀

---

**Version:** 1.0.0-beta
**Created by:** heavylildude (Chris)
**License:** ISC
