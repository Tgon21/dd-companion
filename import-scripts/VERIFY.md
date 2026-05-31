# Verify the import scripts before you paste anything

You should never paste a script you can't check. Both import scripts are published here
**byte-for-byte identical** to what the app shows you, so you can confirm nothing was changed
or added.

There are two scripts:
- [`bookmarklet.txt`](bookmarklet.txt) — the beginner-friendly bookmarklet (a `javascript:` link you click).
- [`console-snippet.txt`](console-snippet.txt) — the same logic for pasting into your browser's developer console.

## How to diff-check (easiest: an online diff tool)
1. Open the script file here on GitHub and click **Raw**, then select-all and copy.
2. In the app, copy the matching script from the **Import** tab.
3. Paste both into a free diff tool such as **diffchecker.com** (left = app, right = this repo).
4. Confirm the result says **"The two files are identical."** If there's *any* difference, don't run it.

## What you're checking for
Read the script (it's short). It should only ever:
- fetch `https://mlb26.theshow.com/apis/inventory.json` (paged),
- keep each card's `uuid`, `name`, and `quantity`,
- save the result to a local `mlb-inventory.json` file.

It should **not** contain any other URL, any reference to a different server, or anything
about passwords/account details. There is no other domain in these scripts — only
`theshow.com`. See [SAFETY.md](../SAFETY.md) for the plain-English explanation.

> Tip: the only web address that should appear in either script is `mlb26.theshow.com`.
> If you ever see a different domain, the script has been tampered with — do not run it.
