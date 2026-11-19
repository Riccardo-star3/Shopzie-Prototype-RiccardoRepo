# Version 24 — help, reviews, and a seller pitch that matches the desktop

Published 19 November 2026, the same day as version 23.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v24-2026-11-19/mobile/` |
| Desktop | `/v24-2026-11-19/` |
| Booking previews — agreed, not built | `/v24-2026-11-19/preview/` |

The desktop is unchanged. **Everything below is the phone.**

## 1. The help assistant

The desktop has had one on all nine pages. The phone now has it too — same
greeting, same five suggestions, same canned reply, same line saying it is not
connected to anything.

Only the container is re-thought. The desktop parks a small card in the
bottom-right corner beside a page you can still read; at 390px that leaves a
conversation four lines tall before the keyboard eats half of it. So on the
phone it is a bottom sheet with the same shape as the filter sheet already in
the build.

Three things are the phone's rather than the desktop's. The launcher **leaves**
when the sheet opens, because the sheet covers it and an X nobody can see is
worse than nothing. The five suggestions **wrap while the conversation is still
just the greeting**, so all of them are readable before you have typed, then
collapse to one scrolling row the moment you ask something. And the input is
16px, which is not a taste decision: anything smaller and iOS zooms the page
when the field takes focus, and the frame never comes back.

## 2. Reviews on the product screen

"What buyers said" was a two-line fold with two sentences in it, which buried
the thing buyers look for before parting with money — and left the
`★ 4.9 · 124 ratings` in the seller row leading nowhere.

It is now the desktop's review block rebuilt for 390px: the average and five
percentage bars side by side, the rule about who may write one, and cards with
stars, a verified badge, the name, and the seller's reply where there is one.
**The rating is now a button** that takes you to it, and a hairline divides the
reviews from "More from &lt;seller&gt;", which used to run straight into them.

The ratings breakdown is worked out from each product's own average, so a 4.9
and a 4.7 do not show the same bars. The reviews themselves are placeholder and
say so.

## 3. Become a seller

The phone's seller pitch had drifted five ways from the desktop's: a different
heading, different words, no icon, no "Learn more" link, and an outlined button
where the desktop has a filled green one. On a recruitment pitch meant to read
the same everywhere, that is five small decisions nobody made.

It is now the desktop's, including the layout the desktop already used on
narrow screens. And the button at the end of the seller pitch is renamed
**Start selling** and pinned to the foot of the screen, so it is there when you
land and still there at the bottom — the same persistent bar every other screen
with a single job already uses.

## 4. A bar that had never pinned

Pinning that button uncovered something older: in the **app build**, the
product's buy bar had never pinned on a phone either. It sat two and a half
screens below the fold, and had done since the build was written.

The rule that makes a pinned bar work lived in the website build's own styles,
so the app build never got it. It is now shared by both. Nothing about how the
version looks changed; a bar that was supposed to follow you now does.

## What has not changed

The same 24 goods and 24 services. Nothing is really ordered, and every screen
that could be mistaken for a real offer says so. Prices, discounts, campaign
copy, availability, ratings and reviews are placeholders. The assistant answers
nothing.
