# FAQ & Troubleshooting

Quick answers to the things people hit most often.

## "Windows protected your PC" when I open it
The app isn't code-signed (no paid certificate), so Windows shows a SmartScreen warning. Click
**More info → Run anyway**. It's the same app you can read the source of — see [Is this safe?](SAFETY.md).

## I opened it but nothing happens / no window
- **Browser version:** a small black console window opens (leave it open) and your browser should
  open to **http://localhost:4000**. If the browser didn't open, type that address in yourself.
- **First launch takes ~1 minute** while it downloads current card prices — give it a moment.
- **Windowed version:** if no window appears, make sure you ran the installer (`Card Query Setup.exe`) and launched it from the **Card Query** shortcut.

## It says the port is in use / localhost:4000 won't load
Something else is using port 4000. Open a Command Prompt in the app's folder and run:
```
set PORT=4500
"Card Query.exe"
```
then use **http://localhost:4500** instead.

## Importing my collection is taking forever
That's normal — it reads your inventory one page at a time and can take **15 seconds to ~3 minutes**
for a big collection. **Don't click the bookmark again while you wait** (that's what triggers the
"multiple files" popup).

## Chrome says "downloaded multiple files automatically"
Choose **"Continue allowing automatic downloads of multiple files"** → **Done**. If you blocked it
earlier: click the 🔒/⚙ icon left of the address bar → **Site settings** → set **Automatic downloads**
to **Allow**, then click the bookmark again.

## The prices look out of date
The market auto-refreshes about every **20 minutes**. To force it now, click **↻ Refresh prices** in
the header. Remember prices are live and can change between refreshes — verify in-game before selling.

## How do I update the app?
The app checks on launch and shows a **"🆕 new version available"** banner with a download link when
there's a newer build. Grab the new download and run it (re-run the installer for the Windowed
version, or replace `Card Query.exe` for the Browser version).

## Is my login / account safe?
Yes — the import only **reads** which cards you own, runs on **your** machine, and never sends
anything to the developer. Full explanation: [Is this safe?](SAFETY.md) · verify the scripts: [VERIFY](import-scripts/VERIFY.md).

## How do I reset everything?
- **Your collection:** click **🗑 Clear my collection** in the Import panel.
- **Cached prices:** delete the folder `%LOCALAPPDATA%\MLBCompanion`.
- **Everything else** (lineups, saved builds, settings) lives in your browser's storage for the app.

## Windowed vs Browser — which should I use?
Same app, two shells. **Windowed** (installer) runs in its own desktop window like a normal program.
**Browser** runs as a single `.exe` and opens in your web browser — nothing installed. Pick whichever
you prefer; you don't need both.

## Where is my data stored?
On your device only. Collection, lineups, saved builds and settings are in the app's local browser
storage; the price cache is at `%LOCALAPPDATA%\MLBCompanion\cache.json`. Nothing is sent anywhere
except theshow.com. See the [Privacy Policy](PRIVACY.md).
