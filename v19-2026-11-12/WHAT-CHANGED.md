# Version 19 — the phone version

Published 12 November 2026.

## What is new

**There are two prototypes in this folder, and they are different products.**

| | Link | What it is |
|---|---|---|
| Desktop | `/v19-2026-11-12/` | The nine-page prototype, unchanged in design since v18. It now also works properly on a phone — see below. |
| **Phone** | **`/v19-2026-11-12/mobile/`** | **A separate design, built for a phone.** Open this one on an actual phone. |

### The phone version

A different design, not the desktop made narrow. The team asked for "a mobile
version", meaning the website seen on a phone, and three things follow from
that:

- **The home screen is a shop, not a brochure.** The first product is visible
  without scrolling, after fifteen words. The desktop home screen puts the
  first product 1,688 pixels down — two full screens — after a hundred and
  twenty words. That difference is the whole point of the redesign.
- **A card carries four things**: photograph, title, price, one line of meta.
  The photograph is 69% of the card's height and the price is the loudest text
  on it.
- **There is no bottom tab bar**, because this is a website and that strip is
  where the browser's own chrome lives — Safari's address bar slides in and out
  over exactly it. The five destinations sit behind the burger in the top
  right, with the basket left out in the open beside it.

**What you can actually do in it:** the kente fabric and the home-cleaning
service are both clickable. Open the product, add it to the basket. Open the
service, pick a day and a time, add the booking. The basket keeps goods and
bookings in separate sections with separate totals, because they are checked
out separately. Everything else is there to show how it looks.

### The desktop version, on a phone

Unchanged in design, but it was only *unbroken* at phone width before, not
usable. Four measured faults fixed, all through one shared stylesheet:

- the header took 192px — a quarter of the screen — and now takes 117px;
- the shop page ran to 7,707px of scrolling and now runs to 3,688px, two
  products across instead of one;
- the help button sat on top of the content;
- seventeen card title links were under the 24px tap-target floor.

**The desktop rendering did not move.** All nine routes were screenshotted from
the published v18 build and from this one at 1440px and 1024px and compared
pixel for pixel: eighteen of eighteen identical.

## Checked before publishing

- Twelve pages, **20 of 20 static checks on every one**.
- The phone version: 35 distinct colour pairings measured on the rendered page,
  **zero below the 4.5:1 floor**, tightest 5.63:1. Smallest type 12px. **No tap
  target under 44px.** No sideways scroll at 390px or 320px.
- Both flows driven in a real browser — product to basket, service to booking —
  with the basket count verified after each.

## Known, and deliberate

- **It is a prototype.** Sellers, prices, ratings and appointment times are
  placeholder content, not real offers. The home screen says so at the bottom.
- **Four screens only** in the phone version: home, product, booking, basket.
  Orders and Account open a panel that says they are not built.
- **The phone version uses a different typeface** (Hanken Grotesk) from the
  desktop (Manrope). That is a decision still to be made, not an accident — see
  the handover. It is loaded from Google Fonts, which for a Finland-facing
  product should become a self-hosted file before launch.

## The QR code

`qr-mobile.png` in this folder points at `/v19-2026-11-12/mobile/`. It was
decoded back and checked against the intended URL before publishing.
