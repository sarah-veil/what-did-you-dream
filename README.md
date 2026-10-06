# What Did You Dream?

A single-page, offline dream-symbol dictionary for the English-speaking web.

Type a dream. The page looks for **symbol words** in what you wrote, matches them against 84 traditional dream symbols, and shows you what each one has usually been taken to mean. It also shows you **which words it matched**, so you can judge for yourself whether the reading fits.

## What this is — and is not

- **Not an AI.** Nothing is generated, guessed, or sent anywhere. No server, no account, no tracking, no analytics, no network requests at all.
- **Not a prediction.** It does not tell you what will happen. It is a dictionary, plus a few questions worth sitting with.
- **Honest about its limits.** Most entries are written at the level of a tradition ("a common reading", "in Jungian terms"), not as citations to a specific book or page.
- `For reflection, not diagnosis.`

## How it works

Everything lives in one file: `index.html`. The symbol list is a plain JavaScript array (`DICT`) near the top of the script; the matching and rendering code follows it.

- Open `index.html` in any browser. That's the whole app — it works offline, including from `file://`.
- To add or edit a symbol, edit the `DICT` array. **Keyword matching is literal**, so adding a word to a symbol's keyword list is what makes it fire.
- To rename the site, change one line: `var SITE_NAME`.

## Files

| File | What it is |
|---|---|
| `index.html` | The entire site (styles, script, and data are inline) |
| `README.md` | This file |

## Notes

- Verified zero external requests: no `fetch`, no `XMLHttpRequest`, no external `<script src>` or stylesheet links (the only `<link>` is an inline `data:` favicon).
- Works at 375px wide and at desktop widths.
