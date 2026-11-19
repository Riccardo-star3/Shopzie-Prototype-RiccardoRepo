# Version 23 — the service booking screen gets a calendar

Published 19 November 2026.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v23-2026-11-19/mobile/` |
| Desktop | `/v23-2026-11-19/` |
| Previews, for the booking screen we have not built yet | `/v23-2026-11-19/preview/` |

The desktop is unchanged from version 22. **Everything below is the phone.**

## 1. The day strip is gone. There is a month calendar

Version 22 shipped a bug on the service booking screen: the day cards stacked
vertically down the page and the time slots wrapped seven across. The markup
said `class="days"` and `class="times"` while the stylesheet said `.md-days`
and `.md-times`, so neither container was styled at all. **If you looked at
services in v22, that is what you saw. This is the fix.**

In its place, a proper month calendar: the month name with back and forward
arrows, a Mo–Su header row, a seven-column grid, the chosen day as a solid
tile, open days in bold with a green dot, closed days light, and a Clear link.
Below it, a time wheel carrying **only bookable times** — the old grid struck
out the unavailable ones and spent a third of the screen saying no.

The selected time in the wheel was invisible when this was first built: the
highlight band is absolutely positioned and the wheel was not, so the band
painted over the text. Everything measurable said it was correct. Only a
screenshot found it.

## 2. Three classes that had never done anything

Live since version 20, in both phone builds:

- The meta line under every product card — *"Accra · 8 days"* — carried
  `class="pm"` while the rule was written `.md-pm`. It rendered near-black at
  default size instead of 13px grey with the days in green.
- **Check out the goods**, **Check out the bookings** and **Apply to sell**
  carried `class="cta block"`, and no `.block` rule has ever existed in this
  stylesheet. The buttons were 185px wide in a 390px screen instead of full
  width.
- The footer bar was built as `class="foot"` while its rule was written
  `.md-foot`, so the footer's own styling — the hairline, the white ground and
  the safe-area inset — had never applied to anything. **On a real phone the
  Add to basket button sat under the home indicator.** This one is the reason
  the button now clears the bottom edge properly rather than by luck.

Both fixed. A new check, `scripts/unstyled.mjs`, walks every screen in both
builds and asks the browser whether any rule matches each class that actually
renders — the only way to catch this family of bug, since the classes are built
at run time and no search of the source can see them.

## 3. Previews, not product

`/preview/` holds two pages for a decision the team has taken but nobody has
built yet. **Nothing in them is live.**

`service-options.html` compared two ways to stop the photograph pushing the
calendar down the page. Option 2 was chosen: the photograph shrinks to a small
round picture beside the title and nothing moves.

`service-booking.html` carries Option 2 with four agreed additions — the
photograph opening full size with a tap anywhere to close it, choosing several
days at once, choosing a start time and then a length rather than two times,
and the reviews moved onto the service screen. Try them; they respond.

**The product has none of this yet.** It is the next piece of work, and it
starts on the desktop: the seller's "Add a service" dialog already has a
multi-day calendar and From/To time ranges, and the buyer's screen should
borrow that vocabulary rather than invent its own.

## What has not changed

The same 24 goods and 24 services. Nothing is really ordered, and every screen
that could be mistaken for a real offer says so. Prices, discounts, campaign
copy, availability and reviews are placeholders.
