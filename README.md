# google-cybersecurity-notes

This repository is now a legacy redirect stub for the old GitHub Pages URL:

- Old site: `https://gyozalab.github.io/google-cybersecurity-notes/`
- Current site: `https://gyozalab.github.io/gyoza-course-notes/`

## Brand update

This project originally started as "煎餃的 Google Cybersecurity 學習筆記" and focused on a single learning track.

After the site expanded into a broader course-notes platform, the project identity was upgraded:

- from `google-cybersecurity-notes`
- to `gyoza-course-notes`

The new name reflects the current scope better: this is no longer only a Google Cybersecurity notes site, but a multi-program learning notes hub under the gyozalab brand.

## Technical note

GitHub repository renames do not preserve the old GitHub Pages path.

That means the previous Pages URL would break if this repository disappeared. To keep old links alive, this repo is intentionally kept as a lightweight redirect layer.

Its job is simple:

- preserve previously shared URLs
- catch old GitHub Pages paths
- send visitors to the right location on `gyoza-course-notes`

## Files in this repo

```text
.
|-- index.html
|-- 404.html
`-- README.md
```

- `index.html`: redirects the old homepage to the new cybersecurity entry page
- `404.html`: catches legacy sub-paths and remaps them to the new site
- `README.md`: explains why this repository still exists

## Redirect behavior

The redirect pages preserve old links as much as possible:

1. Remove the legacy base path `/google-cybersecurity-notes/`
2. Normalize old `.html` suffixes when present
3. Route old cybersecurity note paths into `/gyoza-course-notes/cybersecurity/...`
4. Fall back to the new site root for anything else

## Maintenance policy

This repo should stay minimal and stable.

- Do not add new course content here
- Do not treat this as the main project repo
- Only update it when the destination URL or redirect rules change

If the new site structure changes again, update the `newBase` constant in both `index.html` and `404.html`.
