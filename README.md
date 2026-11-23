# Starving Writer

My writing, poetry and updates. Built with [Zola](https://www.getzola.org/) and the
[Terminimal](https://github.com/pawroman/zola-theme-terminimal) theme.

## The easy way: the editor (Pages CMS)

1. Go to **https://app.pagescms.org** and sign in with GitHub.
2. Open **Starving-Writer**.
3. Click **Posts**, then **Add an entry**. Fill in the title, date and text, and click **Save**.

The editor saves your post into this repository for you. Everything below is for
writing posts by hand instead, which also works.

## Writing a new post by hand

1. Open the `content/posts` folder.
2. Create a new file ending in `.md`, e.g. `my-new-poem.md`.
   The file name becomes the web address: `.../posts/my-new-poem/`.
   Use lowercase letters and dashes, no spaces.
3. Start it like this:

   ```
   +++
   title = "My new poem"
   date = 2026-11-30
   +++

   Your writing goes here.
   ```

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

Wrap a poem in the poem tags. Line breaks and spaces are kept exactly as typed:

```
{% poem() %}
the cursor blinks,
  patient as a lighthouse,
waiting for the first word.
{% end %}
```

### Drafts

Add `draft = true` under the date to keep a post hidden until it's ready.

### Tags (optional)

Add these two lines at the END of the `+++` section (just before the closing `+++`):

```
[taxonomies]
tags = ["poetry", "update"]
```

### A poem box (optional)

Instead of the poem tags, a post can have one poem in a separate box, shown after the text.
Add this line just before `[taxonomies]` (or before the closing `+++`):

```
extra.poem = "first line\n  second line, indented\nthird line"
```

(`\n` means "new line". The editor above handles this for you.)

## Where things live

| What | Where |
|---|---|
| Posts | `content/posts/` |
| Home page welcome text | `content/_index.md` |
| About, Portfolio, Contact | `content/pages/` |
| Name, colours, menu | `config.toml` |
| Your style tweaks (e.g. the poem style) | `static/custom.css` |
| Home and Posts page layouts | `templates/` |
| The Terminimal theme (no need to edit) | `themes/terminimal/` |

## Credits

Terminimal theme by pawroman and panr, MIT License (`themes/terminimal/LICENSE.md`).
Hack font, MIT License (`themes/terminimal/LICENSE-Hack.md`).
