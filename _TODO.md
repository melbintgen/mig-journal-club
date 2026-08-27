# Outstanding before / just after launch

This file starts with `_`, so Quarto never renders it. Safe to keep notes
here that shouldn't be published.

**Do not put internal notes in `<!-- HTML comments -->` inside `.qmd` files.**
Pandoc passes them straight through into the page source, where anyone can read
them with View Source. Use a `::: {.content-hidden}` div, or this file.

## Settled

- [x] **Venue** — Room 124, Building 184. On `index.qmd` and `about.qmd`.
- [x] **Cadence** — monthly, Tuesdays 3:30 pm.
- [x] **Contact for joining** — Jiadong Mao, named on `about.qmd` with no email.
      **The mailing list address is deliberately not published on the site.**
- [x] **MIG brand colour** — `$mig-blue: #094183` in `styles.scss` confirmed.

## Still open

- [ ] **CODEOWNERS** — `.github/CODEOWNERS` is commented out pending real GitHub
      usernames for Kim-Anh and Jiadong. An unrecognised username there fails
      silently: GitHub just never requests the review, with no error.
- [ ] **Jiadong to validate the 18 Aug report** now the site is up.
- [ ] Consider whether `statgen-journal-club` should be archived or point here —
      two journal club sites under one org with no signal about which is current.

## Repo settings (GitHub web UI, needs org admin)

- [x] Create `melbintgen/mig-journal-club`, public, empty
- [x] Settings → Actions → General → Workflow permissions → **Read and write**
- [x] `gh-pages` branch created (orphan commit pushed manually — the publish
      action requires it to exist before CI can run)
- [ ] Settings → Pages → source = `gh-pages`, folder `/ (root)`
- [ ] Branch protection on `main`: require a PR + one approving review, allow
      admin bypass. This is what actually enforces "someone else merges".

## Later

- [ ] giscus comments — revisit at 6–8 posts. Config is pre-written and commented
      out in `posts/_metadata.yml`.
