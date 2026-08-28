# sieal.org

Website for the **Spatial Intelligence and Environmental Analytics Lab (SIEAL)**, Department of Geomatic
Engineering and Geospatial Information Systems, JKUAT, Nairobi.

Built with Jekyll on the [academic-website-template](https://github.com/sbryngelson/academic-website-template)
(MIT). Deployed to GitHub Pages automatically: **push to `main` and the site rebuilds itself.** You never
need to install anything locally.

---

## Everyday jobs

All of these can be done by editing a file in the GitHub web interface and clicking *Commit changes*.
The site rebuilds in about two minutes.

### Add a publication

Edit **`assets/ref.bib`** and paste a new BibTeX entry. Copy the shape of an entry already in the file.

```bibtex
@article{mbani2027example,
  title   = {Title of the paper},
  author  = {Mbani, Benson and Adhiambo, Ruth Mellanie},
  journal = {Journal Name},
  volume  = {1},
  pages   = {123},
  year    = {2027},
  doi     = {10.1038/xxxxx},        % adds a DOI button
  file    = {mbani2027.pdf},        % optional: put the PDF in papers/
  abstract = {...},                 % optional: adds an Abstract toggle
}
```

Two rules:

1. **The key must be unique** — that's the `mbani2027example` part. Reusing a key silently drops an entry.
2. **Use the right type.** `@article` → Journal articles, `@unpublished` → In preparation,
   `@misc` → Datasets and research software, `@phdthesis` → Thesis. Anything else won't appear.
3. **Never put a `%` comment inside an entry.** `%` only works *between* entries. A comment line
   between the `{` and the closing `}` fails the whole build with
   `Failed to parse BibTeX`. Put notes on the line above the `@`.

### Add a news item

Edit **`_data/news.yml`**. Newest goes at the top. The three most recent show on the home page.

```yaml
- date: March 2027
  headline: "What happened"
```

### Add or remove a lab member

Edit **`_data/team_members.yml`**, and put a square photo (500×500 or larger) in `images/team/`.

```yaml
- name: Full Name
  photo: team/full-name.jpg
  info: "Role — one line on what they work on"
  email: name@example.com        # optional
  scholar: https://...           # optional
  github: https://...            # optional
  linkedin: https://...          # optional
```

When someone leaves, move their entry to **`_data/alumni.yml`**. The Alumni table appears automatically
once that file has an entry.

```yaml
- name: Full Name
  duration: 2026-28
  info: Now a PhD student at ...
```

### Change page text

The pages are in **`_pages/`** — `home.md`, `research.md`, `team.md`, `partner.md`, `join.md`,
`contact.md`, `about.md`, `publications.md`, `software.md`. They are Markdown; edit the words
and commit.

Adding a page: create the file with a `permalink:`, then add its name to `nav_pages` in
`_config.yml`. A nav entry whose name has no matching permalink renders a dead link.

### Update the openings

Edit **`_pages/join.md`**. Keep it current — a Join page advertising a closed position is worse than
no Join page. If nothing is open, say so plainly and say when that will change.

---

## Settings

**`_config.yml`** holds the lab identity, the links shown in the sidebar and footer, and the
navigation menu. Blank links are hidden automatically, so removing a link is as simple as emptying it.

Two contact addresses: `email` (general, shown in the sidebar, footer and Contact page) and
`apply_email` (the Join page only, so applications stay filterable). Both are forwarders on
`sieal.org` configured at Namecheap — if either starts attracting spam, change the alias there
and update it here. Nothing else on the site needs to change.

## Domain

`CNAME` contains `sieal.org`. For that to work, the domain's DNS needs:

| Type  | Name  | Value |
|-------|-------|-------|
| A     | `@`   | `185.199.108.153` |
| A     | `@`   | `185.199.109.153` |
| A     | `@`   | `185.199.110.153` |
| A     | `@`   | `185.199.111.153` |
| CNAME | `www` | `sieal-lab.github.io` |

Then in the repo: **Settings → Pages → Custom domain** → `sieal.org`, and tick *Enforce HTTPS*
once the certificate has been issued (this can take up to an hour).

## Running it locally (optional — you do not need this)

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Pulling in template improvements (optional)

```bash
git remote add upstream https://github.com/sbryngelson/academic-website-template.git
git fetch upstream && git diff upstream/main -- _layouts _includes _sass
```

---

## Custom domain

The site is served from **https://sieal.org**. `CNAME` holds the domain and `url:` in
`_config.yml` must always match it — if you ever move the site, change both together or
canonical links and the sitemap will point at the wrong host.

DNS lives at Namecheap (Domain List → Manage → Advanced DNS):

| Type  | Host  | Value |
|-------|-------|-------|
| A     | `@`   | `185.199.108.153` |
| A     | `@`   | `185.199.109.153` |
| A     | `@`   | `185.199.110.153` |
| A     | `@`   | `185.199.111.153` |
| CNAME | `www` | `sieal-lab.github.io.` |

All four A records are required — they are GitHub's redundant edge servers, not alternatives.

## Search engines

### Getting verified

`_config.yml` has `google_site_verification` and `bing_site_verification`. Paste in the code each
tool gives you — **just the code, not the whole `<meta>` tag** — commit, and the tag appears on
every page. Then click Verify.

- Google: [Search Console](https://search.google.com/search-console) → add property → *HTML tag* method.
  Afterwards submit `sitemap.xml` and use *URL Inspection → Request indexing* on the home page.
- Bing: [Webmaster Tools](https://www.bing.com/webmasters) — it can import everything from Google.

Leave either blank and no tag is emitted.

### Page titles and descriptions

Each page's `<title>`, its Google snippet, and its social-share card come from two optional
front matter fields:

```yaml
seo_title: "Open positions - SIEAL"     # defaults to "<title> - SIEAL"
description: "Two funded junior..."     # defaults to site.description
```

Keep `seo_title` under about 60 characters and `description` between 120 and 160 — longer and
Google truncates them. Write the description as the sentence you would want someone to read in
the search results, because that is usually exactly what it becomes.
