# What changed — version 17, 15 October 2026

One screen, rebuilt after a review. Nothing else in the prototype moved.

Everything here is still placeholder content. **Nothing is a commitment.** The sellers,
the customers, the prices, the ratings and the written reviews are all **invented for the
prototype**.

Earlier notes: [version 16](../v16-2026-10-14/WHAT-CHANGED.md) · [version 15](../v15-2026-10-14/WHAT-CHANGED.md) · [version 14](../v14-2026-10-08/WHAT-CHANGED.md)

---

## The wishlist comparison now works the way you would expect it to

Version 16 added a page where saved products could be compared side by side. It opened
with an **empty** panel and asked you to tick two boxes before it would show you anything
— so the first screen of a page called "compare" compared nothing, the tick box that would
have fixed that was easy to miss, and ticking it redrew the panel **above** where you were
looking, so the page jumped and you had to scroll back up.

All three were the same mistake: the comparison was being treated as something you
assemble, rather than as the thing the page is.

### It arrives with the comparison already in it

Open the page and the first three saved products are already side by side. Nothing to find,
nothing to assemble.

### Changing what is compared happens underneath

The saved products sit **below** the comparison now, so choosing never pushes what you are
reading off the top of the screen. Each card carries a real button — **Add to the
comparison**, or **Being compared** when it is already in — with a green outline and a
check in the corner, instead of a small tick box in a row of other controls.

**Press a fourth and it swaps.** Whichever product has been in the comparison longest steps
out to make room, and the page says which. Previously the other cards simply switched off,
which meant working out for yourself that you had to remove one first.

**Remove something and the next saved product takes its place**, so the comparison stays
full rather than collapsing back to an empty frame.

### It reads like a comparison instead of a spreadsheet

The row labels down the left were grey text that blended into the values beside them. They
are now a shaded column with an icon on every row, and they stay put while the products
scroll sideways on a narrow screen.

Each row shows its fact rather than just stating it: the price large with the old price
struck through and **what you save**, the seller's own colour, a pin on where it ships
from, **delivery as a bar**, the rating as **stars**, the category as its icon, and stock
as a green or amber badge.

### Rows where everything agrees are marked

Two products from the same seller agree on six rows out of eight, and those six drown the
two that actually differ. Matching rows are shaded and tagged **same**, the heading says
which ones they are, and **Hide rows that match** clears them away so only the differences
are left.

### What it still will not do

**It does not tell you which product is better.** Cheapest is not best, and two things you
have saved may be a length of cloth and a jar of shea butter, where comparing prices means
nothing at all. The delivery bar shows how long something takes on a fixed scale — it is a
length, not a verdict.

---

## Known gaps, so nobody has to find them

- **A seller has no page of their own.** "Visit the shop" still goes nowhere.
- **Messaging has no screen.** The Message button in a booking does nothing — and this is
  the gap that matters most for keeping conversations on the platform.
- **Nothing anywhere mentions import VAT or customs duty**, and goods ship from Ghana into
  the EU.
- **There is still no logo file.** The wordmark is live text; somebody has to draw it as an
  SVG before a social avatar, a favicon or a slide master can be made.
- A wishlist is not remembered between visits, as the page itself says.
- The seller account steps — business registration, bank account, address confirmed by post
  — are not designed.
