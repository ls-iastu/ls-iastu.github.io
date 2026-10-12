# Shuo Liu: personal academic website

Source for **https://ls-iastu.github.io**, the homepage of Shuo Liu, Gordon and Betty Moore Postdoctoral Research Associate in the Department of Physics at Princeton University.

The site is built with [Jekyll](https://jekyllrb.com/) on GitHub Pages. Every push to `master` rebuilds and publishes it automatically.

## Where things live

| What | File |
| --- | --- |
| Home page text | `_pages/about.md` |
| CV (academic career, presentations and talks) | `_pages/cv.md` |
| Publications page layout | `_pages/publications.html` |
| One file per paper | `_publications/*.md` |
| Name, links, department, address, sidebar and footer info | `_config.yml` (the `author:` block) |
| Header links | `_data/navigation.yml` |

## Adding a paper

Create a new file in `_publications/`, for example `_publications/number-17.md`:

```yaml
---
title: "Paper title"
collection: publications
category: manuscripts          # use "preprints" for arXiv-only papers
date: 2026-03-01
venue: 'Physical Review Letters'
authors: 'Shuo Liu<sup>*</sup>, Co-Author<sup>*</sup>, Another Author<sup>†</sup>'
journal: 'Phys. Rev. Lett. 136, 010101 (2026)'   # leave empty for preprints
arxiv: '2601.01234'
paperurl: 'https://doi.org/...'                   # leave empty for preprints
---
```

For a paper that is accepted but not yet out, set `journal` to e.g. `'Phys. Rev. Lett. (accepted)'` and leave `paperurl` empty; the title then links to arXiv and the arXiv number is shown after the journal line. Add `pin: true` to list a paper first within its year.

`<sup>*</sup>` marks joint first authors and `<sup>†</sup>` marks corresponding authors. Shuo Liu's name is bolded automatically. Journal articles are grouped by the year in `date`; preprints are listed after them, newest first.

## Credits

Based on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, itself a fork of [Minimal Mistakes](https://mademistakes.com/work/minimal-mistakes-jekyll-theme/). See `LICENSE` (MIT).
