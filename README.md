# MIG Journal Club

Readings and discussion from the [Melbourne Integrative Genomics](https://research.unimelb.edu.au/integrative-genomics)
journal club at the University of Melbourne.

**→ [Go to the site](https://melbintgen.github.io/mig-journal-club/)** to read about
the next JC meeting, and the reports from previous meetings.

Each meeting is summarised: what the paper claimed, what we discussed, what was
left unresolved, and suggested follow-up reading.

## Contributing

You do not need to know git, and you do not need to install anything. Everything
below can be done in a web browser.

### Where things live

| What you want to change | File |
|---|---|
| The front page (intro, next meeting) | `index.qmd` |
| When we meet, how to join, recording policy | `about.qmd` |
| A past meeting report | `posts/YYYY-MM-DD-slug/index.qmd` |
| These contributing notes | `CONTRIBUTING.md` |

Reports live one folder per meeting. Click **`posts/`** at the top of this page,
then the folder for the meeting — for example `2026-08-18-scfm-pretraining-scale/`
— then **`index.qmd`**. That one file is the whole report.

### Fixing a typo or an error (5 minutes)

1. Open the page on the [live site](https://melbintgen.github.io/mig-journal-club/).
2. In the **right-hand margin**, click **"Edit this page"**. This opens the exact
   file that produced the page, so you never have to hunt for it.
3. GitHub opens an editor. If you have write access it will let you edit straight
   away; if not it offers to **fork** the repository first — click the green
   button, it just makes your own copy. Either way you end up in the same place.
4. Make your change. The text is plain writing — no code.
5. Click the green **Commit changes...** button (top right).
6. Write a one-line description, e.g. *"Fix typo in criticisms section"*.
7. Choose **Create a new branch and start a pull request**, then
   **Propose changes**.
8. On the next screen click **Create pull request**.

That's it. Someone else reviews and merges it, and the site updates about a
minute later. Small fixes are genuinely welcome — a one-word PR is fine.

### Suggesting a paper

[Open a proposal](https://github.com/melbintgen/mig-journal-club/issues/new?template=propose-paper.yml)
and fill in the form. You do not have to present it yourself.

### Adding a report for a new meeting

1. Open `_template/index.qmd` in this repository and copy all of its text.
2. Go back to the repository home page and click
   **Add file → Create new file**.
3. In the filename box type the full path, including the slashes:
   `posts/2026-09-01-causal-inference/index.qmd`
   Typing `/` creates the folders for you as you go — you do not need to make
   them separately.
4. Paste the template in, fill it out, and follow steps 5–8 above to open a
   pull request.

Keep the date in the folder name the same as the `date:` line inside the file.
[CONTRIBUTING.md](CONTRIBUTING.md) has the category list, the house writing
style, and the rules about figures and copyright — **read the figures section
before adding any image**, since this is a public repository.

### A note on names

Meetings are recorded and reported publicly. Reports name the **presenter**, and
may name whoever suggested follow-up reading, but everything said in discussion is
attributed impersonally — "it was noted", "one attendee argued". Anyone can ask
not to be named, before or after a meeting, no reason needed. See
[about.qmd](about.qmd).

## Building locally

Requires [Quarto](https://quarto.org/docs/get-started/); nothing else.

```bash
quarto preview     # live preview at localhost:4444
quarto render      # build to _site/
```

## Licence

| | |
|---|---|
| Reports under `posts/`, and the site prose | [CC BY 4.0](LICENSE) |
| Configuration, styles, workflows, templates | [MIT](LICENSE-CODE) |

© 2026 Melbourne Integrative Genomics, University of Melbourne.

**This covers our own words only.** The papers we discuss, any quoted passages,
and any reproduced figures remain under their original terms and are not licensed
by us.
