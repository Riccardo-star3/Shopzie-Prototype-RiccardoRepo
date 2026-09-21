# What changed — version 11, 21 September 2026

A small release, all on the **seller dashboard's Overview** (`#/seller`): the list at the top that
tells a seller what is waiting for her.

Everything here is still placeholder content. **Nothing is a commitment.** No real order, buyer
or payment is involved.

Earlier notes: [version 10](../v10-2026-09-21/WHAT-CHANGED.md) · [version 9](../v9-2026-09-15/WHAT-CHANGED.md) · [version 8](../v8-2026-09-15/WHAT-CHANGED.md)

---

## "Needs you today" became "To do"

"Needs you today" did not say what the panel was. It is now **To do**, with a count of what is
left.

## One row per kind of task, readable at a glance

Before, every task had three lines of text, and the last line was green whether it meant
"someone is waiting" or "you will be paid". Now each row has:

- a **coloured icon** for the kind of task
- a **short bold headline**, like "Ship 4 orders" or "2 new bookings"
- a **status in plain words** with a coloured dot
- **one quiet line** of detail

| Colour | Means | Example |
|---|---|---|
| Red, truck | The buyer can cancel if you wait | Ship 4 orders · **Post today** |
| Yellow, calendar | Someone is waiting for your answer | 2 new bookings · **Reply today** |
| Green, euro | Money is waiting on you | Job finished? · **Starts your payment** |
| Grey, speech bubble | No deadline | New message · **4 hours ago** |

The words are always there, so nobody has to rely on seeing the colour.

## Several orders or bookings open in place

When there is **one** item, its button sits right in the row: **Mark done**, **Reply**.

When there are **several**, the row says how many, and **Show 4** opens them underneath. Each one
has a round picture (a photo for products, an icon for services), its own details and its own
button. A short line in the row's colour runs beside each one, so they read as belonging to the
row above.

## Everything is done where it is

- **Accept** a booking and **Mark done** a finished job take one tap.
- **Add tracking** asks for the courier's number right in the row. Press Save or Enter.
- The item then says what happened (**Accepted**, **Tracking added**, **Marked done**) and offers
  **Undo**.
- The count goes down as you go, and a group says **All done** when it is empty.

No extra screens. **Reply** is not built yet, because messaging has not been designed.

## Updated the same day: orders and bookings match the To do list

A small follow-up, added to this version rather than made into a new one. It went in before
this version's link was shared with anyone.

- On the **Products** and **Services** tabs, every order and booking now has the same short
  **coloured line** as the To do list: red for To send and To confirm, yellow for On the way and
  This week, green for Delivered and Finished. The colours match the dots on the filter buttons.
- Order and product pictures are **round and a little bigger** (56px), like the To do list.
- The word above the filter buttons says **Filter** instead of "Show".

The version exactly as first published is kept under the `v11` tag in the repository.

## Accessibility

Checked on the built page, not assumed:

- Every colour pair measured. The weakest, grey on light grey, is 5.59:1, above the 4.5:1
  minimum.
- The tracking-number box has a real label, and Escape cancels it.
- After each action the keyboard lands on Undo, and a screen reader hears what happened and how
  many tasks are left.
- No sideways scrolling at 320px. Every button is at least 24px.

## Still waiting on the team

- **Should a booked appointment mark itself done once its time has passed?** The PRD says the
  seller marks it. Until that is decided, it is one tap on **Mark done**.
- **PRD §7.3**: service packages or appointments. It blocks the services side.
- **Ghana payouts**: Stripe does not pay out to Ghana.
