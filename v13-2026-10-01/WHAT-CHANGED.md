# What changed — version 13, 1 October 2026

Three things, and the first is the one a buyer would notice: **the product detail page exists.**
Until now a product card's title was a link to nothing, so the journey ran card → basket →
checkout and the screen where a person decides whether to buy something had never been designed.

Everything here is still placeholder content. **Nothing is a commitment.** The sellers
(Offeibia, Debbies, Nuru, Adom, Akosua, Amina, Marika), the customers in the seller dashboard,
the prices, the ratings and the nutrition figures are all **invented for the prototype**. No real
product, order, seller or payment is involved.

Earlier notes: [version 12](../v12-2026-09-22/WHAT-CHANGED.md) · [version 11](../v11-2026-09-21/WHAT-CHANGED.md) · [version 10](../v10-2026-09-21/WHAT-CHANGED.md)

---

## The product detail page

Click any product title, anywhere. The page shows the photograph, the price with VAT, the seller
with their verified mark and rating, when it arrives and from where, the return window, a
quantity stepper, Add to basket and a wishlist button — then the description and specifics, the
seller, the ratings, and more from the same seller.

**Every promise in the buy box is a rule from the product requirements rather than a nice
sentence.** You pay Shopziexpress and we hold the money; the seller is paid when you confirm the
item arrived, or automatically 14 days after tracking says it was delivered; if tracking has not
moved in 21 days you get all of it back; damaged or not as described means it goes back and is
refunded once the seller has it.

Its facts are read out of the shop page's own catalogue when the page is built, so a price can
never be right in one place and wrong in the other.

**Two things it deliberately does not do.**

- **There are no written reviews.** The requirements do not describe reviews, so none have been
  invented. The section shows the rating the cards already carry as a spread, and says in as many
  words that the spread is illustrative and that written reviews are not designed yet.
- **The return window reads 14 days**, not the 7 the requirements allow a seller to set. Seven
  days is below the EU right of withdrawal for distance selling, which cannot be shortened. A
  prototype should not show a number that would be unlawful on the day it shipped. **This one is
  still for the team to settle.**

## Food information, for the eight products that need it

Food sold online in the EU has to show the ingredients, the allergens, the net quantity, the
storage, who is responsible for it and the nutrition declaration **before** the buyer pays — not
on the packet when it arrives. "Food & groceries" is the biggest category in the catalogue.

So a food product now has a **Food information** section: ingredients with the allergens
emphasised inside the list, a Contains line that turns red when there is something to declare,
and the nutrition table per 100 g or 100 ml.

**The figures are placeholders and the page says so, in a panel above them.** They belong to a
particular batch of a particular product and in a real shop they would come from the seller. What
is real is which fields appear and in what order.

Two questions this raises are not on the page: the data has to reach it through a **seller
listing form that has not been specified**, and when food is marketed from Ghana into Finland,
**who the responsible operator is** needs an answer from someone who knows EU food law. The page
names the seller and says plainly that an EU importer has to be named too.

## Become a seller

"Join now" on the landing page used to lead nowhere. So did "Learn more" beside it, and the
footer's "Become a seller" on seven of the eight pages. All three now open a real page: why sell
here, the four checks every seller clears before a first listing goes live, and how and when you
are paid — the two different escrow releases for products and for services, payouts every Friday
for orders completed by Wednesday midnight, the €10 minimum that rolls over, SEPA in the EU and
local bank in Ghana.

**What it costs is the section that says the least on purpose.** Listing is free and there is no
monthly charge; beyond that, the commission is not in the requirements, and the six per cent used
in the impact page's arithmetic is an illustrative figure that page labels as one. Rather than
invent a rate on a page headed *What it costs*, it says the commission, the payment-processing
fee and whether services are charged like products are all still open.

The four verification checks are the same four the impact page lists — they are taken from it
when the page is built, not typed again, so the two can never disagree.

## The type is finished

Version 12 was built on five font weights and twenty-three sizes, most of which nobody had
chosen: 14.5px against 14px, 13.5px against 13px, 12.5px against both. Eighty-two of those
declarations spent half a pixel on a difference no reader can see.

It is now **three weights** — one for reading, one for labelling, one for headings and money —
and **eight sizes**, the scale the developers were given in September. The change is meant to be
quiet. Nothing has moved or been redesigned; what has gone is the noise.

One part of it is a fix rather than a tidy-up: **form fields are now large enough that iPhones
stop zooming the page** when you tap into one.

---

## Everything that has not changed

The shop, services, impact, checkout and seller dashboard pages are as they were in version 12,
except for the type. The eight routes are `#/index`, `#/shop`, `#/services`, `#/impact`,
`#/checkout/product`, `#/checkout/service`, `#/seller`, `#/product/<product>` and `#/sell`.

## Known gaps, so nobody has to find them

- **The Become a seller page needs more work.** It is a first pass.
- Creating a seller account opens the ordinary account dialog — the business registration, the
  bank account and the address confirmed by post are not designed.
- A product has one photograph, and its description is written per category rather than per
  product.
- "Visit the shop", "Ask a question" and the wishlist say what they would do and do nothing.
- Messaging has no screen, and the first checkout step still asks you to sign in when the header
  already says you are.
