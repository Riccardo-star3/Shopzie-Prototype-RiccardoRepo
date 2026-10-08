# What changed — version 14, 8 October 2026

Four things, and one of them is a **correction to something version 13 told buyers**.
That one is first, because it is the only change here that makes the prototype say
something different about how the business works.

Everything here is still placeholder content. **Nothing is a commitment.** The sellers
(Offeibia, Debbies, Nuru, Adom, Akosua, Amina, Marika), the customers, the prices, the
ratings, the nutrition figures and — new in this version — **the written reviews** are all
**invented for the prototype**. No real product, order, seller, review or payment is
involved.

Earlier notes: [version 13](../v13-2026-10-01/WHAT-CHANGED.md) · [version 12](../v12-2026-09-22/WHAT-CHANGED.md) · [version 11](../v11-2026-09-21/WHAT-CHANGED.md)

---

## Sellers now clear three checks, not four

Version 13's impact page told buyers that *"every seller clears these four before a single
listing goes live"*. The fourth was **a reviewed first order** — somebody at Shopziexpress
reading every new seller's first order before a second customer could buy from them.

**It has been removed from both pages, and this is a decision rather than a tidy-up.** The
product requirements do not mention verification anywhere: no four checks, no first-order
review, not the word. All four were written for the impact page to give the verified mark
something to mean. The other three — a company-register lookup, a bank-name match, a
letter posted to the address — are automatic. This one was a person, reading every new
seller's first order, forever, and it is the one that quietly stops happening when nobody
is staffed to do it.

So the prototype now promises a buyer only what the business can actually do. **If the
team intends to staff that review, the honest move is to put it back and say so** — not to
leave a promise standing in the hope that it gets built.

## Become a seller, rebuilt

The page from version 13 was a first pass and said so. This is the finished one: **1120px
wide**, matching every other page; a hero with a photograph; *Why sell here* as four short
panels; **How you get started** as four numbered steps ending in "Your listings go live";
**How and when you are paid** as four steps that **arrive one after another** as you scroll
to them; *What it costs*, still refusing to name a commission because the requirements do
not contain one; and five questions as native expanding panels.

Two things to know about the sequence, because they are the kind of thing that goes wrong
quietly. It **does not run at all** for a visitor whose system asks for less motion. And it
**prints**: the first full-page capture of this page came out with the payment section
completely blank, because a capture never scrolls and the steps had never been asked to
appear. A seller printing the terms they are agreeing to would have got empty space where
the escrow and payout rules are.

## Reviews on the product page

The product page had no written reviews, on purpose: the requirements describe none, and
twelve invented customer voices look completely real in a screenshot. The team's buyer
survey then put **"build trust"** at the top of its list, with unreliable reviews sending
29% of people away.

So there are reviews now, **every word of them invented, and the page says so** on the
heading. What is being **proposed** is the rule above them, which costs almost nothing to
build:

> A review can only be written by someone whose order completed. Shopziexpress holds the
> money until the buyer confirms delivery, or 14 days after tracking shows it arrived — and
> the review opens at that moment and at no other.

That is the escrow release the requirements already describe. Most marketplaces cannot
prove a reviewer bought the thing; this one can, from a record it already keeps. **That
sentence is the part worth agreeing or rejecting.** The prose under it is scaffolding.

## A wishlist that works, and one question asked once

**Save for later.** The heart on a product card and on a product page now keeps it; each
product line in the basket has **Save for later**; and the Wishlist in the header opens a
drawer where you can move something back to the basket or drop it. One list, two doors.
Previously every one of those controls announced itself and did nothing.

**And checkout stops asking where you are.** "Where you are" used to sit in the first step —
drawn twice, once under the sign-in form and once under the six-digit code — two steps
before anything used it. Its only job is deciding which payment methods you can use, and
**a parcel going to Helsinki is a buyer in Finland**, so a product order now takes the
answer from the delivery address and never asks. A booking has no delivery address, so it
asks once, on the payment step, directly above the methods it changes.

---

## Everything that has not changed

The shop, services, checkout and seller dashboard pages are as they were in version 13,
apart from the wishlist controls and the checkout change above. The routes are `#/index`,
`#/shop`, `#/services`, `#/impact`, `#/checkout/product`, `#/checkout/service`, `#/seller`,
`#/product/<product>` and `#/sell`.

## Known gaps, so nobody has to find them

- **A seller has no page of their own.** "Visit the shop" still says what it would do and
  does nothing. The verified mark exists; the profile behind it does not.
- **Nothing anywhere mentions import VAT or customs duty**, and goods ship from Ghana into
  the EU. That is a larger surprise cost than postage and nobody has raised it.
- Side-by-side comparison of saved products is not built.
- Creating a seller account opens the ordinary account dialog — the business registration,
  the bank account and the address confirmed by post are not designed.
- A product has one photograph, and its description is written per category rather than per
  product.
- Messaging has no screen.
