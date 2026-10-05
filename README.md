# www_seera-networks_com

Source for **www.seera-networks.com**: the ISEKAI by Seera Networks website (English / 日本語).

It's a static site with no build step:

- `index.html` holds every page (Home, Link, Camera, Compute, About, Team, Blog with all posts, Contact). Pages are sections switched by the script at the bottom; each one has its own address, such as `/#blog`, `/#link` or `/#post-9fb02b24fc07c4`.
- `assets/` holds the images used by the Compute page and the blog posts.
- `CNAME` tells GitHub Pages to serve the site at `www.seera-networks.com`.
- `.nojekyll` turns off GitHub's Jekyll processing, which isn't needed.

## Preview locally

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy (one-time setup)

1. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
2. DNS (Cloudflare): set `www` to a **CNAME** pointing at `seera-networks.github.io`. Keep the existing redirect from `seera-networks.com` to `www.seera-networks.com`.
3. Back in **Settings → Pages**, once the domain check passes, tick **Enforce HTTPS**.

After that, every merge to `main` updates the live site within a minute or two.

## Editing

Each piece of text appears twice, as `<span lang="en">…</span><span lang="ja">…</span>`; keep both languages in step when you change copy.
