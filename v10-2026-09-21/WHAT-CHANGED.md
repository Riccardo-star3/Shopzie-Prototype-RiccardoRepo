# What changed — version 10, 21 September 2026

This release is all about the **seller dashboard** (`#/seller`). Nothing else in the prototype
changed apart from one small fix, listed at the end.

Everything here is still placeholder content. **Nothing is a commitment.** No real order, buyer
or payment is involved.

Earlier notes: [version 9](../v9-2026-09-15/WHAT-CHANGED.md) · [version 8](../v8-2026-09-15/WHAT-CHANGED.md) · [version 7](../v7-2026-09-15/WHAT-CHANGED.md) · [version 6](../v6-2026-09-11/WHAT-CHANGED.md)

---

## The dashboard is in panels now, like the checkout

Each section is **one white panel**, with its heading inside it and the same soft shadow as the
checkout. The tasks, orders and listings inside are **rows split by a thin line**, not separate
cards.

- The **Overview** tab went from seven boxes to two: "Needs you today" and "Your money".
- The **Products** tab went from ten boxes to two: your orders and your listings.
- Inside "Your money", the chart and the figures are separated by a line, not boxed. A box
  inside a box was ruled out on 15 September.

We looked at a second layout with the money in a column on the right of every tab, and chose not
to use it. On a phone that column drops below all the work, and most sellers, especially in
Ghana, will be on phones.

## Long lists open on the five most urgent, then Show more

A seller could have a hundred orders. Showing them all makes the page tens of thousands of
pixels tall. So every order list and listing list now:

- opens on the **five most urgent** rows: orders still to send, oldest first, because the buyer
  can cancel for a full refund until they are sent, then orders on the way, then delivered ones,
  newest first
- grows **ten at a time** with a **Show more** button, which says how many are left
- tells you where you are: "Showing 5 of 20 orders"

After Show more, the keyboard focus moves to the first new row and a screen reader announces the
new count. The panel never scrolls inside itself, because that traps a thumb on a phone and a
keyboard on a laptop.

The demo has **20 orders and 8 listings**, which is enough to show how it behaves.

## The order filters look like filters now

The three big coloured status tiles read like statistics, not like buttons. They are now a row
of **pill buttons** under the word "Show":

**All 20** · **To send 4** · **On the way 5** · **Delivered 11**

(On the Services tab: All · To confirm · This week · Finished.)

- **All** is selected when you arrive. One pill is always selected, and "All" is how you get
  back, so the old "Clear the filter" line is gone.
- The selected pill is dark green with white text. The others are white with a grey outline.
- Each pill has a coloured dot for its status and a count. The counts come from the rows
  themselves, so they cannot disagree with the list.
- A filtered list opens on five rows as well. "Delivered" shows 5 of 11, with its own Show more.

## Less text

Four lines were removed because they told a seller nothing:

- "Everything below is made up, for the prototype. No real order, buyer or payment."
- "One section at a time. Nothing is hidden from you — it is put away."
- "Money moves on a timer whether you act or not."
- "Four things. Each one says what happens if you leave it."

## One small fix everywhere

Moving to a new page (Shop, Services, Our impact, Your dashboard) no longer draws a dark focus
ring around the page title. The keyboard still lands on the title so a screen reader announces
the new page. It just no longer looks like a mistake.

## Accessibility

Checked on the built page, not assumed:

- Every colour pair measured on the rendered page at 1280px and at 320px: none fail.
- The selected pill's white text is 12.23:1 on dark green. The grey outline on the unselected
  pills is 3.86:1, above the 3:1 needed for a control's edge.
- The filters are real toggle buttons, and a screen reader hears which one is selected.
- No text below 12px. No sideways scrolling at 320px.
- The dashboard is the first page built on the new 4px spacing grid and the eight-step type
  scale that the engineering hand-over uses.

## Still waiting on a person, not a designer

- **Sellers in Ghana cannot be paid through Stripe.** Stripe Connect does not pay out to Ghana.
  The weekly Friday payout promise depends on solving it.
- **PRD §7.3** still describes service *packages* where the catalogue offers *appointments*.
  That contradiction is in the PRD itself and blocks the services side.
