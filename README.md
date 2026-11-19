# Katie Buck — Clinical Research Specialist

Professional bio and hero page for Katie Buck, a Clinical Research Specialist based in Carolina Beach, NC. The page is a static site for the clinical research and CRO audience. Wording for skills, experience, certifications, education, and affiliations is taken from her resume. Nothing on the page adds employers, dates, metrics, certifications, or testimonials that the resume does not contain.

**Live site:** https://willyd61.github.io/Katie-Buck-Bio/

The live URL works after GitHub Pages is set to build from GitHub Actions and the workflow on `main` has succeeded. See [Deploy](#deploy).

## Purpose

Give recruiters, study teams, and collaborators a fast, readable public profile covering:

- Areas of focus, including site activation, study startup, eTMF, ICH-GCP, and regulatory submissions
- Professional experience at Syneos Health (Site Activation Specialist I, September 2025 – August 2026) and IQVIA (Clinical Trials Assistant Intern, August 2024 – September 2025)
- Education, certifications, and the UNCW Student Association for Clinical Research (SACR) affiliation
- Contact by email and LinkedIn, plus the resume as a Word file and a PDF export

## Repository structure

```
.
├── .github/workflows/pages.yml   # GitHub Pages deploy
├── assets/
│   ├── Katie-Buck-Resume.docx    # Original resume
│   ├── Katie-Buck-Resume.pdf     # LibreOffice export of that resume
│   ├── apple-touch-icon.png
│   ├── favicon-32.png
│   └── og-image.png              # Social card (text only, no portrait)
├── css/styles.css
├── favicon.svg
├── index.html
├── robots.txt
├── sitemap.xml
├── LICENSE
└── README.md
```

There is no framework and no build step for local preview. The Pages workflow copies the site files into an artifact and deploys that artifact.

## Local preview

From the repository root:

```bash
python3 -m http.server 8080
```

Open http://127.0.0.1:8080/

Paths are relative, so the same files work at the project URL `https://willyd61.github.io/Katie-Buck-Bio/`.

## Deploy

Hosting matches [willyd61/willyd61.github.io](https://github.com/willyd61/willyd61.github.io): GitHub Pages with `build_type` workflow, not a branch deploy.

`.github/workflows/pages.yml` runs on every push to `main` and from **Actions → Deploy Katie Buck bio to GitHub Pages → Run workflow**. Permissions are limited to `contents: read`, `pages: write`, and `id-token: write`. The workflow uses `actions/configure-pages`, `actions/upload-pages-artifact`, and `actions/deploy-pages`.

These repository settings are outside the code and still have to be set in GitHub:

1. **Settings → Pages → Build and deployment → Source: GitHub Actions.**
2. **Description.** The repository description is still the stub text. A fitting description is `Professional bio for Katie Buck, Clinical Research Specialist.`
3. **Topics.** None are set. Useful topics: `clinical-research`, `github-pages`, `biography`.
4. **Website / homepage:** `https://willyd61.github.io/Katie-Buck-Bio/`

Until the Pages source is GitHub Actions, pushes will not publish the site.

## Accessibility

The page targets WCAG 2.1 AA:

- Semantic landmarks (`header`, `nav`, `main`, `section`, `footer`) and one `h1`
- A skip link, visible keyboard focus, and underlined or bordered links
- Text contrast checked for body copy, hero text, and controls on their backgrounds
- No information that depends on color alone, and no text baked into images except the social card and icons
- Responsive, mobile-first layout, large enough hit targets for the primary actions, and `prefers-reduced-motion` support
- The resume summary and role descriptions are real text, so they can be resized, copied, and read by assistive technology

## SEO

- Unique title, meta description, canonical URL, and `lang="en"`
- Open Graph `profile` tags and a Twitter large-image card
- JSON-LD `Person` schema, including `sameAs` for LinkedIn: https://www.linkedin.com/in/katie-victoria-buck
- `favicon.svg`, a PNG favicon, `robots.txt`, and `sitemap.xml`
- The social image is a text card. The resume has no portrait, so the page does not use one

## Privacy

This repository is public.

- The page and this README publish Carolina Beach, NC, the email address Ktvbuck12@gmail.com, and LinkedIn at https://www.linkedin.com/in/katie-victoria-buck.
- The resume has no street address. None is published here.
- The downloadable resume files do not include a telephone number. None is published on the page or in this README.

## Resume files

`assets/Katie-Buck-Resume.docx` is the Word resume with the telephone number removed from the contact line. The email address and LinkedIn hyperlink are unchanged.

`assets/Katie-Buck-Resume.pdf` is a one-page export of that file from LibreOffice Writer 24.2. The Word file uses Garamond, which was not installed in the conversion environment. The export embeds EB Garamond under the family name Garamond so the PDF stays on one page. The wording matches the Word file, including the email and LinkedIn hyperlinks. Glyph shapes are EB Garamond rather than Microsoft Garamond.

The visible resume text says “linkedin” only. The URL was stored as a hyperlink in the document and was confirmed as https://www.linkedin.com/in/katie-victoria-buck.

## What the resume does not contain

The page leaves these out rather than filling them in:

- Graduation years, an associate-degree major, GPA, or honors
- Certification dates or credential numbers
- A portrait
- Counts, percentages, or other performance metrics
- Testimonials
- A middle name printed on the resume. The page uses the name Katie Buck

“Investigator Oversite” is spelled the way the resume spells it.

## Credits

- Biographical content and resume: Katie Buck
- Site published from this repository by [willyd61](https://github.com/willyd61)
- Hosting: GitHub Pages
- PDF export: LibreOffice Writer
- Pages workflow pattern: [willyd61/willyd61.github.io](https://github.com/willyd61/willyd61.github.io)

## License

Site code (HTML, CSS, page images, and workflow configuration) is under the [MIT License](LICENSE). Copyright (c) 2026 willyd61.

The resume files and the biographical content on the site are © Katie Buck, all rights reserved. They are not covered by the MIT License.
