# What changed — version 7, 15 September 2026

A small release, from the team's feedback on version 6. Everything else is as it was:
[version 6's notes](../v6-2026-09-11/WHAT-CHANGED.md) still describe the prototype.

All content remains placeholder. **Nothing here is a commitment.**

---

## A seller can name her own category

**Seller dashboard → Add a product / Add a service → Category.**

The list now ends with **Other**. Choosing it opens two fields:

- **"What would you call it?"** — short, two or three words. This is what appears on her
  listing, so it is required: a listing filed under Other with no category name has nothing
  to show on a card.
- **"What sort of thing is it?"** — a sentence. This is what a person reviewing the
  suggestion would actually read.

Two fields rather than one free-text box because the two jobs are different, and one box has
to be wrong at one of them.

**It is on both forms, not only services.** The team asked for it on Add a service. It is one
dialog with two shapes, and a seller who can invent a service category but not a product one
would notice.

**What it says will happen.** Publishing under Other confirms that the suggested category
*would be sent to us* — it does not pretend the category simply appears on the site. What
should actually happen to a seller-proposed category is an open question: the shop and
services filter rails are built on a fixed list, so a new one has nowhere to live until
somebody decides whether these get reviewed, merged, or published as they are. **That is a
decision for a person, not a designer.**

## Two categories a seller could not previously choose

The dialog offered four categories per kind. The shop and services pages each filter on
**five**. So a seller could not list:

- a **Home & kitchen** product
- a **Garden & outdoor** service

— while buyers were being invited to browse for exactly those. Both are now in the dialog.
Two copies of one list, and nothing comparing them.

---

## Still waiting on a person, not a designer

Unchanged from version 6, and both still open:

**PRD §7.3 contradicts the catalogue.** §7.3 describes service *packages* and a requirements
form; the catalogue and this prototype are built on *appointments* — pick a time, the seller
confirms. Those are different products. **It blocks everything on the services side.**

**Delivery and returns wording comes from the PRD, not the live site.** Returns are the
seller's own window of 7 to 30 days, the buyer pays return postage unless the item was wrong,
and money is released 14 days after tracking shows delivery. The live site currently promises
free shipping and 90-day returns, which the PRD says will not exist.

## Accessibility

Checked rather than assumed. The two new fields are hidden with the `hidden` attribute, so
they leave the tab order when they are not showing — a field a keyboard can reach but nobody
can see is a trap. The dialog's focus trap still holds with them open, both clear the 24px
target and 12px type floors, and every field has a real label. Eighteen checks were driven in
a browser against the live route, and all 36 computed colour pairs on the page pass.
