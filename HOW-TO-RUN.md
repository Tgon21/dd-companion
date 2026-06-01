# How to Run the App (Windows)

Card Query lets you see your duplicate cards and what they'd sell for,
browse the full card database, and build lineups. **Everything runs on your own PC** — and
no account/login is required just to browse.

## Run it
1. Double-click **`MLB Companion.exe`** (or run the installer **`MLB Companion Setup.exe`** for a standalone app window).
2. A small console window opens — **leave it open**, that's the app running.
3. Your browser opens automatically to **http://localhost:4000**. If it doesn't, type that address in your browser.
4. The **first launch takes ~1 minute** to download current card prices. After that it's instant; prices auto-refresh every ~20 minutes.

## Close it
Close the browser tab, then close the console window (or press **Ctrl+C** in it). That fully stops the app.

## Windows SmartScreen
The app isn't code-signed, so Windows may show **"Windows protected your PC."**
Click **More info → Run anyway**. That just means there's no paid signing certificate on the file.

## Pulling in your own cards (optional)
In the app's **Import** tab there are two ways to load your collection:
- **Beginner:** a bookmarklet you click while logged in at mlb26.theshow.com.
- **Advanced:** paste your session cookie / a cURL command.

Your login/session **never leaves your computer** — it's used only to talk to theshow.com and is never saved to disk. See **[SAFETY.md](SAFETY.md)** and **[verify the scripts](import-scripts/VERIFY.md)**.

## Where your data lives
- **Card-price cache:** `%LOCALAPPDATA%\MLBCompanion\cache.json`
- **Your collection / saved lineups:** stored in your browser (localStorage)
- Delete the cache folder anytime to reset prices.

## Port already in use?
If something else is using port 4000, open a Command Prompt in the app's folder and run:
```
set PORT=4500
"MLB Companion.exe"
```
then use **http://localhost:4500** instead.
