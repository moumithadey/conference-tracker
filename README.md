# Conference Tracker

A personal conference discovery and submission tracker, hosted on GitHub Pages.

## Features

- 🔍 AI-powered conference discovery (web search via Anthropic API)
- 📥 Inbox with new/interested/submitting/passed views
- ⚠️ Deadline alerts for upcoming conferences
- 🔁 Duplicate detection on import
- 📄 CSV export for spreadsheets
- 📅 ICS calendar export (deadlines → Google Cal / Outlook / Apple Calendar)
- 💾 All data saved locally in your browser (localStorage)
- 🌐 Works fully standalone with your own API key

---

## Setup: Hosting on GitHub Pages

### 1. Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **New repository** (the green button or + icon top right)
3. Name it something like `conference-tracker`
4. Set it to **Public** (required for free GitHub Pages)
5. Click **Create repository**

### 2. Upload the file

**Option A — via the GitHub website (easiest):**
1. On your new repository page, click **Add file → Upload files**
2. Drag and drop `index.html` into the upload area
3. Click **Commit changes**

**Option B — via Git (if you have it installed):**
```bash
git clone https://github.com/YOUR_USERNAME/conference-tracker.git
cd conference-tracker
cp /path/to/index.html .
git add index.html
git commit -m "Initial commit"
git push
```

### 3. Enable GitHub Pages

1. In your repository, go to **Settings** (top tab)
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Set branch to **main** (or master), folder to **/ (root)**
5. Click **Save**

After about 60 seconds, your app will be live at:
```
https://YOUR_USERNAME.github.io/conference-tracker/
```

Bookmark that URL — it's your permanent link.

### 4. Add your Anthropic API key

1. Open the app in your browser
2. Click **⚙ Settings / API key** in the sidebar
3. Paste your Anthropic API key (starts with `sk-ant-`)
4. Click **Save settings**

Your key is stored only in your browser's localStorage — it never leaves your device except when making API calls directly to Anthropic.

> **Get an API key:** Go to [console.anthropic.com](https://console.anthropic.com), sign up, and create an API key under **API Keys**.

---

## Updating the app

When a new version of `index.html` is available, just re-upload it to your repository via **Add file → Upload files** and choose to overwrite the existing file. Your localStorage data is separate from the file, so your conferences, notes, and settings are preserved.

---

## Data & Privacy

- All conference data, notes, and settings are stored in **your browser's localStorage only**
- No data is sent to any server except Anthropic's API (for discovery searches)
- Clearing your browser data will erase your conference list — use the CSV export to back it up

---

## Exporting your data

Use **⬇ Export** in the sidebar at any time to download:
- **CSV** — open in Excel or Google Sheets, or use as a backup
- **ICS** — import upcoming deadlines into Google Calendar, Outlook, or Apple Calendar
