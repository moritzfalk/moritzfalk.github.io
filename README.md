# Moritz Falk — CV website

A static, responsive portfolio built from CV_English.pdf. The page uses plain HTML and inline CSS, system fonts, and native expandable project sections. No build step, external fonts, or dependencies are required. YouTube videos use linked preview images that open in a new tab. No JavaScript is needed.

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

## Content and media

English is the default at `index.html`. Complete German and Japanese versions live at `de.html` and `ja.html`, with a language selector on every page. Each page has inline styles and shares the same assets; keep layout and content changes consistent across all three pages. The Japanese introduction states that Japanese proficiency is approximately JLPT N4 (self-assessed) and English is preferred for technical discussions. The downloadable CV remains in English. Language selection is explicit, with no automatic redirect. Alternate-language metadata is included for search engines. Each project has a stable anchor: `blick`, `arc`, `custom-engine`, `retro-racer`, `ddgi`, `rasterizer`, and `ray-tracer`.

The supplied portrait is stored at `assets/moritz-falk.jpg` and displayed with a square CSS crop in the introduction. Replace that file to update the photo on all three pages; the original photo is unchanged.

Project media and links:

- Blick links to https://blickeditor.com/ and uses the existing blog screenshot. The UI Painter article is linked at https://blickeditor.com/blog/caching-an-immediate-mode-ui.
- ARC links to the “ARC: A New ImGUI Library” talk from Better Software Conference 2025: https://www.youtube.com/watch?v=UULQyRKc6sM.
- The custom engine links to the supplied unlisted demo: https://www.youtube.com/watch?v=VtJMUp938f8.
- SynthForce 2099 links to the team's itch.io submission and includes its screenshot: https://deltaofpie.itch.io/synthforce-2099.
- MiniRay links to https://github.com/moritzfalk/MiniRay and includes `GitHubShot.PNG` from that repository.
- The software rasterizer uses an H.264 copy of the supplied GIF, with controls and no autoplay. Its reference is https://github.com/ssloy/tinyrenderer.
- DDGI uses the supplied February 10, 2023 recording, remuxed for progressive playback without re-encoding. Original audio is preserved.

The original local media files are unchanged. Videos use `preload="none"`; YouTube thumbnails are stored locally and link directly to YouTube, avoiding embedded players that can require visitors to sign in before playback. The ARC preview uses the video’s `maxres2.jpg` typography demo still, framed with CSS to exclude the presenter inset. Both the rasterizer and DDGI descriptions mention the author's sharing on Handmade Network's #showcase-projects Discord channel; no specific Discord message links were supplied.

The downloadable CV is an unchanged copy of the supplied PDF, including its postal address. The webpages list Stuttgart, the supplied email address, and the supplied X profile at https://x.com/falk_moritz. Email and X contact links appear in both the introduction and contact section on all three language versions. Replace `assets/moritz-falk-cv.pdf` if a different public CV is preferred.

Project dates and technical descriptions follow the supplied CV. No project URLs, screenshots, testimonials, performance figures, or qualifications have been invented. The Blick project links to the published UI Painter article.
