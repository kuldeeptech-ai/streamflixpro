# Streamflix Vercel Proxy

A minimal Vercel project that rewrites `/embed/movie/:id` requests to the configured origin.

## Deploy without API tokens

1. Extract this ZIP.
2. Upload the files to a new GitHub repository (keep `vercel.json` and `index.html` at the repository root).
3. Sign in to Vercel using GitHub.
4. Choose **Add New → Project**, then import that repository.
5. Keep the default settings and click **Deploy**.
6. In Vercel, open **Settings → Domains** and confirm the assigned `*.vercel.app` domain.
7. Test: `https://YOUR-VERCEL-DOMAIN/embed/movie/579974`

## Important

- This rewrite is configured for `https://nxsha.space`. Use it only if you own or are authorized to proxy that origin.
- No Cloudflare API token or Vercel API token is needed for the manual GitHub import flow; you only sign in to the Vercel website.
- Vercel rewrites proxy the matching request, but they do not guarantee that domains inside returned HTML, redirects, JavaScript, or media playlists are hidden or rewritten.
- The origin must allow these requests and return compatible content. This project does not bypass access controls, DRM, or provider restrictions.
