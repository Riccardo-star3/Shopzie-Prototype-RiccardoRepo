# What changed — version 9, 15 September 2026

The third release today, and it is all about **signing in**. The account icon in the top-right
now opens a real panel, on every page, and the checkout's first step matches it exactly.

Everything here is still placeholder content. **Nothing is a commitment.** No message is sent,
no code is texted, nothing is saved or checked.

Earlier notes: [version 8](../v8-2026-09-15/WHAT-CHANGED.md) · [version 7](../v7-2026-09-15/WHAT-CHANGED.md) · [version 6](../v6-2026-09-11/WHAT-CHANGED.md)

---

## There is a sign-in panel now, on every page

Click **Account** in the header, then **Sign in** or **Create an account**. Until this release
those two went nowhere.

It is the same panel on all six pages, generated from one source rather than copied six times.
It closes on Escape, keeps the keyboard inside it while it is open, and puts focus back on the
Account button when it closes.

## One field takes an email **or** a phone number

This is the change the team asked for, and the reason is Ghana: some buyers and sellers there
have no email address at all.

So there is **one box**, labelled "Email or phone number". What you type decides what happens:

- **Type an email** → you get a password field, as before.
- **Type a number** → the password disappears, a country picker appears, and the button changes
  to "Send me a code".
- **Type a number starting with `+`** → no country picker. You already said which country.

The country list is **Finland and Ghana first**, then the other 26 EU countries. Nothing else is
offered, because nothing else is a market.

A leading zero is dropped once a country code goes on the front, so `024 123 4567` with Ghana
selected becomes `+233 24 123 4567` — which is what a real code would be sent to.

**One rule worth knowing:** an account can start with only a phone number, but a second way to
reach you is required before you can sell or be paid. The create-account panel says so. A number
can be lost or reassigned, and a payout cannot hang off a single SIM.

## Apple, Google and Microsoft

Three buttons above the form, with an "or" divider under them.

The team's note said "Gmail" and "Outlook". Those are mail products, not sign-in services — the
account behind a Gmail address is a **Google** account, and the one behind an Outlook address is
a **Microsoft** account. Naming the button after the mailbox would tell anyone whose Google
account sits on a work domain that the button is not for them, when it is.

Clicking one says what it would do. None of them is wired to anything.

## A six-digit code step

The team asked for 2FA on account creation. It is a real screen, not a promise: enter six digits,
resend, or go back and use something else.

Every path ends there — signing in by email, signing in by phone, and creating an account. It
says **"emailed"** or **"texted"** depending on what you typed, and names the address or the full
international number.

In the checkout the code step sits **inside** "Your account" rather than becoming a fourth circle
on the progress bar. The bar counts the stages of an order; proving who you are is not one of
them. Going back to correct your address later does not ask for a code again.

**One honest note for the team, which is written up in full in the project notes:** on the email
path this really is two-factor — a password you know, plus a code sent to something you have. On
the phone path there is no password, so the code is the only proof. That is passwordless sign-in,
not two-factor. It changes no screen, and it matters when sellers start getting paid.

## The checkout lost its green dashed banners

There were three: one at the top of the page, one over the sign-in step, one over the card
fields. Two of them explained things that no longer need explaining — the sign-in step is built
now, so "signing in is not built here" had become untrue.

The third one stayed, because it is the only one with a real consequence behind it: it stops
someone demoing this from typing a real card number. It is now a quiet grey line next to the card
fields instead of a dashed green box. A warning that appears three times stops being read as a
warning.

The sign-in panel's own notice was softened the same way, for the same reason.

## Accessibility

Checked on the built page, not assumed:

- Every new control clears the 24 × 24px minimum. The provider buttons are 48px tall.
- No text below 12px anywhere.
- No sideways scrolling at 1280px, 390px or 320px.
- The code field is **one input**, not six separate boxes. Six boxes look the part and break
  everything that matters: a screen reader announces six unlabelled fields, pasting a code from a
  text message fills only the first, and the phone's "tap to fill the code" has nothing to attach
  to.
- Colours measured, not guessed. The quiet grey line is 5.74:1 on white; the green code note is
  6.47:1.

## Still waiting on a person, not a designer

- **Sellers in Ghana cannot be paid through Stripe.** Stripe Connect only pays out to the US, UK,
  EEA, Canada and Switzerland. Ghana is not on that list and points to Paystack instead. This is
  true whatever the sign-in looks like, and the weekly Friday payout promise depends on solving
  it.
- **PRD §7.3** still describes service *packages* where the catalogue offers *appointments*. That
  contradiction is in the PRD itself and blocks the services side.
