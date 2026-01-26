# Blog

A dead simple, SEO-friendly, AI-friendly HTML blog.
No frameworks, no build steps, no config files.
Just semantic HTML that works everywhere, forever.

This is not a template.
It’s a **design stance**.

## Design Philosophy

Modern web tooling is optimized for teams, products, and scale.
This blog is optimized for **thinking, writing, and longevity**.

Blog is built around a few deliberate constraints:

### 1. Files over systems

Everything is a file.
No databases, no CMS, no hidden state.

Your blog is just:

* HTML documents
* A stylesheet
* (Optionally) an RSS feed

If you can use a text editor, you can own your content.

### 2. Zero configuration is a feature

There is no config file.
This README *is* the config.

No generators, no pipelines, no dependency trees.
You don’t “set up” this blog — you just start writing.

### 3. Semantic HTML is the platform

The browser is the runtime.
HTML is the API.

We use:

* `<article>`, `<header>`, `<time>`
* Proper `<meta>` tags
* Real links, real pages

Because that’s what search engines, screen readers, and LLMs actually understand.

### 4. AI-native, not AI-bloated

The structure is intentionally:

* Flat
* Predictable
* Convention-based

So humans and machines can both:

* Generate new posts
* Modify existing ones
* Parse the entire site without context

No abstractions to reverse-engineer.

### 5. Boring is a design goal

No JavaScript.
No hydration.
No build step.
No upgrade path.

This blog will work:

* In 2026
* In 2036
* On slow devices
* On broken networks
* On future crawlers

Boring scales in time.

---

## Author

**Youssef El Abbassi**
Software engineer interested in BCI.

---

## Structure

```
blog/
├── index.html          # Homepage with posts listing
├── style.css           # Single stylesheet for everything
├── feed.xml            # RSS feed (optional)
├── posts/              # All blog posts
│   └── YYYY-MM-DD-slug.html
└── assets/             # Images and files
    └── images/
```

This is the entire system.

If you understand this tree, you understand the whole blog.

---

## Conventions

### Post Filenames

Format: `YYYY-MM-DD-slug.html`
Example:

```
2026-01-26-building-tools-for-myself.html
```

The filename is:

* The ID
* The URL
* The database key

No indirection.

---

### Post Template

Every post is a standalone HTML document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Brief description for SEO (150-160 chars)">
    <title>Post Title — Blog</title>
    <link rel="stylesheet" href="../style.css">
    <link rel="canonical" href="https://elabbassi.com/posts/YYYY-MM-DD-slug.html">
</head>
<body>
    <header>
        <nav><a href="../index.html">← Back to blog</a></nav>
    </header>
    <main>
        <article>
            <header>
                <h1>Post Title</h1>
                <time datetime="YYYY-MM-DD">Month DD, YYYY</time>
            </header>
            <p>Content goes here...</p>
        </article>
    </main>
    <footer>
        <p><a href="mailto:youssef@elabbassi.com">youssef@elabbassi.com</a></p>
    </footer>
</body>
</html>
```

Each post:

* Is fully valid on its own
* Has a stable URL
* Can be shared, archived, or scraped independently

---

### Index Updates

When adding a new post, update `index.html`:

```html
<li>
    <time datetime="YYYY-MM-DD">YYYY-MM-DD</time>
    <a href="posts/YYYY-MM-DD-slug.html">Post Title</a>
</li>
```

Posts are listed newest first.

No pagination. No infinite scroll.
Just a chronological log of thought.

---

## AI Instructions

This blog is designed to be generated and maintained by humans *and* machines.

When generating content:

1. **New post** → Create file in `posts/` using naming convention
2. **Update index** → Add link to `index.html` (newest first)
3. **Images** → Place in `assets/images/`
4. **No JavaScript** unless absolutely necessary
5. **Voice** → Direct, technical, introspective. Not marketing.

The goal is **legibility**, not optimization.

---

## Deployment

Drop the folder on any static host:

* GitHub Pages
* Netlify
* Vercel
* A USB stick
* An S3 bucket
* A random server in 2042

No build step.
No runtime.
No vendor lock-in.

---

## What This Is Resisting

This project is quietly against:

* CMS abstractions
* Markdown pipelines
* Static site generators
* Framework churn
* Tooling for tooling’s sake

Not because they’re bad —
but because **writing does not need infrastructure**.

---

## License

MIT