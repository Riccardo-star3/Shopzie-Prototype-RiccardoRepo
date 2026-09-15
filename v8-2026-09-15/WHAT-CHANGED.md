# What changed — version 8, 15 September 2026

The second release today, and a much larger one than version 7. Two areas were reworked from
the team's feedback: **the checkout** and **the seller's add-a-listing dialog**.

Everything here is still placeholder content. **Nothing is a commitment.**

Earlier notes: [version 7](../v7-2026-09-15/WHAT-CHANGED.md) · [version 6](../v6-2026-09-11/WHAT-CHANGED.md)

---

## The checkout is one step at a time

It used to be three panels on one scroll. Now there is **one panel, and a progress bar above it.**

**The progress bar** carries a label over each numbered circle, joined by a line. A finished step
is solid green with a tick, the one you are on is ringed, the ones ahead are light. It is built
from the steps that are actually in your order, never from a hardcoded three — a product order
has a delivery step where a service order has an appointment step.

**Moving around.** Back and Continue at the end of every panel, and the finished circles on the
bar are buttons: click one to go back and change something. Nothing you typed is lost. Upcoming
circles are deliberately **not** clickable — there is nothing there yet, and a control that
refuses to do anything is worse than one that is not there.

**Step one is now Sign in**, with "New here? Create an account instead" one click away. It used
to be a create-an-account form and nothing else, which asks a returning buyer to fill in five
fields to reach a basket they have already filled. Anyone at a checkout has almost certainly
bought here before. These are the same two paths the header's account menu already offers.

There is no guest option to design: **PRD §7.1 requires an account for every purchase.** Signing
in is not built in this prototype and the panel says so plainly — nothing is sent or checked.

## The checkout looks different, too

**The panels lift off the page.** They carry the same shadow as the twin-entry cards on the
landing page, so they read as objects rather than as regions of one surface.

**The fields are lighter at rest and unmistakable when you are in one.** The resting stroke went
from 1.5px to 1px and lighter in colour; the field you are filling in takes a 2px dark green
edge. The gap between the two states is about three times what it was.

> One note on the request, because it was not met in full. The resting stroke could not go as
> light as asked. The fields are white on a white panel, so the border is the **only** thing
> identifying the control, and WCAG 1.4.11 sets a floor of 3:1 for that. The colour chosen sits
> at 3.33:1, which is as light as it can go with any margin. Most of the lightening came from the
> thickness instead, which costs no contrast at all.

## The seller's Add a product / Add a service dialog

**The fields are white now**, matching the checkout. They were a pale green with a very faint
edge — measured at 1.07:1 against the panel and 1.12:1 for the edge, which means the control had
no visible boundary at all. That was an accessibility failure, not only a style preference.

**The availability calendar picks stretches of days.** Click a day, then click another: everything
between them is taken. Click the same day twice for just that one. Every pair adds to what is
already picked, so a seller can mix a fortnight with three odd days without switching modes.

- The **ends** of a stretch are solid green; the **days between** are pale green with a green
  outline, so you can see what is included.
- While you are half-way through a choice, the list of dates steps aside and **two short lines**
  explain the two options, each with a small picture of what the result looks like.
- Touching stretches **merge**; removing a day from the middle of one **splits** it. The summary
  underneath names each stretch rather than saying "first date to last date", which used to
  describe a block of days that had not been picked.
- **Clear all days** appears once there is something to clear.

**The available-time section** is now a plain white panel like the calendar above it, rather than
a green wash inside a green wash.

---

## Still waiting on a person, not a designer

Both unchanged, and both still open:

**PRD §7.3 contradicts the catalogue.** §7.3 describes service *packages* and a requirements
form; the catalogue and this prototype are built on *appointments*. Those are different products.
**It blocks everything on the services side.**

**Delivery and returns wording comes from the PRD, not the live site.** Returns are the seller's
own window of 7 to 30 days, the buyer pays return postage unless the item was wrong, and money is
released 14 days after tracking shows delivery. The live site currently promises free shipping
and 90-day returns, which the PRD says will not exist.

**And one new question.** A seller can now propose her own category under "Other". What happens
to that suggestion is undecided — the shop and services filter rails are a fixed list, so a new
category has nowhere to live until somebody decides whether these get reviewed, merged, or
published as they are. The prototype is honest about it and says the suggestion would be sent to
us rather than pretending it appears on the site.

## Accessibility

Checked rather than assumed, in a real browser and not only on paper.

Moving between checkout steps moves focus to the new panel's heading and announces the change,
because a panel that silently replaces another leaves a keyboard user standing on a button that
no longer exists. Pressing Enter in a field advances rather than placing the order. Hidden panels
and closed panes leave the tab order entirely. The calendar is a real date grid driven by the
arrow keys, and arming and completing a stretch work identically from the keyboard, with focus
surviving both. Every new control clears the 24 × 24px floor and nothing is under 12px.

Every colour pairing was computed before use. There is no known contrast exception in this
version.
