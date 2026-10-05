# www_seera-networks_com

Source for the ISEKAI by Seera Networks website (English / 日本語).

With GitHub Pages turned on, it's served at **https://seera-networks.github.io/www_seera-networks_com/**. Whether it should also replace the current site at www.seera-networks.com hasn't been decided; see *Custom domain (optional)* below.

It's a static site with no build step:

- `index.html` holds every page (Home, Link, Camera, Compute, About, Team, Blog with all posts, Contact). Pages are sections switched by the script at the bottom; each one has its own address, such as `/#blog`, `/#link` or `/#post-9fb02b24fc07c4`.
- `assets/` holds the images used by the Compute page and the blog posts.
- `.nojekyll` turns off GitHub's Jekyll processing, which isn't needed.

## Preview locally

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy (one-time setup)

1. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
2. After a minute or two the site is live at https://seera-networks.github.io/www_seera-networks_com/. Every merge to `main` updates it.

## Custom domain (optional, not decided yet)

`www.seera-networks.com` currently serves a separate Carrd page through Cloudflare. To move the domain to this site instead:

1. Add a file named `CNAME` containing `www.seera-networks.com`, or set the custom domain in **Settings → Pages**.
2. In Cloudflare DNS, set `www` to a **CNAME** pointing at `seera-networks.github.io`. Keep the redirect from `seera-networks.com` to `www`.
3. Tick **Enforce HTTPS** in **Settings → Pages** once the domain check passes.

## Editing

Each piece of text appears twice, as `<span lang="en">…</span><span lang="ja">…</span>`; keep both languages in step when you change copy.
