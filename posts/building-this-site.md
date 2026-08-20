The previous version of this site was a Bootstrap template from a course
assignment. It had an "enrollment" modal, a fake team section, and a blog
theme demo that shipped with somebody else's vacation photos in it. It was
fine for a grade. It was not fine for a portfolio.

So this is a rebuild. The whole thing is a single HTML page, one stylesheet,
and about forty lines of JavaScript. No framework, no build step, nothing to
install. You can read the entire codebase in one sitting, which I think is a
feature.

## The design

I wanted it to feel like a nicely set document rather than a web app: warm
paper background, ink text, one shade of green, Fraunces for headlines and
Inter for everything else. Hairline rules instead of cards and shadows. The
most radical thing on the page is a numbered section every now and then.

The portrait in the hero is in full color because I like the warm lights in
the background. For a while it was warm monochrome with a hover-to-color
effect, which looked classy, but simpler won.

## How this blog works

Posts are plain markdown files in a `posts/` folder:

```text
posts/
  index.json             # the list of posts
  building-this-site.md  # this post
```

There is no database and no CMS. The listing page reads `index.json`, the
post page fetches the markdown file and renders it in your browser with
marked and DOMPurify. Writing a post means dropping a file in the folder,
adding one line to the JSON, and redeploying. That is the whole workflow,
and it will stay that way until it hurts.

> Simple things should stay simple until they have a reason not to.

## What I might write about next

Probably the AI-heavy work: what building retrieval pipelines taught me
about chunking, and what breaks first when a phone call is answered by an
LLM in production. Stay tuned.
