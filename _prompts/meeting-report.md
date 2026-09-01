# Prompt: transcript → meeting report

Reconstructed from the 18 Aug 2026 session, which produced
`posts/2026-08-18-scfm-pretraining-scale/index.qmd`. That post is the worked
example — read it before using this.

`_prompts/` starts with `_`, so Quarto never renders it. Safe for internal notes.

**How to use:** attach the transcript(s), fill in the four bracketed fields at the
top, paste the rest verbatim. The output format lives in `_template/index.qmd`,
not here — this prompt points at it rather than restating it, so the two cannot
drift apart.

---

## The prompt

````
We ran a journal club on this paper:

  PAPER:       [URL or DOI]
  PRESENTER:   [name]
  DATE:        [YYYY-MM-DD]
  ANNOUNCEMENT / SIDE PAPERS: [paste the invitation email or Slack message,
                               including any follow-up papers attendees raised]

The transcripts are attached.

Write a report of the discussion for the MIG journal club site
(https://melbintgen.github.io/mig-journal-club/).

AUDIENCE. Colleagues at MIG who missed the meeting and want to know what they
missed. Assume they are technically literate but have not read the paper. The
report should make a non-attendee wish they had been there. It is published
publicly, so the paper's authors may well read it.

TASK. Familiarise yourself with the paper for context, then focus on what was
discussed, criticised and defined. Do not minute the meeting — convey the
substance of the arguments.

SCOPE. Draft only. Produce the contents of the one file and stop there.
A human creates the post folder, opens the pull request, has it reviewed by
someone who attended, removes `draft: true`, and merges. Do not create branches,
open pull requests, commit, or publish anything. Do not decide that a
contentious passage is fine to publish — flag it and let the reviewer rule.

WRITING
- Narrative scientific prose. Not bullet-point minutes, not an executive summary.
- Concise. Use few headings, only where the discussion genuinely changed subject.
  Headings should name the argument, not act as generic labels.
- Australian English.
- Capture each argument properly: the objection raised, why it mattered, and
  whether it survived. An argument stated but not explained is not worth including.
- Record disagreements that were left unresolved. Do not manufacture consensus.
- Do not narrate the meeting's own structure ("the discussion then turned to…").
- No AI-isms. Do not write "the room" — say "the group", "attendees", or just
  describe the argument. Also avoid: delve, landscape, tapestry, underscores,
  highlights the importance of, it is worth noting, in today's world.

ATTRIBUTION — this is a public site, so get this right
- Name the presenter.
- Name whoever proposed follow-up reading.
- Name an individual for a specific substantive contribution ONLY where the
  transcript makes the speaker unambiguous.
- Otherwise attribute impersonally: "it was noted", "one attendee argued",
  "several attendees".
- Criticise the work, never the authors. Delete any sentence speculating about
  the authors' competence, motives, seniority or background, however mildly.
- Omit room, building and logistics details.
- Flag separately (do not publish) anything that depended on unpublished or
  in-progress work by an attendee, so it can be cleared first.

VERIFY — do not trust the transcript
- Room-microphone transcripts mangle names badly. Check every person, paper,
  method, tool and institution before it goes in. If you cannot verify a name,
  write "a review was cited" rather than guessing.
- Check every citation against PubMed or the DOI. Give the full citation with a
  DOI link.
- Check every number from the paper (sample sizes, percentages, dataset scale)
  against the paper itself, not against the transcript.
- List at the end anything you could not verify, so I can check it.

OUTPUT — one Quarto file at posts/YYYY-MM-DD-short-slug/index.qmd

Start from the repository's template, which is the canonical skeleton:
https://github.com/melbintgen/mig-journal-club/blob/main/_template/index.qmd
(or `_template/index.qmd` in a local clone).

Keep its front-matter fields, its paper callout block and its closing note
exactly as they are. Do not invent a different structure. If the template and
this prompt ever disagree, the template wins — it is the file contributors
actually copy.

Filling it in:
- title        Short and descriptive, naming the topic. NOT the paper's title.
- description  One line. What the paper claims, then the open question the
               discussion left standing. Drives the listing, link previews and
               the feed, so it has to earn a click on its own.
- date         YYYY-MM-DD, matching the folder-name prefix.
- author       Leave empty. These are transcript summaries, not authored pieces.
- categories   Two to four, only from the list in CONTRIBUTING.md.
- draft        Leave `draft: true` in place. Whoever reviews it removes that line.

The template ships three placeholder headings ("The paper", "Discussion",
"Follow-up reading"). Those are a starting point, not a form to fill in —
replace them with headings that name the actual arguments. The 18 Aug report
used "The study", "Terminology clarified in discussion", "Criticisms", and
"Transfer works for language but maybe not for expression?".
````

---

## Why each constraint is there

Everything below was learned the hard way on the first run. The original prompt
was three sentences; the rest is scar tissue.

**"Not the room" and "not minutes"** — your correction after the first draft:
*"this is terrible writing, too many AI-isms (like, what is 'the room', can't we
just say the group), it has too many titles, it is also not concise. We don't want
to report what the meeting was about or minute it."* The first draft had a heading
per topic and read like an agenda.

**Verify every name** — the first published version said *"A review by Jiang was
cited."* Jiadong corrected it to **Shihua Zhang's team**. The transcript had
mangled it and nobody caught it before publication. Assume every proper noun in a
room-mic transcript is wrong until checked.

**Criticise the work, not the authors** — the first draft ended the criticisms
section with a line suggesting the study would have been better designed by
single-cell specialists. It was flagged pre-publication, survived into the first
commit, and Jiadong deleted it outright. It is the single most likely sentence to
be found by the people it is about.

**Name individuals only where unambiguous** — Jiadong changed *"The more
substantive contribution was a reframing…"* to *"Jiadong proposed a reframing…"*.
Impersonal attribution is the safe default, but where the speaker is certain and
the contribution is substantive, crediting them is better. The transcript's room
mic is what makes this a judgement call rather than a rule.

**`description` frames the claim, not the verdict** — originally it asserted the
paper's finding as fact. Reworded to *"The paper reports that… Was there a flaw in
the study design?"* — accurate to a meeting that did not accept the result at face
value, and it earns the click.

**`author: ""`** — these are summaries compiled from a recording. Attributing them
to the presenter misrepresents who wrote them; attributing them to the compiler
foregrounds the wrong person. Empty renders cleanly with no byline.

**No logistics** — the first draft carried "Room 124, Building 184" into a
permanent public archive page. Venue belongs on `about.qmd`, where it can be
updated when it changes.

**The template is the single source of truth for format** — the first draft of
this prompt spelled out the front matter, callout and closing note inline, which
immediately disagreed with `_template/index.qmd` (the prompt omitted `draft:
true`, and the template's generic headings contradicted the prompt's "name the
argument, not a generic label"). Two copies of a format drift the moment either
is edited. The prompt now links to the template and only adds the things a
template cannot express: what makes a good title, how to frame the description,
and the attribution and verification rules.

## Still worth adding next time

- Ask for a **short list of unverified claims** at the end, so review has
  something concrete to check rather than re-reading everything.
- The transcripts for 18 Aug were attached in chat and never saved to disk. Only
  the finished report survives in `~/University of Melbourne/MIG/journal-club/`.
  Keep the raw transcript somewhere — it is the only way to check a disputed
  attribution later.
