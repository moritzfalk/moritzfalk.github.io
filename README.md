# Moritz Falk — CV website

A static, responsive portfolio built from CV_English.pdf. The page uses plain HTML and inline CSS, system fonts, and native expandable project sections. No build step or external fonts are required. YouTube videos use linked preview images that open in a new tab. Each main project follows the same order: a short project description, an article or demo link, then technical bullet points. Employment roles and responsibilities are listed alongside each project. Content and navigation work without JavaScript; Cloudflare Web Analytics uses a small external script.

A compact header keeps the portrait, name, role, contact link, and language selector visible before the projects. The fuller introduction, company affiliation, programming and spoken languages, and contact/CV links follow the projects in the about and contact section. Project roles and technical descriptions remain explicit. Smaller projects show thumbnail previews even when their details are collapsed.

## Preview

Open `index.html` directly, or run `python3 -m http.server 8080` from this directory and visit `http://localhost:8080`.

## GitHub Pages

Live site: https://moritzfalk.com/

The custom domain is registered with Cloudflare. Keep the `CNAME` file containing `moritzfalk.com` on both branches. Cloudflare DNS points the apex to GitHub Pages using four A and four AAAA records, with `www` as a CNAME to `moritzfalk.github.io` (DNS only). Keep the `_github-pages-challenge-moritzfalk` TXT record to preserve GitHub domain verification. GitHub Pages provides HTTPS and redirects the original GitHub Pages URL and `www` to the custom domain.

This repository keeps the static website on `main` and `gh-pages`. GitHub Pages publishes the root of `gh-pages`; no Zola build or custom workflow is needed. Both branches were synchronised when replacing the original site, preserving the previous content in Git history.

After editing and committing on `main`, publish with:

```sh
git push origin main:main main:gh-pages
```

If either remote branch has changed, fetch and reconcile those changes before publishing. Do not force-push. All asset links are relative. See [GitHub's publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Traffic analytics

Cloudflare Web Analytics is configured for `moritzfalk.com` using manual JavaScript snippet installation. Each language page loads the same Cloudflare-provided module before its closing body tag. The site token in the HTML is a public analytics identifier, not an account credential. Hosting and DNS remain unchanged.

View visits, page views, and referrers in the [Cloudflare dashboard](https://dash.cloudflare.com/9d0bff38ab38f698c0966b81b81c9998/web-analytics/overview/visits?siteTag~in=6a34d9fbe1c941e980039478adab12a6&excludeBots=Yes). Collection begins after deployment; statistics may take a few minutes to appear.

## Content and media

English is the default at `index.html`. Complete German and Japanese versions live at `de.html` and `ja.html`, with a language selector on every page. Each page has inline styles and shares the same assets; keep layout and content changes consistent across all three pages. The Japanese about and contact section states that Japanese proficiency is approximately JLPT N4 (self-assessed) and English is preferred for technical discussions. The downloadable CV remains in English. Language selection is explicit, with no automatic redirect. Alternate-language metadata is included for search engines. Each project has a stable anchor: `blick`, `arc`, `custom-engine`, `retro-racer`, `ddgi`, `rasterizer`, and `ray-tracer`.

The supplied portrait is stored at `assets/moritz-falk.jpg`. The header uses square, prefiltered copies from `assets/previews/`, preserving the previous centre crop. When replacing the portrait, regenerate its preview sizes as well; the original photo is unchanged.

Project media and links:

- Blick’s official SVG logo links to https://blickeditor.com/. The section includes an article card with the NASA Apollo cover drawing. The UI Painter article is linked at https://blickeditor.com/blog/caching-an-immediate-mode-ui.
- ARC links to the “ARC: A New ImGUI Library” talk from Better Software Conference 2025: https://www.youtube.com/watch?v=UULQyRKc6sM.
- The custom engine uses the full 1080p source frame at 1:10, including the presenter inset, and links to the supplied unlisted demo: https://www.youtube.com/watch?v=VtJMUp938f8.
- SynthForce 2099 links to the team's itch.io submission and includes its screenshot: https://deltaofpie.itch.io/synthforce-2099.
- MiniRay links to https://github.com/moritzfalk/MiniRay and includes `GitHubShot.PNG` from that repository.
- The software rasterizer uses an H.264 copy of the supplied GIF, with controls and no autoplay. Its reference is https://github.com/ssloy/tinyrenderer.
- DDGI uses the supplied February 10, 2023 recording, remuxed for progressive playback without re-encoding. Original audio is preserved.

The original local media files are unchanged. Videos use `preload="none"`; YouTube thumbnails are stored locally and link directly to YouTube, avoiding embedded players that can require visitors to sign in before playback. The ARC preview uses a 1440p source frame at 10:30, framed with CSS to exclude the presenter inset. New preview filenames avoid stale cached thumbnails.

The downloadable CV is an unchanged copy of the supplied PDF, including its postal address. The webpages list Stuttgart, the supplied email address, and the supplied X profile at https://x.com/falk_moritz. Email, X, and CV links appear in the about and contact section on all three language versions, with a contact shortcut in the header. Replace `assets/moritz-falk-cv.pdf` if a different public CV is preferred.

Project dates and technical descriptions follow the supplied CV. No project URLs, screenshots, testimonials, performance figures, or qualifications have been invented. The Blick project links to the published UI Painter article.

The about and contact section includes a compact co-founder affiliation with a linked Dihedron Software logo in all three languages. Programming and spoken languages use inline labels on two rows. Its official small-format logo comes from https://dihedron.net/static/dihedron/favicon.png, stored locally as `assets/dihedron-logo.png`; the card links to https://dihedron.net.

Small raster images have prefiltered variants in `assets/previews/`, generated with Lanczos3 reduction and JPEG shrink-on-load disabled. Project thumbnails have separate 88×66 mobile and 144×96 desktop versions at 1×, 2×, and 3× density, including the existing dark letterboxing. The 72-CSS-pixel portrait uses 144/216/288/432/576-pixel square versions with width descriptors and `sizes="72px"`. A 144-pixel minimum gives modest zoom extra resolution, while larger versions extend up to the original square crop; the Dihedron icon uses 36/54/72/108-pixel previews and the 128-pixel original with width descriptors and `sizes="18px"` for its 18-pixel content box. Its 36-pixel minimum also gives modest zoom extra resolution. The article cover uses 85/125/170/250/255/375-pixel widths with `srcset` and `sizes`. JPEG previews use quality 90 and 4:4:4 chroma sampling; the cover and logo remain PNGs. All versions derive from the original local assets, which remain available for expanded views. Regenerate affected previews when replacing an image. This requires no runtime image service or extra JavaScript.
