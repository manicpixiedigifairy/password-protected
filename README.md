# Password Protected

Hosted case study page for the Password Protected spec concept (Victoria's Secret Fashion Show 2026). This repo holds only this page, kept apart from the other portfolio repos.

## Where it lives

| What | Where |
| --- | --- |
| The page | `password-protected/index.html`, with its images in `password-protected/assets/` |
| Netlify site | https://victoriassecretjournal.netlify.app |
| Loader block | `loader/password-protected.html` |

## How it works

1. `password-protected/index.html` is the full page. The locked and open journal frames, feather wings and lipstick kiss live in `password-protected/assets/`. Everything else is drawn in the page itself.
2. Netlify publishes the `password-protected` folder (see `netlify.toml`), so the Netlify URL opens straight on the page.
3. The loader block goes in a Readymag Code widget or a Squarespace Code block. On each visit it asks GitHub for the newest commit on `main`, then loads that exact version of the page through jsDelivr (a free CDN that serves public GitHub repos), so a push shows up on the next visit. If that fails it tries the `main` branch on jsDelivr, then the Netlify site.

## Set up the loader (one time)

1. Open the page in the site builder and add a **Code** widget (Readymag) or **Code** block (Squarespace).
2. Paste the contents of `loader/password-protected.html`. In Readymag, leave **Use iFrame** off.
3. Check it in **Preview**, since editors may not run custom code.
4. Publish.

## Update the page

Edit the files in `password-protected/`, commit and push to `main`. The loader picks it up on the next visit, and Netlify redeploys once the repo is linked to the Netlify site.
