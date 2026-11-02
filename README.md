# Logo Directory

A one-page, searchable list of organisations (radiology and medical bodies, journals, AI and tech, finance, social networks and publishing tools), each with a logo or initials badge, a one-line description and a link to its official website.

**What's in this folder**

| File | What it is |
|---|---|
| `index.html` | The web page itself. You don't need to edit it. |
| `organisations.json` | The list of organisations. This is the only file that changes when you add one. |
| `README.md` | These instructions. |

**About the logos:** no logo images are stored here. Logos are shown live from the free, open-source [Simple Icons](https://simpleicons.org) library. If an organisation isn't in that library (most medical bodies and journals aren't), the page shows a coloured badge with its initials instead.

**About the yellow "verify" tag:** these links were written from knowledge of the official sites but have not yet been clicked through and checked. Click each one; if it opens the right site, ask Claude to change its status to `ok`.

---

## Part 1 — Put the site online with GitHub Pages (one-off, about 5 minutes)

1. Go to **github.com** and sign in.
2. Open this repository: **drljchacko-hub/logo-directory**.
3. Make sure the files are on the main branch:
   - If you see a yellow banner saying a branch "had recent pushes", click **Compare & pull request**, then **Create pull request**, then **Merge pull request**, then **Confirm merge**.
4. Click **Settings** (the gear-icon tab near the top of the repository page).
5. In the left-hand menu, click **Pages**.
6. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
7. Under **Branch**, choose **main**, leave the folder as **/ (root)**, and click **Save**.
8. Wait 1–2 minutes, then refresh the page. A box appears at the top saying **"Your site is live at …"**.
9. Your web address will be:
   **https://drljchacko-hub.github.io/logo-directory/**
   Click **Visit site** to open it. Bookmark it.

> **Note:** double-clicking `index.html` on your own computer will show a message saying the list couldn't load. That is normal — browsers block it for security. Always use the web address above.

**Note on privacy:** GitHub Pages sites are public. This directory contains no personal or patient information, so that is fine.

---

## Part 2 — Add a new organisation

### Easiest way: ask Claude

Open a Claude Code session on this repository and type something like:

> Add the **Society for Pediatric Radiology** to my logo directory under "International Radiology Societies & Congresses", website **https://www.pedrad.org**. Commit and push it.

Claude will add it to `organisations.json`. GitHub Pages updates the live site within about 2 minutes.

### Do it yourself on the GitHub website

1. On the repository page, click **organisations.json**.
2. Click the **pencil icon** (✏️ "Edit this file") at the top right of the file.
3. Find any existing entry, for example:

   ```json
       {
         "name": "Radiopaedia",
         "category": "Clinical & Research Tools",
         "description": "Open-edit radiology reference articles and cases.",
         "url": "https://radiopaedia.org",
         "icon": "",
         "initials": "Rp",
         "status": "ok"
       },
   ```

4. Click just after the `},` line at the end of that entry, press **Enter**, and paste a copy of the block above.
5. Change the text inside the quote marks:
   - **name** — the organisation's full name.
   - **category** — copy an existing category name *exactly* (same spelling and capitals), or type a new one to create a new section.
   - **description** — one short line.
   - **url** — the official website, starting with `https://`.
   - **icon** — leave as `""` unless you know its [Simple Icons](https://simpleicons.org) name (search that site; the name is the lower-case word in the icon's web address, e.g. `pubmed`).
   - **initials** — the short text for the badge (e.g. `"SPR"`). Keep it to 2–6 characters.
   - **status** — `"ok"` if you've checked the link, or `"verify"` if not.
6. **Check the punctuation** — this is the only fiddly part:
   - Every entry is wrapped in `{ }` and followed by a comma `,` — **except the very last entry in the list**, which has no comma.
   - Every line inside an entry ends with a comma, except the last line (`"status": …`).
   - Use straight double quotes `"`, not curly quotes.
7. Scroll down, click **Commit changes…**, then **Commit changes** again.
8. Wait about 2 minutes and refresh your site.

**If the page says "The list could not be loaded" after an edit**, a comma or quote mark is usually missing. Either undo the change (repository → **Commits** → click the latest → **⋯** → revert), or ask Claude: *"Fix the JSON in organisations.json."*

### To remove or change an organisation

Same steps: edit `organisations.json`, change or delete the whole `{ … },` block, and commit. (Or simply ask Claude.)
