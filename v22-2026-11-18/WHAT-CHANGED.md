# Version 22 — the phone works when it is opened on a desktop

Published 18 November 2026.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v22-2026-11-18/mobile/` |
| Desktop | `/v22-2026-11-18/` |

Two things in this release. The phone version no longer looks broken when
somebody opens the link on a laptop — which is how most of the team will open
it. And the desktop hero now carries service campaigns as well as product
ones, which the phone reads at build time to fill its own Services carousel.

## 1. The phone build, opened on a desktop

The phone version is drawn as a device mock above a certain width: a 390px
frame with a bezel, sitting on a grey ground. That mock was broken in three
separate ways, none of them visible on an actual phone, which is why none had
been caught. All three were in version 21 as published.

**The page scrolled sideways.** The navigation drawer and the filter sheet are
kept inside the frame by switching them to absolute positioning. Absolute
positions against the nearest positioned ancestor — and the drawer was being
written into the page *beside* the frame rather than *inside* it, so it
positioned against the browser window instead. The closed drawer parked 300px
off the right edge of the window and dragged the whole page sideways with it;
the dimming shade covered the browser rather than the phone. They are now
written inside the frame. On a real phone these are fixed to the viewport, so
nothing there changed.

**The phone was taller than the window.** The frame was a fixed 844px against
a laptop viewport of roughly 780, so its foot hung off the bottom of the
screen and you had to scroll the page to see the tab bar — on something meant
to look like a phone lying on a desk. The frame is now sized to the window,
down to a floor of 560px. Checked at six window sizes from 1280×720 to
1920×1080: the whole phone fits, with no page scrolling.

**A half-width window got a bare column.** The mock only started at 760px
wide, so between 560 and 759 the build was a 390px column floating on white
with no bezel and no caption — which reads as broken rather than as a phone,
and a shared link is very often opened in a half-width window beside Slack.
The mock now starts at 560px. Phones in portrait top out around 480px, so
nothing real falls below that line.

**And the Products/Services switch now moves in the mock.** Its slide-away
animation read the browser window's scroll position, but inside the mock the
content scrolls within the frame, so on a laptop the switch simply sat there.
It now reads whichever element is actually scrolling.

Checked at twelve window widths from 320 to 1920 in both builds: no sideways
scrolling anywhere, the frame and bezel correct, the drawer and the filter
sheet inside the frame, the switch hiding and returning, and no console
errors.

## 2. Service campaigns, on both prototypes

The desktop landing page's hero carousel now runs **ten slides, not five** —
five product campaigns and five service ones, each tagged with which it is.
The five new ones are cleaning, trades, garden, beauty and lessons, with
photographs made for them.

The phone reads that hero at build time, as it has since version 21, and now
**filters it by the side of the switch you are on**: Products shows the five
product campaigns, Services shows the five service ones. So the phone gets a
dedicated carousel per side without a second set of campaign copy existing
anywhere. Change a campaign on the desktop and the phone changes with it. The
build refuses to ship if either side comes back empty.

This was the first piece of work to go through the desktop-first rule agreed
on 12 November: anything genuinely new is built on the desktop and then
adapted to the phone, never the other way round.

## Housekeeping

The three comparison builds left over from choosing the switch —
`md-web-switch2`, `md-web-sticky`, `md-web-slide-grey` — are gone, along with
the flags and the code paths that produced them. Version 21 still has them if
anyone wants to look.

## What has not changed

The catalogue is the same 24 goods and 24 services. Nothing is really ordered,
and every screen that could be mistaken for a real offer says so. Prices,
discounts and campaign copy are placeholders.
