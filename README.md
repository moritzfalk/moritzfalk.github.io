# Moritz Falk — CV website

A static, responsive portfolio built from CV_English.pdf. The page uses plain HTML and inline CSS, system fonts, and native expandable project sections. No build step, JavaScript, external fonts, or dependencies are required.

## Preview

Open `index.html` directly, or run `python3 -m http.server 8080` from this directory and visit `http://localhost:8080`.

## GitHub Pages

Live site: https://moritzfalk.github.io/

This repository keeps the static website on `main` and `gh-pages`. GitHub Pages publishes the root of `gh-pages`; no Zola build or custom workflow is needed. Both branches were synchronised when replacing the original site, preserving the previous content in Git history.

After editing and committing on `main`, publish with:

```sh
git push origin main:main main:gh-pages
```

If either remote branch has changed, fetch and reconcile those changes before publishing. Do not force-push. All asset links are relative. See [GitHub's publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Content and media

All page content and styles live in `index.html`. Each project has a stable anchor: `blick`, `arc`, `custom-engine`, `retro-racer`, `ddgi`, `rasterizer`, and `ray-tracer`.

The Blick screenshot is from the existing blog assets. The other project sections intentionally use text until actual project media is supplied. Add images or video within the relevant `project-body` or `experiment-body`, using `figure` and `figcaption` for captions. The `.media` class supports responsive images and videos, and `.video` supports a 16:9 iframe. Give every embedded video a descriptive title, use lazy loading, and avoid autoplay. Prefer a click-to-load player for YouTube so the page does not contact YouTube until a visitor chooses to play it.

The downloadable CV is an unchanged copy of the supplied PDF, including its postal address. The webpage itself lists only Stuttgart and the supplied email address. Replace `assets/moritz-falk-cv.pdf` if a different public CV is preferred.

Project dates and technical descriptions follow the supplied CV. No project URLs, screenshots, testimonials, performance figures, or qualifications have been invented. The blog post is not linked because it has not yet been published.
