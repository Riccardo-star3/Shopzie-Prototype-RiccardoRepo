# Version 20 — the phone version becomes a real marketplace

Published 12 November 2026. Same day as version 19, which is unusual and
deliberate: v19 went out in the morning, and what it showed on a phone was
four screens and six products. This is the version to open at the meeting.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v20-2026-11-12/mobile/` |
| Desktop | `/v20-2026-11-12/` |

## 1. The typeface is finally real

**Every page in this project has asked for Manrope since the beginning and
none of them ever downloaded it.** There was no font link, no `@font-face` and
no font file anywhere in the repository. So Manrope appeared only on a machine
where somebody had installed it, and on a phone — where nobody has — the
prototype has always rendered in iOS's or Android's own font instead.

Measured before the fix: at 1440px and at 390px the browser reported **zero
loaded webfonts** while the page asked for Manrope. Measured after: Manrope
400, 700 and 800, all loaded.

The font now lives in the repository as three `.woff2` files, 42 KB in total,
**inlined into every page**. Three reasons rather than one:

- the standalone builds have to stay single files you can email;
- a page that fetches nothing cannot change appearance halfway through a
  demonstration because the wifi is poor;
- a Finland-facing product should not be asking Google for a font on every
  page view.

**The phone version changed typeface to match.** It had been using Hanken
Grotesk, which is what the design direction arrived with. Both prototypes are
now one product. Hanken Grotesk was compared against Manrope across four
screens before the decision; the comparison is kept in the project as
`design/font-compare.html`.

**What moved as a result:** very little, and never sideways. Comparing the
published v19 build against this one at 1440px and 390px across six routes:
no page got wider, no layout broke, and pages are a few pixels *shorter* where
text now wraps differently — the largest change is 72px on a 2,056px page.

## 2. The phone carries the whole catalogue, not a sample of it

v19's phone build had **six products and three services, typed by hand**. That
is enough to show a layout and not enough to show a marketplace: filters over
six items are a filter over a lie, and search had almost nothing to find.

The phone now carries **24 goods and 24 services — the same catalogue the
desktop shows**, lifted from `design/shop.html` and `design/services.html` at
build time rather than retyped. There is no second copy to drift out of date.

## 3. The buyer journey works end to end

You can now do the whole thing on a phone, twice over — once for goods, once
for a booking:

**Browse.** Goods and services each have their own list with a running count
("24 of 24"), eight at a time with a Show more. A filter sheet slides up from
the bottom: six groups for goods (category, ships from, arrives within, seller
rating, offers, sort) and five for services (category, town, rating,
availability, sort). The apply button counts the results before you commit to
them — *Show 4 results* — and the filters you chose stay on screen as chips
you can take off one at a time.

**Search.** One field searches both halves of the marketplace at once and
shows goods and services in one set of results.

**Buy.** A product page with stock, delivery time, seller and Add to basket. A
service page with a day strip, a time grid and a booking that lands in the
basket next to the goods — kept in separate sections, because a parcel from
Ghana and a cleaner in Helsinki are not one order.

**Check out.** Four steps, one thing per screen, with the step number visible
throughout: account, delivery (or your appointment), payment, check and pay.
The money-held-until-it-arrives promise is stated on the screen where it
matters. Nothing is really ordered; the confirmation says so.

## 4. Become a seller, reachable

The seller screen exists on the phone — why sell here, how you get started,
what it costs — and it says plainly that **the commission rate is not settled**
rather than inventing one. The six per cent on the impact page is labelled
there as illustrative and is not repeated here as if it were decided.

## Checked before publishing

Everything below was run, not assumed:

- **Three scripted passes through the build in a real browser at 390px**: the
  buying journey, the booking journey, and both routes into the seller screen.
  No page errors, no console errors.
- **No external requests at all** — verified by watching the network, not by
  reading the source. Manrope 400/700/800 confirmed loaded.
- **No tap target under 44px. No sideways scroll** at 390px, on any screen
  reached.
- Twelve pages, **20 of 20 static checks on each**; shared-component drift
  clean; `check-tokens.py` in step; `sync-check.py` says every generated file
  is current with its source.
- The QR code in this folder was decoded back and matched against the intended
  URL before committing.

### Four faults these checks found, and the fix for each

Worth recording, because each one was invisible until something clicked it:

1. **Search was quietly narrowed by the browse filters.** Searching "shea"
   returned nothing while Raw shea butter sat in the catalogue. Typing a word
   is a different intent from narrowing a list; search now ignores the filters.
2. **A dead end whose way out went nowhere.** "Nothing found" offered *Browse
   all goods*, which kept the search term and landed on 0 of 24. Leaving the
   search screen now clears the query.
3. **The seller screen had been written and was unreachable** — no control
   anywhere pointed at it.
4. **Two lines ran together in the basket**: "Ground spice blend, 250" /
   "gDebbies". Caught on a screenshot; no static check can see it.

## Still true, and still deliberate

Placeholder content throughout — sellers, prices, ratings and appointment
times are not real offers, and every screen that could be mistaken for one
says so. Orders and Account say they are not built.
