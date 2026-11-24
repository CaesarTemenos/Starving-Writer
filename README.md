# Solemn Vespers

My writing, poetry and updates, at https://solemnvespers.com. Built with [Zola](https://www.getzola.org/) and the
[austere](https://github.com/tomwrw/austere-theme-zola) theme.

## The easy way: the editor (Pages CMS)

1. Go to **https://app.pagescms.org** and sign in with GitHub.
2. Open **Starving-Writer**.
3. Click **Posts**, then **Add an entry**. Fill in the title, date/time and text, and click **Save**.

The editor saves your post into this repository for you. Everything below is for
writing posts by hand instead, which also works.

### Adding to the portfolio

In the editor, click **Portfolio**, then **Add an entry**. Choose a **Type** (Poetry, Short Story,
etc.); it shows in the list as **POETRY — 24 Nov 2026 — Title**. The Portfolio page's intro
text is under **Portfolio intro**. (To change the list of types, edit the `values` line under
`category` in `.pages.yml`.)

## Writing a new post by hand

1. Open the `content/posts` folder.
2. Create a new file ending in `.md`, e.g. `my-new-poem.md`.
   The file name becomes the web address: `.../posts/my-new-poem/`.
   Use lowercase letters and dashes, no spaces.
3. Start it like this:

   ```
   +++
   title = "My new poem"
   date = 2026-11-30T14:30:00
   +++

   Your writing goes here.
   ```

   The date is year-month-day, then `T`, then the time (24-hour clock).
   Newer posts appear first.

4. Save (on GitHub: **Commit changes**). The post appears on the Home and Posts
   pages automatically, newest first.

### Formatting cheatsheet

| You type | You get |
|---|---|
| An empty line between paragraphs | A new paragraph |
| `*italics*` | *italics* |
| `**bold**` | **bold** |
| `## A heading` | A sub-heading |
| `[link text](https://example.com)` | A link |
| `> a quotation` | A quote block |

### Poems

**In the editor:** type the poem in the Text box. Press **Shift+Enter** for a new line
within a stanza, and **Enter** for a new stanza. (Indents at the start of a line are lost.)

**By hand, to keep indents too:** wrap the poem in the poem tags. Line breaks, blank
lines and spaces are kept exactly as typed:

```
{% <poem> %}
the cursor blinks,
  patient as a lighthouse,
waiting for the first word.
{% </poem> %}
```

### Avoid `{{` and `{%` in your writing

Zola reads those as instructions, so a post containing them won't build.
(If you ever need them, ask Claude.)

### Drafts

Add `draft = true` under the date to keep a post hidden until it's ready.

### Tags (optional)

Add these two lines at the END of the `+++` section (just before the closing `+++`):

```
[taxonomies]
tags = ["poetry", "update"]
```

## Where things live

| What | Where |
|---|---|
| Posts | `content/posts/` |
| Home page welcome text | `content/_index.md` |
| Portfolio pieces (and the intro, in `_index.md`) | `content/portfolio/` |
| About, Contact | `content/pages/` |
| Name, tagline, colours, menu, profile picture setting | `config.toml` |
| Profile picture file | `static/images/profile.png` |
| Your style tweaks (poem style, post previews) | `static/custom.css` |
| Home and Posts page layouts, post previews, poem tags | `templates/` |
| The austere theme (no need to edit) | `themes/austere/` |

## Credits

austere theme by tomwrw, MIT License (see `themes/austere/README.md`).
Source Serif 4 font, via Google Fonts.
