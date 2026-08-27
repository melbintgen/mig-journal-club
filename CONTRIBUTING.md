---
title: "Contributing"
---

There are three ways to contribute, in increasing order of effort.

## 1. Fix something — one click

Every page has an **"Edit this page"** link in the right-hand margin. Click it and
GitHub opens an editor, forks the repository for you, and offers to open a pull
request. You do not need to install anything, or know git.

Use it for typos, broken links, a mangled citation, or a point we recorded wrong.
Small corrections are genuinely welcome — nobody will think less of a one-word PR.

## 2. Propose a paper

Open a [paper proposal](https://github.com/melbintgen/mig-journal-club/issues/new?template=propose-paper.yml).
You do not have to present it yourself.

## 3. Report about the meeting

Reports are usually drafted from the recording by an organiser and then reviewed
by the presenter. If you would rather write your own, do that — it is better.

### The process

1. **Copy `_template/`** to `posts/YYYY-MM-DD-short-slug/` and rename it. The date
   prefix is a filing convention; the `date:` field in the front matter is what
   actually orders the site, so keep the two in sync.
2. **Write the report** in `index.qmd`. Fill in every front-matter field.
3. **Open a pull request.** The PR template has a short checklist — it exists to
   catch the two things that actually cause problems, copyright and attribution.
4. **A second person reviews and merges.** Never merge your own report. The
   reviewer checks the science, and checks that criticism reads as being about the
   work rather than the people.

To preview locally you need [Quarto](https://quarto.org/docs/get-started/):

```bash
quarto preview
```

This is optional. Reports are prose, so the GitHub pull request diff is perfectly
readable on its own, and CI renders every PR to catch broken YAML.

### Front matter

```yaml
---
title: "Short descriptive title, not the paper's title"
description: "One sentence. Shows in the listing and in link previews."
date: 2026-08-18
author: "Presenter Name"
categories: [single-cell, foundation-models, benchmarking]
draft: true
---
```

`draft: true` hides the report from the listing while you work. Remove it when
ready. Note the page still renders — blank — at its final URL while drafting.

**Once a report is merged, do not rename its folder.** The URL is the permanent
address people cite and link to.

### Categories

Pick from this list, so the sidebar stays usable:

`single-cell` · `spatial` · `multi-omics` · `microbiome` · `genomics` ·
`statistics` · `causal-inference` · `experimental-design` · `batch-effects` ·
`machine-learning` · `foundation-models` · `benchmarking` · `reproducibility` ·
`meta-science`

Two or three per report is plenty. To add a new category, propose it in your PR —
the point of a fixed list is that `scRNA-seq`, `scRNAseq` and `single-cell RNA-seq`
don't become three separate entries.

## Figures and copyright {#figures}

This is a public repository, so this part matters.

- **Never commit a PDF of a paper.** Link to the DOI.
- **Do not screenshot figures from paywalled papers.** Reproducing a figure from a
  closed-access paper on a public website is a copyright breach.

A figure in a report must be one of:

1. **Your own** — a schematic you drew, or a plot you made from public data.
2. **From an open-access paper under a CC licence**, reproduced with attribution
   and a link to the source. Check the licence; "free to read" is not the same as
   "free to reuse".
3. **Absent.** Describing a figure in prose is almost always enough, and it is
   what most of our reports do.

Short quotations from a paper are fine, in quotation marks, with a citation.

## Writing style

The house style is narrative prose, not bullet-point minutes. What we are trying
to capture is the *argument* — the objection someone raised, why it mattered, and
whether it survived. A reader who was not in the room should be able to follow the
reasoning.

- Sections follow the shape of the discussion, not a fixed template.
- Name the presenter and anyone who proposed follow-up reading. Attribute other
  points impersonally: room microphones do not separate speakers reliably, and
  people speak more freely knowing that.
- Criticise the work, not the authors. See the
  [code of conduct](CODE_OF_CONDUCT.md).
- Record disagreement that was left unresolved. It is more useful than a tidy
  consensus that nobody actually reached.
- If the discussion relied on unpublished or in-progress work by someone in the
  room, check with them before it goes on a public site.

Do not put internal notes in `<!-- HTML comments -->`. They are passed straight
through into the published page source. Use a `::: {.content-hidden}` div instead.

The [first report](posts/2026-08-18-scfm-pretraining-scale/) is a reasonable model.
