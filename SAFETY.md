# Is This Safe? — What Importing Your Collection Actually Does

Short version: the import **only reads which cards you own** (uuid, name, quantity) from
theshow.com's own inventory endpoint, the same one the website uses. It runs **in your own
browser / on your own machine**, and it **never sends anything to the developer or any third
party**. You can read every line of the scripts yourself — see
**[Verify the import scripts](import-scripts/VERIFY.md)**.

## What it does
- Calls `https://mlb26.theshow.com/apis/inventory.json` (paged) while **you** are logged in.
- Collects, for each card: its **uuid, name, and quantity owned**.
- Saves that list to a file (`mlb-inventory.json`) that you then load into the app.

## What it does NOT do
- ❌ It does **not** read your password, email, payment info, or any account details.
- ❌ It does **not** send your data to the developer, a website, or anyone else — it can't; there's no server involved beyond theshow.com itself.
- ❌ It does **not** buy, sell, list, or change anything in your account. It only **reads**.
- ❌ It does **not** automate gameplay or the marketplace (doing so would violate The Show's Terms — this tool won't).

## About the "Advanced" cookie option
If you use the Advanced import (pasting a session cookie or cURL command):
- The cookie is used **for a single request** to ask theshow.com for your inventory, then **discarded**.
- It is **never written to disk, never logged, and never transmitted anywhere except theshow.com**.
- Treat your session cookie like a password — only paste it into software you trust, and only on your own machine.

## Why you can trust it
- The app runs **locally**; there is no developer-operated server in the loop. See the [Privacy Policy](PRIVACY.md).
- The import scripts are short and published here unchanged so you can **diff-check** them before pasting anything. See [VERIFY.md](import-scripts/VERIFY.md).

Still unsure? Don't paste anything you haven't verified, and stick to the read-only beginner bookmarklet.
