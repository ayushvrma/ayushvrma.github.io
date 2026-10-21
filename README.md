# Portfolio

Static site (no build step). Deploy with GitHub Pages.

## Deploy
1. Create a repo (name it `<username>.github.io` for a root URL, or any name for `<username>.github.io/<name>`).
2. Push these files to `main`.
3. Settings → Pages → Source: **Deploy from a branch** → `main` / `(root)`.

## Preview locally
`python3 -m http.server` then open http://localhost:8000 (needed so `fetch` works).

## Add a photo
Drop the file in `images/gallery/` and add an entry to `gallery/gallery.json`:
`{"src": "images/gallery/name.jpg", "caption": "Shown on hover", "note": "A few personal words shown under the photo when opened."}`
Clicking a photo opens it full width inside the page with the caption and note below.

## Add logos
Save logos as PNGs in `images/logos/` named `spyne.png`, `irame.png`, `diool.png`, `cmu.png`, `usc.png`, `thapar.png`. Until a file exists, an initials tile shows instead.

## Add a blog post
1. Write `posts/my-post.md` (plain Markdown).
2. Add to `posts/posts.json`:
   `{"slug": "my-post", "title": "My post", "date": "2026-10-21", "summary": "One line."}`
3. Push. It appears at `blog.html?p=my-post`. While `posts.json` is `[]`, the blog shows "Coming soon."

## Edit links
Replace `YOUR-LINKEDIN` and `YOUR-GITHUB` in `index.html`.
