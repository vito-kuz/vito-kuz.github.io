# Claude Code Credit Sprint (Nov 1–4)

Nov 1, 2026 · @Vito

## How to use this doc

Your $100 cloud session credit expires **Wed Nov 4, 11:59 PM Pacific**. This doc gets all 12 picks done before then, all running on the credit instead of your Pro limits.

- **Where the work happens:** Claude Code cloud sessions (claude.ai/code, or the Code tab in the desktop or phone app with **Cloud** selected). Cowork, scheduled tasks and regular chats don't use the credit.
- **How each pick works:** do Step 0 once, upload the files listed for that pick, paste its prompt, walk away. Each prompt tells Claude to work without stopping and to list any assumptions in a README.
- **Checking the balance:** Settings → Usage on claude.ai. If money is left Wednesday afternoon, rerun a pick with a bigger ask (more resume versions, more games, a longer study plan).
- **Model:** keep the default (Opus or Sonnet). On Pro, Fable switches to paid usage credits once the bonus is gone.
- **Privacy:** everything goes in a **private** repo except the portfolio website (#15), which is public by design. Keep youth names, Viber exports and personal finances out of the public one.

The 12 picks: #36 Learn Git, #1 Prompt version history, #3 Prompt review, #19 Resumes, #16 Expo pitch + LinkedIn + cover letter, #15 Portfolio site, #18 OSHA-10 comparison, #21 FE roadmap, #26 Choir binder, #31 Youth meeting notes, #33 Game bank, #34 Offline kit.

## Step 0: one-time setup (about 20 minutes)

You need a GitHub account, two repos (project folders on GitHub), and Claude Code connected to them.

1. **GitHub account.** Sign up free at github.com if you don't have one. Pick a username you'd be happy putting on a resume, since the portfolio address will be `username.github.io`.
2. **Private workbench repo.** On GitHub: **+** (top right) → **New repository** → name `vito-workbench` → **Private** → tick **Add a README** → **Create**. Eleven of the 12 picks live here.
3. **Public portfolio repo.** Same steps, but name it exactly `yourusername.github.io` and choose **Public**. Only #15 uses it.
4. **Connect Claude Code.** Go to claude.ai/code. Follow the prompt to connect GitHub and allow the Claude app on both repos.
5. **Upload the input files.** In `vito-workbench`: **Add file** → **Upload files** → drag in the files from the table below → **Commit changes**. Drop them all at the top level; #36 sorts them into folders.
6. **Start a session.** At claude.ai/code, pick the repo, paste a prompt, send. You can close the tab; it keeps working.
7. **Get results back.** When it finishes, it may have saved its work on a side branch. If you see **Create PR**, click it, then on GitHub click **Merge pull request**. To download, open a file and click the download icon, or **Code** → **Download ZIP** for everything.

**Files to upload to `vito-workbench`** (all from your Claude\_general folder):

| Used by | Files |
| --- | --- |
| #19, #16, #15, #21, #18 | Kuzmych\_Forever\_Resume\_Master\_Bank\_2026-10.md, Kuzmych\_MECOP\_Civil\_Engineering\_Master\_Guide\_2026-10.md, Kuzmych\_Civil\_Engineering\_Internship\_General\_Guide\_2026-10.md |
| #26 | Choir song list.xlsx, CCS\_Choir\_Song\_Archive\_Final1.docx, Main\_Choir\_Wall\_Board\_1up\_Portrait.xlsx |
| #31 | Youth-Group-Meeting-Notes-Org-Team.md, Youth-Group-Meeting-Notes-Consolidated.md, Youth-Group-Open-Decisions-Checklist.md, Viber messages/CCS Organization Team - messages.CSV, Viber messages/Youth Leaders and helpers - messages.CSV |
| #33 | Viber messages/CCS Youth Announcements - messages.CSV, Coastal\_Retreat\_Venues\_Complete\_Reference.md |
| #1, #3 | Your current scheduled-task prompts, one .txt file per task (Cowork can export these into your Claude\_general folder for you) |
| #34 | Nothing extra; it reuses everything above |

Newest versions are listed where you have several copies (the \_2026-10 and Final1 files). If the Final1 choir archive isn't the one you consider current, swap it.

## Schedule

Four days, three or four sessions a day, with Wednesday left for the picks that reuse earlier results. Start sessions before you head out at 6 PM; they keep running while you're away.

| Day | Start these | Why this order |
| --- | --- | --- |
| Sun Nov 1 | Step 0, then #36 Learn Git | #36 sorts the uploaded files into folders that every later prompt expects. Do it while you're at the computer, since it's a lesson. |
| Mon Nov 2 | #1 Prompt history, #19 Resumes, #18 OSHA-10, #21 FE roadmap | Four independent jobs; run them side by side. Merge #1 and #19 when they finish. |
| Tue Nov 3 | #3 Prompt review, #16 Pitch + LinkedIn + cover letter, #15 Portfolio, #26 Choir binder | #3 needs #1's files; #16 and #15 reuse #19's resumes. |
| Wed Nov 4 | #31 Meeting notes, #33 Game bank, then #34 Offline kit last | #34 bundles the finished pieces from the other picks. Check the balance around 3 PM and spend what's left before 11:59 PM. |

- [ ] Sun: Step 0 done
- [ ] Sun: #36
- [ ] Mon: #1, #19, #18, #21
- [ ] Tue: #3, #16, #15, #26
- [ ] Wed: #31, #33, #34, balance check

## A. Learning Git and your Claude setup

### #36 Learn Git by doing (Sunday, in `vito-workbench`)

The only interactive one: it waits for you after each step. By the end the workbench is organized for every other pick.

```text
I'm not a programmer. Teach me Git and GitHub by doing, using this repo. Go one step at a time, explain each idea in one or two plain-English sentences, and wait for me to say "next" before moving on.

Cover, in this order: what a repo, a commit, a branch, a pull request and a merge are; how to see a file's history; how to undo a change.

As the hands-on exercise, organize this repo:
- inputs/career/ : the three Kuzmych_*.md files
- inputs/choir/ : Choir song list.xlsx, CCS_Choir_Song_Archive_Final1.docx, Main_Choir_Wall_Board_1up_Portrait.xlsx
- inputs/youth/ : the Youth-Group-*.md files, Coastal_Retreat_Venues_Complete_Reference.md, and every Viber *.CSV file
- inputs/claude-system/ : any .txt prompt files (may be empty for now)
- empty output folders career/, church/, claude-system/, offline-kit/, each with a one-line README.md saying what will go there
Use a separate commit with a clear message for each folder so I can see them in the history. Then show me how to merge your branch into main.

Finish by writing GIT-CHEATSHEET.md: the 10 things I'll actually need, written for someone who uses GitHub's website and Claude Code, not the command line.
```

### #1 Prompt version history (Monday)

Puts every scheduled-task prompt under version control, so any change shows up as a before/after and nothing can be lost. Needs the prompt .txt files uploaded to `inputs/claude-system/` first.

```text
Work without stopping to ask; if anything is unclear, decide sensibly and list your assumptions at the top of claude-system/README.md.

Build a version-controlled library of my Claude scheduled-task prompts from the .txt files in inputs/claude-system/ (one or more files per task).

1. For each task create claude-system/prompts/<task-name>.md containing the prompt text EXACTLY as given. Do not fix, reword or reformat the prompt itself. Above it, add a short header: task name, schedule and purpose if the file states them (otherwise "unknown"), and the date of the version.
2. If a task has more than one dated version, commit the oldest first and each newer one as its own later commit, so GitHub's history shows exactly what changed between versions.
3. Write claude-system/README.md: a table of every task (name, schedule, link to its file, one-line purpose), then a "How to update a prompt" section for a non-coder: editing a file on GitHub's website, writing a commit message that says what changed and why, viewing a file's history and differences, and restoring an older version.
4. Start claude-system/CHANGELOG.md with today's entry.
```

### #3 Review all task prompts together (Tuesday, after #1 is merged)

Aims straight at the usage-limit failures. It only proposes changes; your live tasks stay untouched until you approve edits back in Cowork.

```text
Work without stopping to ask; list assumptions at the top of the report.

Review every prompt in claude-system/prompts/ as one system. These run unattended on a schedule on a Claude Pro plan, and several runs have failed by hitting usage limits. Goal: make them cheaper and more reliable without losing anything they do.

Write claude-system/REVIEW.md with:
1. A table per task: length in words, what it reads, what it writes, its biggest cost drivers.
2. Overlaps between tasks (the same source read by several tasks, rules repeated in several prompts) and whether a shared rules block would help.
3. Contradictions and ambiguous instructions, quoting the exact lines.
4. Padding: wording that costs tokens without changing behavior.
5. Failure risks: steps with no fallback when a connector or the laptop is unavailable, memory files that grow without limit, steps that depend on the laptop being awake.
6. A ranked top-10 list of changes with the expected effect of each.

Then write a proposed revision of each task to claude-system/proposed/<task-name>.md, with before/after word counts. Do NOT change anything in claude-system/prompts/.

Keep every rule that protects me, word for word in meaning: never create Gmail drafts; never create, edit, reschedule or delete anything in Planning Center without my approval; never touch To-Do List lines that carry another task's tag.
```

After #3: bring REVIEW.md back to a Cowork chat and decide which changes to apply. The scheduled tasks themselves can only be edited from Cowork.

## B. Career

All in `vito-workbench` except #15. Every prompt is told to use only facts from your own files and to mark gaps `[ADD]` rather than invent anything.

### #19 Tailored resumes (Monday)

```text
Work without stopping to ask; list assumptions at the top of career/resumes/README.md.

Source of truth: inputs/career/Kuzmych_Forever_Resume_Master_Bank_2026-10.md. Use the two guides in inputs/career/ only for context on MECOP and target roles.

Create one-page resumes in career/resumes/, each as .md, .docx and PDF, single column and ATS-friendly:
(a) MECOP / general civil engineering internship
(b) consulting firm (structural, transportation, water)
(c) public agency (city, county, WSDOT, ODOT)
(d) contractor / construction field role
(e) part-time or campus job
Also make (f) a public-safe copy of (a) with email only, no phone number or home address, named resume-public.md.

Never invent experience, dates, GPA, courses or certifications; write [ADD: what's missing] instead. In README.md, add a table of what each version emphasizes and a list of every [ADD] gap for me to fill.
```

### #16 Expo pitch, LinkedIn About, cover letter (Tuesday)

```text
Work without stopping to ask; list assumptions at the top of career/pitch/README.md.

Use only facts from inputs/career/ and career/resumes/. Mark gaps [ADD]. Write in my voice: a friendly, plain-spoken civil engineering student, not salesy.

Create in career/pitch/:
1. EXPO-PITCH.md for the MECOP Company Expo in mid-November (job-fair format, walking up to a company table): a 30-second spoken intro (about 75 words), three variants leaning structural, transportation and construction, a 15-second follow-up line for the end of a conversation, and 5 smart questions to ask a company. Add a practice version broken into short beats to memorize.
2. LINKEDIN.md: 5 headline options, a short About (about 600 characters) and a full About (under 2,600 characters).
3. COVER-LETTER.md and .docx: a one-page template with [BRACKETS] for the company-specific parts, plus one filled example for a general civil consulting internship.
```

### #15 Portfolio website (Tuesday, in the public `username.github.io` repo)

Before starting: download `resume-public.md` from #19, read it over, then upload it to the public repo. Everything in that file will be on the internet, so remove anything you don't want public.

```text
Work without stopping to ask; list assumptions in README.md.

Build my personal portfolio website in this repo. GitHub Pages publishes it automatically at the repo's name. Content source: resume-public.md (everything in it may be public). Use nothing else except placeholders marked [ADD].

Requirements: plain HTML and CSS with index.html at the top level, no frameworks and no build step; fast and readable on a phone; accessible; professional, with one accent color; light and dark mode.
Sections: Home (name, "Civil Engineering student at Portland State University", a two-sentence intro, a photo placeholder), Projects and coursework (cards, [ADD] where descriptions are missing), Experience, Resume (a resume.pdf you generate from resume-public.md, linked for download), Contact (email only; never a phone number or home address).

In README.md explain, for a non-coder: how to change text on GitHub's website, how to swap in a photo, and how long changes take to go live.
```

After it's merged, check **Settings → Pages** in that repo; the site address shows there.

### #18 OSHA-10 provider comparison (Monday)

```text
Work without stopping to ask; list assumptions at the top of the report.

Research online OSHA 10-Hour Construction courses (not General Industry) for a civil engineering student in Oregon and Washington. Compare at least 5 OSHA-authorized online providers on: price, how their authorization can be verified, time limits, how fast the DOL card arrives, phone friendliness, refund policy, student discounts and review quality. Check whether PSU, MECOP, ASCE or AGC student chapters offer it free or discounted. Say briefly whether OSHA-30 is worth doing instead at my stage.

Open the pages you cite. Every price gets a link and the date you checked it.

Write career/osha10/COMPARISON.md: a comparison table, one clear recommendation, and a "watch out for" list (non-authorized sellers, fake cards).
```

### #21 FE exam roadmap (Monday)

```text
Work without stopping to ask; list assumptions at the top of the roadmap.

I'm a civil engineering sophomore at Portland State (2026-27) planning to take the FE Civil exam around graduation. Build a long-range roadmap.

Research and cite, with dates checked: the current NCEES FE Civil exam specification (knowledge areas, question count, format, reference handbook version, fee) and the EI/EIT path with the Oregon and Washington boards. Look up PSU's civil engineering curriculum and map each FE knowledge area to the PSU courses that cover it.

Write career/fe-roadmap/ROADMAP.md: a term-by-term plan from now to the exam (habits during each course, such as using the NCEES Reference Handbook on homework and keeping an FE notes binder; when to start formal review; free and paid prep resources with costs), a topic checklist, and a budget. Also make a one-page printable summary PDF.
```

## C. Church and youth

All in `vito-workbench` (private). The Viber exports are large, so these prompts tell Claude to process them with a script instead of reading them whole, which also saves credit.

### #26 Choir starter binder (Tuesday)

```text
Work without stopping to ask; list assumptions at the top of church/choir-binder/README.md.

I sing in the Main Choir at my church and occasionally co-direct the Youth Choir. Inputs: inputs/choir/ (our song list workbook, the CCS Choir Song Archive catalog, and the main choir wall board). Check what language the song titles are in; if many are Russian or Ukrainian, give the announcement templates in English and that language.

Create church/choir-binder/:
1. BINDER.docx and BINDER.pdf, printable:
   - a 30/60/90-day plan for someone starting to co-direct a church youth choir
   - a timed rehearsal plan template (warm-up, new music, review, run-through, announcements, prayer)
   - a warm-up library of 20 or more exercises grouped by goal (breath, tone, range, diction, blend), each with how to lead it and how long it takes
   - a pre-Sunday checklist and a section-leader role description
   - announcement message templates (rehearsal reminder, schedule change, new song with practice link, thank-you)
2. TRACKER.xlsx with working formulas: an attendance sheet by member and date, and a song-planning sheet built from our song list (title, key, voicing or group, last sung if the data has it, and a flag when a song was used within the last 3 months, since the church rotates songs on roughly a 3-6 month cycle).
Use only songs that appear in my files. Don't make up dates.
```

### #31 Youth meeting notes, updated reference (Wednesday)

You already have a September consolidation and a newer Org Team notes file. This pick merges them with the Viber leader chats into one current reference.

```text
Work without stopping to ask; list assumptions at the top of the reference.

Inputs in inputs/youth/: Youth-Group-Meeting-Notes-Org-Team.md (newest notes), Youth-Group-Meeting-Notes-Consolidated.md (an earlier consolidation), Youth-Group-Open-Decisions-Checklist.md, and two Viber exports: "CCS Organization Team - messages.CSV" and "Youth Leaders and helpers - messages.CSV". The CSVs are large: inspect their columns, then process them with a script rather than reading them whole. Messages may be in Russian or Ukrainian; write the reference in English and keep short original quotes only where the wording matters.

Create church/youth-reference/:
1. REFERENCE.md and REFERENCE.docx, organized by theme: recurring schedule, events, roles and who does what, rules and policies, money and budget, supplies. Every item gets a date and a source (meeting notes or Viber, with the message date). Newer information wins over older; say when something changed.
2. DECISIONS-LOG.md: a table of date, decision, source, newest first.
3. OPEN-ITEMS.md: everything raised but not resolved, newest first, merged with the open decisions checklist.
Refer to people by first name as written. Leave out phone numbers, addresses and anything personal about individual teens.
```

### #33 Game and activity bank (Wednesday)

Optional: also upload Youth\_Shed\_Inventory\_Compact\_cleaned.docx so it can mark which supplies you already have.

```text
Work without stopping to ask; list assumptions at the top of church/game-bank/README.md.

Build a searchable bank of games and activities for our church youth group (teens and young adults).
Sources: (1) inputs/youth/"CCS Youth Announcements - messages.CSV": find the games, activities and events we've already done, with dates (process it with a script; messages may be in Russian or Ukrainian); (2) your own knowledge and web research for new ideas; (3) Coastal_Retreat_Venues_Complete_Reference.md for beach and retreat activities that suit those venues; (4) the shed inventory .docx if present, to mark supplies we already own.

At least 80 entries. Fields: name, type (icebreaker, team game, indoor, outdoor, beach, retreat or overnight, devotional or discussion activity), group size, time needed, prep level, supplies, energy level, rules in 3-6 steps, safety notes, "we've done this" with last date.
Keep everything appropriate for a church group: no humiliation, no unusual physical risk.

Create church/game-bank/: games.csv, GAMES.md grouped by type, and games.html: a single file that searches and filters by type, group size and indoors/outdoors, works offline on an iPhone or iPad, and loads nothing from the internet.
```

## D. Offline kit

### #34 Offline kit (Wednesday, last)

For the what-if of 2+ weeks without a computer or internet: a printable binder plus one file that opens offline on your iPhone or iPad. It runs last so it can bundle the other picks' results.

```text
Work without stopping to ask; list assumptions at the top of offline-kit/START-HERE.md.

Prepare me for a possible stretch of two or more weeks with no computer and no reliable internet (a what-if, nothing planned). I'm a civil engineering student at Portland State, a youth group leader who sings in my church's Main Choir and occasionally co-directs the Youth Choir. I have an iPhone and an iPad. Normally I run several automated Claude tasks that need my laptop awake.

Create offline-kit/:
1. BEFORE-GOING-OFFLINE.md: a checklist ordered by how far ahead to do each item. Include: downloading course materials and readings, setting files and maps to offline, email auto-reply text, pausing automated tasks that would fail without the laptop, telling instructors, choir and youth leaders, and who covers what while I'm away.
2. HANDOFF-TEMPLATES.md: fill-in handoff sheets for choir (rehearsal plan, songs in progress) and youth group (upcoming events, open items).
3. CONTACTS-TEMPLATE.md: a blank contacts sheet to print and fill by hand. Do not put real personal data in it.
4. PSU-OFFLINE-INFO.md: phone numbers and in-person locations for the PSU offices a student might need (registrar, financial aid, civil engineering department, advising, IT help). Open the pages you cite; give each number its link and the date checked.
5. KIT.pdf, printable, combining the one-pagers from this repo: career/pitch practice sheet, the FE roadmap summary, the choir binder's rehearsal template and warm-ups, the top 20 games from church/game-bank, and church/youth-reference/OPEN-ITEMS.md. Skip any that don't exist and say so.
6. offline-kit.html: one self-contained file with all of the above, readable on an iPhone or iPad with no internet, loading nothing from outside.
Add short instructions for saving the HTML and PDF on an iPhone and iPad so they open offline.
```

## After Wednesday: going deeper into Claude Code

Once the credit is gone, Claude Code still comes with Pro; it just draws on the same limits as everything else. These are the next steps, easiest first.

- **Keep `vito-workbench` as your home base.** Prompt changes, resumes and church references now have version history. Keep adding to it instead of loose files.
- **Add a CLAUDE.md file to the workbench.** It's a standing note Claude Code reads at the start of every session (who you are, folder layout, your hard rules), so you stop repeating context.
- **Try a local session.** In the desktop app's Code tab, choose **Local** and point it at a folder on your laptop. It works on your files directly, with no uploading.
- **Version your skills.** Put your custom skills in the workbench so they're backed up and their history is tracked, the same way #1 handles prompts.
- **Keep connector work in Cowork.** Gmail, Calendar, Planning Center, Drive, memory and this Project's docs stay easiest here. A good split is to build in Code and place or apply in Cowork.
