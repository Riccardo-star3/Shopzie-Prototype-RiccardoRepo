# What changed — version 15, 14 October 2026

A tidying release rather than a new feature: four things a person using the prototype
would notice, one correction to a number the product was stating twice, and the first
piece of guidance written for the people who will actually supply the photographs.

Everything here is still placeholder content. **Nothing is a commitment.** The sellers,
the customers, the prices, the ratings, the nutrition figures and the written reviews are
all **invented for the prototype**.

Earlier notes: [version 14](../v14-2026-10-08/WHAT-CHANGED.md) · [version 13](../v13-2026-10-01/WHAT-CHANGED.md) · [version 12](../v12-2026-09-22/WHAT-CHANGED.md)

---

## "Join now" no longer skips the page it was advertising

Pressing **Join now** on the landing page used to drop you **2,193 pixels down a
3,143-pixel page** — past the photograph, past why you would sell here, past how you get
started, past how and when you are paid — onto the sign-up band at the bottom.

It assumed somebody pressing that button had already decided. They have not: that band is
on the landing page and is usually the first thing anybody reads about selling here. It
now opens the page at the top.

**"See the dashboard first" has gone from that page too.** It sent a person deciding
whether to sell into *another seller's* dashboard — a stranger's bookings and payouts —
with no way back to the argument they were reading.

## One number, not three

The prototype was saying three different things about what Shopziexpress charges:

- the seller dashboard's earnings chart said **"after the 8% fee"**, flatly
- the impact page says **6%**, labelled there as an illustrative figure
- the Become a seller page **refuses to name a rate at all**

The third one is right, because the product requirements contain no rate. The dashboard
chart now reads **"after the marketplace fee"**. The impact page keeps its 6%
deliberately: it is labelled, and the whole arithmetic on that page rests on it — a figure
shown with its workings is a different thing from a seller being shown an invented cut of
their own money.

## A booking now says which country

In the seller dashboard, opening a service booking shows where to go. It gave the street
and the city; it now gives the country as well, and the **Open in Maps** link carries it
too — which is the half that matters, because a street plus a Finnish postcode can match
more than one place.

## How to photograph a product

New, and aimed at sellers rather than at us. When a seller adds a product, step 4 asks for
a photo and now offers **How to photograph it** — closed until they want it.

It covers the handful of things that change the result: daylight and no flash, a plain
light background, filling the frame, one item, showing scale, wiping the lens. What not to
do: no text or watermarks, no collages, no colour filters, nobody else's face without
asking. And what the file needs to be — **4:3 landscape, at least 1600 × 1200 pixels**,
JPEG, PNG or WebP, under about 5 MB.

Those sizes are measured from this prototype rather than chosen: the product page renders
a photograph at 640 × 480 and a shop card at 304 × 228, both 4:3, so 1600 × 1200 clears
the largest of them on a high-resolution screen with room to spare.

**It promises nothing about what happens to the file afterwards** — whether it is cropped,
resized or re-encoded, and what the real upload limit is — because none of that is
designed yet, and it says so.

## Also, for whoever supplies the next photographs

The product images in this prototype are **1200 × 900**. The product page wants 1280 × 960
to be sharp on a high-resolution screen, so they are about 6% short and very slightly soft
there. Nobody would notice in a review. The next batch should be shot at 1600 × 1200.

---

## Not in the prototype, but new and worth knowing about

**Brand guidelines for the marketing team** now exist, in `handover/`, as a web page and a
four-page PDF. The colours, type and wordmark in them are read out of the live prototype
each time they are rebuilt, so they cannot quietly go out of date.

They open with the three numbers marketing must not state — the commission rate, any
community-fund amount, and how long seller checks take — because none of the three has
been decided, and impact claims are regulated in the EU.

**And they name a blocker: there is no logo file.** The wordmark is live text set in
Manrope in the page's markup. That is right for a website and useless for a social avatar,
a favicon, a slide master, print, or an email signature. Somebody has to draw it as an SVG
before any of those can be made.

## Known gaps, so nobody has to find them

- **A seller has no page of their own.** "Visit the shop" still goes nowhere.
- **Messaging has no screen.** The Message button in a booking does nothing — and this is
  the gap that matters most for keeping conversations on the platform.
- **Nothing anywhere mentions import VAT or customs duty**, and goods ship from Ghana into
  the EU.
- Side-by-side comparison of saved products is not built.
- The seller account steps — business registration, bank account, address confirmed by
  post — are not designed.
