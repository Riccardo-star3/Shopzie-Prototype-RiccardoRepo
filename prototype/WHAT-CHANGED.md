# What changed — version 2, 11 September 2026

The previous prototype was **five separate pages** with a full-screen video hero on a light grey
ground. This one is **one file with six routes** on a white ground with a green palette. Almost
nothing carried over, so this is a description of what is here rather than a list of edits.

Everything below is placeholder content — prices, names, ratings, orders and figures are invented so
the pages feel real. **Nothing here is a commitment.**

---

## The one thing to know before you open it

**It is a single HTML file.** The six pages switch in place on hash routes: `#/index`, `#/shop`,
`#/services`, `#/impact`, `#/checkout/product`, `#/checkout/service`, `#/seller`. Your browser's back
button works, every page is linkable, and the basket survives moving between them.

It is one file because the previous version was published as five separate pages and **every link
between them was dead**. Each published page lived on its own origin, so clicking "Shop" from the
landing page left the prototype entirely. One document has no way out of itself.

---

## What is new since version 1

### The palette is green, not yellow — and not grey

`#FED415` was removed completely. The ground is white with hairline cards. Every colour pairing in
the prototype was measured against WCAG 2.1 AA before it was used, not after.

| Token | Value | Where |
|---|---|---|
| `--deep` | `#0B3D2B` | headings, dark surfaces, focus ring, and the far end of every ladder |
| `--action` | `#14704F` | filled primary buttons, white label — hover goes to `--deep` |
| `--green` | `#1B7F47` | fills only: search button, seller mark, stars, chart bars |
| `--green-d` | `#146237` | green **text** |

There is no video hero. The accessibility exception version 1 carried — copy over the bright parts
of the clip falling below the contrast floor — no longer exists, because the clip no longer exists.

### Six routes, not five pages

| Route | What it shows |
|---|---|
| `#/index` | Landing. Five-slide hero carousel with a working pause control, then **twin entry** — two equal cards, Shop products and Book a service — the become-a-seller band, two teaser rows, trust strip, SEO block, impact section, footer, help assistant. |
| `#/shop` | 24 products, a seven-group filter rail that **really filters**, sort, cross-sell band, show-more. Below 900px the rail becomes a focus-trapping drawer. |
| `#/services` | 24 services, 7 facets, and a **location search** — a hand-built combobox offering five Finnish towns that then measures real distance from that town or from the browser's geolocation. |
| `#/checkout/product` and `#/checkout/service` | Products and services check out **separately** (PRD §7.1), so one order never holds both. When the basket holds both kinds, a switcher at the top moves between the two orders. Delivery step for goods, appointment step for bookings, payment last. |
| `#/impact` | The fund arithmetic line by line, four funded projects that add up to the fund exactly, four seller-verification checks. Figures are marked illustrative. |
| `#/seller` | **New in this version — see below.** |

### The seller dashboard is new

Built to the user journey diagram, and the largest single addition. One seller, Akosua, who sells
printed wax fabric **and** braids hair — the dual seller is the thing that makes this neither Amazon
nor Fiverr, and until this version it was invisible because she existed as two different names in
two different catalogues.

Three sections behind one tab strip, **only one open at a time**, because the first draft put
everything on one scroll and it was a wall:

- **Overview** — "Needs you today" first, as four rows, each saying *what happens if you leave it*.
  Then the money: a six-month income chart, with the figure in a caption underneath rather than as a
  large number. Work above money, deliberately.
- **Products** and **Services** — three large **stage tiles** (to send / on the way / delivered, and
  to confirm / this week / finished) that are colour-coded and **filter the list below them**. Then
  the orders, each carrying its product photograph or service icon; a green band holding the Add
  button; then the listings.
- **Add a product / Add a service** opens one dialog that changes shape by kind, with a real
  availability calendar (arrow keys, Home/End, PageUp/PageDown) and uneven time ranges — a seller
  can say they are free from 10:25, not only on the hour.

**Controls that are not built say what they would do** rather than doing nothing. "Open" on an order
says *"Opens the full order: the buyer, the address, and what happens next. Not built yet."* That is
deliberate: a button that does nothing reads as broken, and one that pretends to work is worse.

### The basket crosses the whole prototype

"Add to basket" and "Check availability" open the same basket. A booked slot joins a product in it,
so the marketplace reads as one place — but the footer offers **one checkout per kind**, because
§7.1 settles them separately. Both panels trap focus.

---

## What we would like feedback on

- Layout, hierarchy, colour, wording.
- What is **missing** from a page.
- Anything that reads as a promise we cannot keep.
- The seller dashboard especially: it is the newest thing here and the least reviewed.

## What to ignore

The specific products, prices, names and photographs. Fifteen of the 24 shop products still use
drawn icons rather than photographs; that is a known gap, not a design choice.

---

## Two questions that need a person, not a designer

**PRD §7.3 contradicts the catalogue.** §7.3 describes service *packages* and a requirements form.
The catalogue and this prototype are built on *appointments* — pick a time, the seller confirms.
These are different products. The contradiction is in the PRD itself and it is unresolved; it
changes the service card, the booking panel and the service checkout if it goes the other way. **It
blocks everything on the services side.**

**Delivery and returns wording comes from the PRD, not the live site.** Returns are the seller's own
window of 7 to 30 days, the buyer pays return postage unless the item was wrong, postage is
calculated at checkout, and money is released 14 days after tracking shows delivery. The live site
currently promises free shipping and 90-day returns, which the PRD says will not exist. If the PRD
is out of date, now is the time to say so.

---

## Accessibility

WCAG 2.1 AA and EN 301 549, which has been EU law since 28 June 2025. Nothing below 12px, no tap
target below 24 × 24px, focus visible everywhere including on dark surfaces, `prefers-reduced-motion`
respected, and every page works at 320px wide with no sideways scroll.

Worth trying with the keyboard: Tab reaches a skip link first; the burger and filter drawers trap
focus and return it on Escape; the account menu and language switcher deliberately do **not** trap,
because they are menus rather than dialogs; the seller's availability calendar is a real date grid
you can drive with the arrow keys.

Every colour pairing in this version was computed rather than judged. There is no known contrast
exception in this version.

---

## This is a design prototype, not the website

It exists to settle the visual language and the layout. The product will be built in React and
TypeScript — engineering will receive design tokens and component specifications, not this HTML.
