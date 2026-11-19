# Version 25 — the help assistant has a way out

Published 19 November 2026, shortly after version 24.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v25-2026-11-19/mobile/` |
| Desktop | `/v25-2026-11-19/` |
| Booking previews — agreed, not built | `/v25-2026-11-19/preview/` |

**One fix, and it only showed up on a desktop.** The desktop is unchanged from
version 24.

## The assistant covered the whole frame with no visible way out

Version 24 added the help assistant as a sheet that rises from the foot of the
screen. On a phone it behaved correctly. Opened on a laptop — where the phone
is drawn as a device sitting on a desk — the sheet came out **taller than the
frame it lives in**, so it started above the frame's top edge and the frame
clipped the top off. The header went with it, and the header is where the
close button and the drag handle live.

What was left was a conversation filling the whole frame, with no header, no
close button, and no strip of dimmed page to tap. There was no way out except
the Escape key.

The sheet is now measured against the phone frame rather than the browser
window, so it always sits inside it with the header showing and a strip of the
dimmed page above it.

## And more than one way out

The close button existed in version 24; it was simply clipped. But one small
target in a top corner is a thin promise on a sheet that covers the screen, so
there are now five ways to dismiss it:

- the close button
- the Escape key
- tapping the dimmed page above the sheet
- tapping the handle at the top of the sheet
- **pulling the handle down**, the way a sheet with a handle invites

A short tug counts as a tap and closes it; a longer pull that stops short snaps
back, so the sheet is never left half open.

The filter sheet was measured the same way and had the same latent fault. It
was saved by being shorter than its own limit, but it is fixed here too rather
than left to surface later.

## What has not changed

Everything else is version 24: the assistant itself, reviews on the product
screen, the seller pitch, and the pinned buttons. The same 24 goods and 24
services. Nothing is really ordered, the assistant answers nothing, and every
screen that could be mistaken for a real offer says so.
