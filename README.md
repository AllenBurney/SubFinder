# 🎬 SubFinder

A lightweight, single-file web app to search and download movie subtitles — no server, no dependencies, no build step. Just open the HTML file in a browser.

Powered by the [OpenSubtitles REST API](https://opensubtitles.stoplight.io/).

---

## Features

- Search subtitles by movie name
- Filter by language (English, Hindi, Spanish, French, and more)
- View subtitle metadata — language, format, uploader, download count
- One-click `.srt` download
- Handles rate limits, quota errors, and network failures gracefully
- Works entirely in the browser — no backend required

---

## Getting Started

### 1. Get a free API key

Sign up at [opensubtitles.com/en/consumers](https://www.opensubtitles.com/en/consumers) and create an API key. The free tier allows **20 subtitle downloads per day**.

### 2. Add your API key

Open `subfinder.html` in any text editor and find this line near the top of the `<script>` block:

```js
const API_KEY = "YOUR_KEY_HERE";
```

Replace `YOUR_KEY_HERE` with your actual API key.

### 3. Open in browser

Just double-click `subfinder.html` — no server, no install, no setup needed.

---

## Usage

1. Type a movie name in the search bar
2. Select your preferred subtitle language from the dropdown
3. Click **Search**
4. Browse the results and click **⬇ Download .srt** on the subtitle you want
5. The `.srt` file will download to your device

---

## API Limits (Free Tier)

| Limit | Value |
|---|---|
| Subtitle downloads per day | 20 |
| Search requests | Generous, but rate-limited |
| API key required | Yes (free) |

If you hit the daily download limit, the app will show a clear message. Limits reset every 24 hours.

---

## Publishing / Sharing

> ⚠️ **Do not share the HTML file publicly with your API key hardcoded in it.** Anyone who views the source can steal your key and exhaust your daily quota.

**Safe options:**

- Share it privately (e.g. send the file directly to someone you trust)
- Add a UI input so each user enters their own API key (recommended for public hosting)
- Move the API key to a backend proxy before deploying publicly

**Free hosting options** (once the API key issue is handled):

- [GitHub Pages](https://pages.github.com) — push to a repo and enable Pages
- [Netlify](https://netlify.com) — drag and drop the file
- [Vercel](https://vercel.com) — similar to Netlify

---

## File Structure

```
subfinder.html    ← entire app (HTML + CSS + JS in one file)
README.md         ← this file
```

---

## Tech Stack

- Pure HTML, CSS, and JavaScript — no frameworks, no dependencies
- [OpenSubtitles REST API v1](https://opensubtitles.stoplight.io/)

---

## Troubleshooting

**"Invalid or missing API key"**
→ Make sure you replaced `YOUR_KEY_HERE` with a real key from opensubtitles.com.

**"Rate limit reached"**
→ Wait a minute and try your search again.

**"Daily download quota exceeded"**
→ You've used all 20 free downloads for today. Resets in 24 hours.

**Download opens in a new tab instead of saving**
→ This is a browser behaviour on some systems. Right-click the tab and choose "Save As" to save the `.srt` file.

**No results found**
→ Try a shorter or simpler movie title, or switch to a different language.

---

## License

MIT — free to use, modify, and distribute.
