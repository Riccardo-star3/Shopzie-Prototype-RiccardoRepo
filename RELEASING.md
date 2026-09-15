# Publishing a new version

The rule this repository exists to keep: **a link shared with the team keeps working forever.**
Everything below serves that one sentence.

## The three rules

1. **Every version gets its own folder**, named `vN-YYYY-MM-DD` — the version number and the
   date it was published. That folder's URL is its permanent link.
2. **A published folder is never edited again.** Not for a typo, not for a broken image, not for
   an accessibility fix. Corrections go into the *next* version. The moment an old folder is
   edited, a link someone shared stops showing what they shared.
3. **Only `index.html` at the root changes.** It gains a row per release. The rows already on it
   stay exactly as they are.

## When to cut one

**At the end of a block of work, not after every change.** A session usually covers several
tasks. Each release costs a folder, a row on the index, a tag and a message to the team, so
publishing per change spends all of that for nothing and hands the team a stream of links
nobody asked for.

Work is still written to the Mac after every finished piece — that is separate, and it is not
optional. But the repo stays untouched until the work is done.

## Steps

Say the new version is 7 and today is 25 October 2026.

**1. Create the folder.** Copy the finished build into `v7-2026-10-25/`. It needs everything the
version requires to stand alone: `index.html`, `img/`, and a `WHAT-CHANGED.md` describing what is
new. Never a symlink, never a shared `img/` folder at the root — a shared folder means changing
an image silently changes every old version too.

**2. Add a row to the root `index.html`.** Two places:

- The **Current** panel near the top: version number, date, and two or three sentences on what
  changed. Move the previous current version down into the list.
- The **wordmark link** at the very top of the page (`<a href="v6-…/">Shopziexpress</a>`). It
  points at the current version, so it moves every release. Missed on the first release after
  this file was written, which is why it is called out separately rather than left to "update
  the Current panel".
- The top of the `<ol class="list">`: a new `<li class="item">` copied from the one below it,
  with the version, date, short description and both links updated.

Do not touch any row below the one being added.

**3. Update `README.md`.** The two links at the top, the version table, and the route table if
the routes changed.

**4. Check before pushing.** Open the root page and click through every link, including the old
ones. A release that quietly breaks version 4 is worse than a late release.

**5. Commit and push** from GitHub Desktop. Summary line: `Version 7 — <short description>`.

**6. Tag it.** On GitHub: Releases → Draft a new release → tag `v7` → publish. A folder can be
tidied away by accident; a tag cannot.

**7. Send the team the version link**, not the root link, unless you specifically want them to
see whichever is newest.

## What not to do

- **Don't reuse a folder name.** If a version is published and then found to be broken, the fix
  is version 8, not a quiet edit to version 7.
- **Don't delete an old version** to save space. The whole repository is a few tens of megabytes
  and the point of it is that nothing disappears.
- **Don't put the newest version at the root.** That is the mistake this scheme replaced: the
  root link moved every time, so a link shared in September showed something different in
  October.
- **Don't share the root link when you mean a specific version.** The root is the index; it
  changes by design.

## Where the source lives

The prototype is built in `Documents/Shopzie - White UI/` on Riccardo's Mac — `design/` holds the
pages, `scripts/` builds them, `build/` holds the seller dashboard parts. This repository holds
**published output only**. Nothing here should be edited by hand except `index.html`,
`README.md` and this file.
