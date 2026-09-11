# Shopziexpress — design prototype

**Live:** https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/

Four linked pages showing the current design direction. Click through them — the
top bar, the burger menu, "Shop now" and every product card all navigate.

| Page | File | What it shows |
|---|---|---|
| Landing | `index.html` | Hero, the two doors, categories, flash sale, impact band |
| Shop | `shop.html` | Product listing with filters, sorting and an empty state |
| Services | `services.html` | Service listing with location, availability and packages |
| Product | `product.html` | Product detail: gallery, buy box, reviews, delivery terms |

## Please read before reviewing

**All content is placeholder.** Prices, seller names, ratings, availability and
product counts are invented to make the pages feel real. The only genuine
photograph is the hero image (Esha Verma, via Unsplash); everything else is a
coloured placeholder standing in for seller photography.

**This is a design prototype, not the website.** It exists to settle the visual
language and layout. The product will be built in React and TypeScript —
engineering will receive design tokens and component specifications, not this HTML.

**What to give feedback on:** layout, hierarchy, colour, wording, what is missing
from a page, and anything that reads as a promise we cannot keep.

**What to ignore:** the specific products, prices, names and photographs.

## Things worth knowing while you review

- **The delivery and returns wording on the product page comes from the PRD**, not
  from the current live site. Returns are the seller's own window of 7 to 30 days,
  the buyer pays return postage unless the item was wrong, postage is calculated at
  checkout, and money is released 14 days after tracking shows delivery. The live
  site currently promises free shipping and 90-day returns, which the PRD says will
  not exist. If the PRD is out of date, that is worth saying now.
- **Products and services check out separately** (PRD §7.1), so the product page
  says so rather than implying one basket.
- **Every colour was measured against WCAG 2.1 AA before use.** The European
  Accessibility Act has applied to EU e-commerce since June 2025.
- Try the page **with the keyboard**: Tab reaches a skip link first, the burger menu
  traps focus and closes on Escape, and every control has a visible focus ring.

## Design foundations

Palette, typography and radius are documented in `design-foundations.html`, kept
with the design files rather than in this repo, along with `DESIGN.md` — the
binding accessibility and quality rules for the project.

## Earlier versions

Every version shared with the team, with the reason each was dropped:
https://riccardo-star3.github.io/Shopzie-Prototype-RiccardoRepo/archive/
