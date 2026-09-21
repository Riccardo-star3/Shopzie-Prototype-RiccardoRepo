# Shopziexpress — design prototype

**All versions: https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/**

**Current version (10), published 21 September 2026:**
https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v10-2026-09-21/

## How the links work

**Every version has its own permanent link, and that link never changes.** A version, once
published, is never edited again. Corrections go into the next version rather than backwards
into an old one. So a link sent to the team today shows exactly the same thing in a year, and a
decision can be traced back to what people were actually looking at when they made it.

| Share this | When |
|---|---|
| A **version link** (`…/v10-2026-09-21/`) | You want someone to look at a specific version. Safe to bookmark, quote in a document, or paste into a ticket. |
| The **index link** (the root, above) | You want someone to find whichever version is current. This is the one page that changes. |

| Version | Published | Link |
|---|---|---|
| 10 — the seller dashboard, in panels | 21 Sep 2026 | [`/v10-2026-09-21/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v10-2026-09-21/) |
| 9 — signing in, by email or by phone number | 15 Sep 2026 | [`/v9-2026-09-15/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v9-2026-09-15/) |
| 8 — the checkout takes one step at a time | 15 Sep 2026 | [`/v8-2026-09-15/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v8-2026-09-15/) |
| 7 — a seller can name her own category | 15 Sep 2026 | [`/v7-2026-09-15/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v7-2026-09-15/) |
| 6 — one file, six routes, seller dashboard | 11 Sep 2026 | [`/v6-2026-09-11/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/v6-2026-09-11/) |
| 5 — video hero, light grey, five pages | Aug 2026 | [`/archive/2026-09-11/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/2026-09-11/) |
| 4 — framed build, deep-green hero | 16 Aug 2026 | [`/archive/2026-08-16/`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/2026-08-16/) |
| 3 — retail marketplace layout | Jul 2026 | [`/archive/v3.html`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/v3.html) |
| 2 — warm artisan direction | Jul 2026 | [`/archive/v2.html`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/v2.html) |
| 1 — first prototype, built in Lovable | Jun 2026 | No longer online |

Publishing the next version: see [`RELEASING.md`](RELEASING.md).

## The current version

**It is a single HTML file.** Seven routes switch in place on hash routes — the back button
works, every page is linkable, and the basket survives moving between them.

| Page | Route | What it shows |
|---|---|---|
| Landing | `#/index` | Hero carousel with a pause control, twin entry (Shop products / Book a service), the seller band, two teaser rows, trust strip, impact section |
| Shop | `#/shop` | 24 products, a seven-group filter rail that really filters, sort, show-more |
| Services | `#/services` | 24 services, 7 facets, and a location search that measures real distance from a Finnish town or from your browser |
| Checkout — product | `#/checkout/product` | Delivery, then payment. Card, PayPal, Klarna in Finland and the EU, Mobile Money in Ghana |
| Checkout — service | `#/checkout/service` | Appointment, then payment. Products and services check out separately — PRD §7.1 |
| Our impact | `#/impact` | The fund arithmetic line by line, four funded projects, four seller-verification checks |
| Your dashboard | `#/seller` | The seller side, in panels: what needs you today, your money, then orders and listings with status filters and Show more |

**What changed in this version:**
[`v10-2026-09-21/WHAT-CHANGED.md`](v10-2026-09-21/WHAT-CHANGED.md) — read that first if you saw
the previous one.

**Why one file rather than five pages.** Version 5 was published as five separate pages and
every link between them was dead: each page lived on its own origin, so clicking "Shop" from the
landing page left the prototype. One document has no way out of itself.

## Before you review

**All content is placeholder.** Prices, seller names, ratings, availability, orders and product
counts are invented so the pages feel real. Fifteen of the 24 shop products still use drawn icons
rather than photographs — a known gap, not a design choice.

**This is a design prototype, not the website.** It exists to settle the visual language and
layout. The product will be built in React and TypeScript — engineering will receive design
tokens and component specifications, not this HTML.

**Give feedback on:** layout, hierarchy, colour, wording, what is missing from a page, and
anything that reads as a promise we cannot keep. The **seller dashboard** especially: it is the
newest thing here and the least reviewed.

**Ignore:** the specific products, prices, names and photographs.

## Two things that need a person, not a designer

**PRD §7.3 contradicts the catalogue.** §7.3 describes service *packages* and a requirements
form; the catalogue and this prototype are built on *appointments* — pick a time, the seller
confirms. Those are different products. The contradiction is in the PRD itself, it is unresolved,
and it changes the service card, the booking panel and the service checkout if it goes the other
way. **It blocks everything on the services side.**

**The delivery and returns wording comes from the PRD**, not from the current live site. Returns
are the seller's own window of 7 to 30 days, the buyer pays return postage unless the item was
wrong, postage is calculated at checkout, and money is released 14 days after tracking shows
delivery. The live site currently promises free shipping and 90-day returns, which the PRD says
will not exist. If the PRD is out of date, now is the time to say so.

## Accessibility

Every colour pairing was **computed before use, not judged after**. WCAG 2.1 AA and EN 301 549,
EU law since 28 June 2025. Nothing below 12px, no tap target below 24 × 24px, focus visible
everywhere including on dark surfaces, reduced motion respected, and every page works at 320px
wide with no sideways scroll. **There is no known contrast exception in the current version.**

Try it with the keyboard: Tab reaches a skip link first, the burger and filter drawers trap focus
and return it on Escape, the account menu and language switcher deliberately do not trap because
they are menus rather than dialogs, and the seller's availability calendar is a real date grid
you can drive with the arrow keys.

Older versions are frozen and have **not** had any of these fixes applied.

## A note on `prototype/`

`prototype/` is left over from the previous scheme, where one folder always held the newest
version. It currently holds the same files as `v6-2026-09-11/`. It is kept so that any link
already shared still resolves, but **it will not be updated again** — do not link to it. Version
links are the ones to share.

## History

The repository moved here on 11 September 2026 from `Dkwafo/Shopzi-prototype`, which is no
longer updated. Versions 1 to 5 were published from there.
