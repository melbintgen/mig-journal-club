# Outstanding before / just after launch

This file starts with `_`, so Quarto never renders it. Safe to keep notes
here that shouldn't be published.

**Do not put internal notes in `<!-- HTML comments -->` inside `.qmd` files.**
Pandoc passes them straight through into the page source, where anyone can read
them with View Source. Use a `::: {.content-hidden}` div, or this file.

## Needs a real value

- [ ] **Venue for 1 Sept** — `index.qmd` currently says "venue to be confirmed".
- [ ] **Standing cadence and usual room** — `about.qmd` says "roughly fortnightly,
      Tuesdays at 3:30 pm". Confirm.
- [ ] **Contact point for joining** — `about.qmd` says "contact the journal club
      organisers". Needs a name or a role address.
      **The mailing list address is deliberately not published on the site.**
- [ ] **CODEOWNERS** — `.github/CODEOWNERS` is commented out pending real GitHub
      usernames for the organisers.
- [ ] **MIG brand colour** — `styles.scss` uses `$mig-blue: #094183` as a guess.

## Repo settings (GitHub web UI, needs org admin)

- [ ] Create `melbintgen/mig-journal-club`, public, **empty** (no README/licence/
      gitignore — they would conflict with this scaffold's first commit)
- [ ] Settings → Actions → General → Workflow permissions → **Read and write**
      *(do this before the first push, or `publish.yml` fails on its first run)*
- [ ] After the first successful publish: Settings → Pages → source = `gh-pages`
- [ ] Branch protection on `main`: require a PR + one approving review, allow
      admin bypass. This is what actually enforces "someone else merges".

## Review

- [ ] **Jiadong to validate the 18 Aug report** once the site is up.
- [ ] Consider whether `statgen-journal-club` should be archived or point here —
      two journal club sites under one org with no signal about which is current.

## Later

- [ ] giscus comments — revisit at 6–8 posts. Config is pre-written and commented
      out in `posts/_metadata.yml`.
