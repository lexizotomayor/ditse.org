# ditse — notes from home and abroad

Essays on Philippine history and culture, with a dash of personal experience. By Alexie Zotomayor.
Built with Eleventy 3 (Nunjucks), hosted on Netlify, with Netlify Forms for Contact and Comments and Decap CMS at `/admin/`. Same build as House of Taga, rebranded.

## Run it

```bash
npm install
npm start          # dev server with live reload
npm run build      # production build into _site/
```

Node 20+ (`.nvmrc` pins 22).

## Put it on Netlify

1. Push this folder to a new GitHub repo (e.g. `lexizotomayor/ditse.org`).
2. Netlify → **Add new site → Import from Git** → pick the repo. Build command and publish folder come from `netlify.toml`.
3. **Domain management** → add `ditse.org`.
4. **Identity** → Enable, set Registration to **Invite only**. Under **Services → Git Gateway** → Enable.
5. **Identity → Invite users** → your email. Accept the invite, set a password, and you land in `/admin/`.
6. **Forms** → turn on email notifications for **contact** and **comments**.

## Writing (Decap CMS)

Edit at **https://ditse.org/admin/**. Every save commits to GitHub and Netlify rebuilds in a minute or two.
- **Stories:** title, date, category, lead photo, the story itself (paste it in one go; the + button adds photos, YouTube, pull quotes, editor's notes), optional short version, timeline, tags, and a draft switch.
- **Pages:** featured story, About, Privacy.

## Comments and feedback

Every story ends with a comment form. Submissions go to Netlify → Forms → **comments** with the story's slug. To publish one: open the story in the CMS → **Comments** → add name, comment and date → Publish. Comments appear newest first.

## Where things live

| Path | What |
|---|---|
| `src/_data/site.js` | Name, URL, email, copyright |
| `src/_data/periods.js` | The four categories |
| `src/_data/stories_raw/*.json` | One file per story (written by the CMS) |
| `src/admin/config.yml` | What the CMS can edit |
| `src/_includes/` | Layouts and partials |
| `src/assets/css/site.css` | Styles and colour tokens (paper #F2EEE6, navy #012169, red #C8102E) |

## To do

- Replace the placeholder story `why-ditse` and set the featured story under Pages.
- Confirm the email address in `site.js` (kumusta@ditse.org is a placeholder).
- Approve the About and Privacy drafts; add a portrait.
