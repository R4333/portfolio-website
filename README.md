# Muhammad Abdullah — Portfolio

A personal portfolio site with a markdown blog: static HTML, CSS, and a
little vanilla JS. No frameworks, no build step.

## Run it

Open `index.html` in a browser, or serve it locally:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

```
index.html          — single-page site (hero, work, experience, about, contact)
style.css           — design system (Fraunces + Inter, paper/ink/green palette)
main.js             — mobile nav toggle + subtle scroll reveals
blog/index.html     — blog listing
blog/post.html      — post viewer (renders markdown client-side)
posts/index.json    — the list of posts
posts/*.md          — posts, in plain markdown
img/me.jpg          — portrait photo
resume.pdf          — downloadable résumé
favicon.svg         — monogram favicon
```

## Writing a blog post

1. Create `posts/my-post-slug.md` and write it in markdown.
2. Add an entry to `posts/index.json` (newest is sorted automatically):

```json
{
  "slug": "my-post-slug",
  "title": "My post title",
  "date": "2026-08-20",
  "description": "One-line summary shown on the blog listing."
}
```

3. Redeploy. That's it.

The post page fetches the markdown and renders it in the browser with
marked + DOMPurify, so there is nothing to build. The `slug` must match the
filename (without `.md`).

Deployable as-is to GitHub Pages, Vercel, or Netlify.
