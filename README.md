# Shopziexpress — design prototype

**Open it here: https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/**

That link always points at the current version. Nothing else in this repo needs opening.

> **The link changed on 11 September 2026.** The prototype used to live at
> `dkwafo.github.io/Shopzi-prototype`. This is its current home — please update any
> bookmark. The old repo still holds version 1 and is not being updated.

**What changed in this version: [`prototype/WHAT-CHANGED.md`](prototype/WHAT-CHANGED.md)** — read
that first if you saw the previous one.

## What's in here

| Folder | What it is |
|---|---|
| `prototype/` | **The current prototype.** One file, `index.html`, plus `img/` |
| `archive/` | Superseded versions. [Browse them here](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/) |
| `index.html` | A redirect at the root, so the short link above keeps working |

## The current prototype

**It is a single HTML file.** Six pages switch in place on hash routes — the back button works, every
page is linkable, and the basket survives moving between them.

| Page | Link | What it shows |
|---|---|---|
| Landing | [`#/index`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/index) | Hero carousel with a pause control, twin entry (Shop products / Book a service), the seller band, two teaser rows, trust strip, impact section |
| Shop | [`#/shop`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/shop) | 24 products, a seven-group filter rail that really filters, sort, show-more |
| Services | [`#/services`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/services) | 24 services, 7 facets, and a location search that measures real distance from a Finnish town or from your browser |
| Checkout — product | [`#/checkout/product`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/checkout/product) | Delivery, then payment. Card, PayPal, Klarna in Finland and the EU, Mobile Money in Ghana |
| Checkout — service | [`#/checkout/service`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/checkout/service) | Appointment, then payment. Products and services check out separately — PRD §7.1 |
| Our impact | [`#/impact`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/impact) | The fund arithmetic line by line, four funded projects, four seller-verification checks |
| Your dashboard | [`#/seller`](https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/#/seller) | The seller side: what needs you today, your money, your products and your services |

The top bar, the burger menu and the logo work from every page. "Add to basket" and "Check
availability" open the same basket, and a booked slot sits alongside a product in it.

**Why one file rather than five pages.** The previous version was published as five separate pages
and every link between them was dead — each page lived on its own origin, so clicking "Shop" from
the landing page left the prototype. One document has no way out of itself.

## Before you review

**All content is placeholder.** Prices, seller names, ratings, availability, orders and product
counts are invented so the pages feel real. Fifteen of the 24 shop products still use drawn icons
rather than photographs — a known gap, not a design choice.

**This is a design prototype, not the website.** It exists to settle the visual language and layout.
The product will be built in React and TypeScript — engineering will receive design tokens and
component specifications, not this HTML.

**Give feedback on:** layout, hierarchy, colour, wording, what is missing from a page, and anything
that reads as a promise we cannot keep. The **seller dashboard** especially — it is the newest thing
here and the least reviewed.

**Ignore:** the specific products, prices, names and photographs.

## Two things that need a person, not a designer

**PRD §7.3 contradicts the catalogue.** §7.3 describes service *packages* and a requirements form;
the catalogue and this prototype are built on *appointments* — pick a time, the seller confirms.
Those are different products. The contradiction is in the PRD itself, it is unresolved, and it
changes the service card, the booking panel and the service checkout if it goes the other way. **It
blocks everything on the services side.**

**The delivery and returns wording comes from the PRD**, not from the current live site. Returns are
the seller's own window of 7 to 30 days, the buyer pays return postage unless the item was wrong,
postage is calculated at checkout, and money is released 14 days after tracking shows delivery. The
live site currently promises free shipping and 90-day returns, which the PRD says will not exist. If
the PRD is out of date, now is the time to say so.

## Accessibility

Every colour pairing was **computed before use, not judged after**. WCAG 2.1 AA and EN 301 549, EU
law since 28 June 2025. Nothing below 12px, no tap target below 24 × 24px, focus visible everywhere
including on dark surfaces, reduced motion respected, and every page works at 320px wide with no
sideways scroll. **There is no known contrast exception in this version** — the one version 1 carried
was the copy over the hero video, and there is no video any more.

Try it with the keyboard: Tab reaches a skip link first, the burger and filter drawers trap focus and
return it on Escape, the account menu and language switcher deliberately do not trap because they are
menus rather than dialogs, and the seller's availability calendar is a real date grid you can drive
with the arrow keys.

## Archive

Every version that has been shared with the team, with a note on why each was dropped:
**https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/**

Before replacing the current version, copy the outgoing `prototype/` folder into a dated folder
under `archive/` — for example `archive/2026-08-16/` — and add a row to the top of that page.
The current version always lives at `prototype/`, so the link shared with the team never changes.

Each version also gets a **tag** (Releases, on the right of the repo page), so the whole repo at that
moment can be recovered even if a folder is later tidied away.
