# What changed — version 16, 14 October 2026

One new page, and a handful of repairs to things that had been quietly broken for weeks.

Everything here is still placeholder content. **Nothing is a commitment.** The sellers,
the customers, the prices, the ratings, the nutrition figures and the written reviews are
all **invented for the prototype**.

> **Version 15 was cut earlier the same day and went live in the same push as this one.**
> It was never shared, so if you are catching up, this version contains everything it did.
> Its notes are worth reading on their own: [version 15](../v15-2026-10-14/WHAT-CHANGED.md).

Earlier notes: [version 15](../v15-2026-10-14/WHAT-CHANGED.md) · [version 14](../v14-2026-10-08/WHAT-CHANGED.md) · [version 13](../v13-2026-10-01/WHAT-CHANGED.md)

---

## A wishlist page, where saved products can be compared

The wishlist has been a drawer since 8 October. A drawer is the right place to answer
"did that save?" without losing your place, and it stays. What it cannot do is put two
products beside each other — it is a column about 400px wide, and there is room for one.

The team's survey asked for side-by-side comparison of saved products. So there is now a
page at **Account → Wishlist**, and the drawer has gained **"See all and compare"** at its
foot, in the same place the basket drawer has "Check out products".

### What it compares

Tick up to three saved products and they appear side by side on the eight things the
prototype knows about them: **price, seller, where it is sent from, how long it takes,
the seller's rating, how many ratings, the category, and whether it is in stock.**

**It does not pick a winner, and that is deliberate.** Marking the cheapest would be
wrong twice over: cheapest is not best, and two things you have saved may be a length of
cloth and a jar of shea butter, where comparing prices means nothing at all.

What it does instead is mark the rows where the products **agree**, and offer to hide
them. Two items from the same seller agree on six rows out of eight — the same town, the
same delivery time, the same rating, the same stock — and those six drown the two that
actually differ. The heading says how many match, so you know before you press it whether
hiding will remove one row or six.

**Three at a time**, because by the fourth column you have stopped comparing and started
scanning.

### It tells you it is not keeping anything

The list lives in the browser tab. That did not need saying while it was a drawer — a
drawer reads as "while I am browsing". A page called *Your wishlist* reads as somewhere
things are **kept**, and this product has not built that: there is no account that
remembers a list and nobody has designed one. So the first line under the heading says
the list disappears when the tab closes.

---

## Three repairs, and all three were invisible

### The drawer's "Move to basket" button vanished when you pointed at it

A filled green button with a white label. Hovering it made the green disappear and left
white text on white — an invisible button, on five pages, since the wishlist drawer was
built five weeks ago. It referred to a colour that was removed from the design system on
8 September.

### The wishlist page's breadcrumb came out as a numbered list

"1. Home 2. Your wishlist", with the numbers showing. Caught before release.

### The comparison table could drag the whole page sideways on a phone

The table is meant to scroll on its own at narrow widths, and it does. The page behind it
was also moving about 70px sideways to show nothing at all.

---

## Nothing else moved

No prices, no copy, no layout anywhere else. The eight existing pages are the same as they
were in version 15, apart from the hover colour repair, which they all share.

## Known gaps, so nobody has to find them

- **A seller has no page of their own.** "Visit the shop" still goes nowhere.
- **Messaging has no screen.** The Message button in a booking does nothing — and this is
  the gap that matters most for keeping conversations on the platform.
- **Nothing anywhere mentions import VAT or customs duty**, and goods ship from Ghana into
  the EU.
- **There is still no logo file.** The wordmark is live text; somebody has to draw it as
  an SVG before a social avatar, a favicon or a slide master can be made.
- The seller account steps — business registration, bank account, address confirmed by
  post — are not designed.
- A wishlist is not remembered between visits, as the page itself says.
