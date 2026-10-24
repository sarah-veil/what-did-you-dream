# 你梦见什么？ · What Did You Dream?

一个单页、离线可用的中英双语梦境象征词典。

线上地址：[dream.dqquan.com](https://dream.dqquan.com/)

写下梦境。页面会在文字中查找 **象征词**，与 84 条传统梦境象征对照，并显示每种象征通常被怎样理解。页面也会列出命中的词语，方便你自行判断解释是否贴近。

## What this is — and is not

- **Not an AI.** Nothing is generated, guessed, or sent anywhere. No server, no account, no cookies, no tracking. As shipped it makes **no network requests at all**; there is one optional anonymous page counter that stays switched off until a token is configured.
- **Not a prediction.** It does not tell you what will happen. It is a dictionary, plus a few questions worth sitting with.
- **Honest about its limits.** Most entries are written at the level of a tradition ("a common reading", "in Jungian terms"), not as citations to a specific book or page.
- `供自省，不作诊断。`

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

- Verified zero runtime requests: no `fetch`, no `XMLHttpRequest`, no external `<script src>` or stylesheet links (the only `<link>` is an inline `data:` favicon).
- Works at 375px wide and at desktop widths.
- Chinese matching is literal phrase matching and runs entirely in the browser.
