# MIG Journal Club

Readings and discussion from the [Melbourne Integrative Genomics](https://research.unimelb.edu.au/integrative-genomics)
journal club at the University of Melbourne.

**→ [melbintgen.github.io/mig-journal-club](https://melbintgen.github.io/mig-journal-club/)**

This repository holds the source for that site. Each meeting gets a write-up:
what the paper claimed, what the room made of it, and what was left unresolved.

## Contributing

- **Spotted an error?** Use the "Edit this page" link in the margin of any page.
  GitHub forks the repo and opens a pull request for you — no git, no local setup.
- **Want to suggest a paper?** [Open a proposal](https://github.com/melbintgen/mig-journal-club/issues/new?template=propose-paper.yml).
- **Writing up a meeting?** Copy `_template/` to `posts/YYYY-MM-DD-slug/` and open
  a PR. See [contributing.qmd](contributing.qmd) for the full process, the category
  list, and the rules on figures.

Meetings are recorded and written up publicly. Attendees can ask not to be named —
see [about.qmd](about.qmd).

## Building locally

Requires [Quarto](https://quarto.org/docs/get-started/); nothing else.

```bash
quarto preview     # live preview at localhost:4444
quarto render      # build to _site/
```

Computational output is frozen (`_freeze/` is committed), so CI renders the site
without an R or Python toolchain.

## Licence

| | |
|---|---|
| Write-ups under `posts/`, and the site prose | [CC BY 4.0](LICENSE) |
| Configuration, styles, workflows, templates | [MIT](LICENSE-CODE) |

© 2026 Melbourne Integrative Genomics, University of Melbourne.

**This covers our own words only.** The papers we discuss, any quoted passages,
and any reproduced figures remain under their original terms and are not licensed
by us.
