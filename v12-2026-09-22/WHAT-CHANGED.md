# What changed — version 12, 22 September 2026

All on the **seller dashboard** (`#/seller`), and all about **bookings**: seeing when they are,
answering them, and cancelling one when something goes wrong.

Everything here is still placeholder content. **Nothing is a commitment.** The customer names
(Aino K., Sanna L., Mikko R., Emilia V., Adwoa M.) and their addresses are **invented** for the
prototype. No real booking, customer or payment is involved.

Earlier notes: [version 11](../v11-2026-09-21/WHAT-CHANGED.md) · [version 10](../v10-2026-09-21/WHAT-CHANGED.md) · [version 9](../v9-2026-09-15/WHAT-CHANGED.md)

---

## The date and time come first

A seller knows what she offers. What she needs to see is **when**. Every booking, in To do and
in the Services list, now starts with a small **date tile** (weekday and day number) and a bold
**time line**, "Tomorrow, 10:00". The service name moves to the grey line underneath.

The prototype's "today" is fixed at **Tuesday 22 September 2026**, so the dates always make
sense when you click through.

## A calendar view of bookings

On the **Services** tab, a **List | Calendar** switch sits next to the filters. The calendar
replaces the list in the same place (no pop-up). It shows the month, marks today, follows the
filter you picked, and lists a day's bookings when you choose that day. On a phone, days show
coloured dots instead of labels.

## One colour per status, everywhere

Booking requests were yellow in To do and red in Services. Now the whole dashboard uses the
same three colours: **red** needs you, **yellow** is booked or on its way, **green** is done.

## Open a booking to see everything about it

**Open** on any booking (in the list, or under a calendar day) opens a panel on the right. On a
phone it fills the screen.

- **When:** the date and time, with how long it takes.
- **What you earn:** the amount, and the Friday it is paid to you. The **(i)** next to it
  explains how payment works.
- **Service:** the name, what the price covers, and the order number.
- **Where:** the full address, with a **Map** button that opens it in Google Maps.
- **Customer:** their name, and whether they have booked with you before.
- **Their note:** what the customer wrote when booking.

## Accepting a booking

A request can be accepted in three places, and all three stay in step:

- **Accept** in the To do list
- **Accept** in the Services list, next to Open
- **Accept booking** at the bottom of the booking panel

## Cancelling or declining, with a reason

If a seller is ill or cannot make it, **Cancel booking** (or **Decline** for a request):

1. First asks **"Cancel this booking?"** and says what happens: the customer gets a full refund
   and the seller is not paid. **Keep the booking** is the safe choice and is selected first.
2. Then asks the seller to **tell the customer why**: a reason (I'm ill, I can't make that time,
   something else), whether to **offer another day**, and a message. The message is written for
   her from those choices, and she can change any of it.

The booking then shows as **Cancelled** or **Declined** everywhere and drops off the calendar.

**Message** and **Edit time** are shown but not built yet: messaging has not been designed.

## To do only shows what is still to do

When something is done (accepted, tracking added, marked done), it **leaves the To do list**
and moves to a green **Done today** box at the bottom, with **Undo**. A group with nothing left
disappears.

## Open questions for the team

- **How much of the price does the seller keep?** The panel shows the full price because the
  PRD does not say what Shopzie keeps.
- **The customer's side of booking** should ask for the same details the seller sees here
  (address, a note). That screen has not been designed yet.
