# Version 21 — the phone gets a switch, and it gets out of the way

Published 12 November 2026, the same afternoon as version 20. v20 made the
phone a real marketplace; this one changes how you move around it.

| | Link |
|---|---|
| **Phone** — open on an actual phone | `/v21-2026-11-12/mobile/` |
| Desktop | `/v21-2026-11-12/` |

The desktop is unchanged from version 20. **Everything below is the phone.**

## 1. Seasonal and special offers have somewhere to live

The team asked for a slot where campaigns can sit on the screen buyers
actually land on. There is one now, at the top of the phone home screen:
five campaigns, swipe between them, dots for where you are.

**The campaigns are not a second list.** They are read out of the desktop
landing page's hero at build time — ground colour, eyebrow, headline, lede,
button, photograph and the discount disc. Change a campaign on the desktop and
the phone changes with it. The build stops rather than shipping an empty slot
if that markup moves.

**It does not rotate by itself.** A band that moves on a 390px screen competes
with the goods beneath it, and an auto-advancing carousel then needs a pause
control taking room the screen has not got. Swipe and dots instead, so there
is nothing to pause.

The layout, the type and the colours are the desktop's own — specifically the
desktop's own *phone* rules, which already answer this at 820px and narrower:
photograph on top, text under it, and the discount disc shrunk to a white
circle moved clear of the product. The first attempt invented a side-by-side
layout with a different green, black headlines and a square tag, and was
rightly thrown out.

## 2. Products and Services, as one control

A switch at the top of the home screen: **Products** or **Services**. It
changes the categories and the list underneath it. Tap a side, drag the
handle, or use the arrow keys.

**It pins itself to the top of the screen and gets out of the way while you
read.** Scroll down and it slides up off the screen along with the header.
Scroll back up and it returns, pinned to the very top. While you are browsing,
the chrome on screen is **54px — six per cent of the screen** rather than the
174px it would cost to pin the header as well.

Coming back takes a deliberate upward scroll of about 100px, and the counter
resets if you change direction, so a thumb wobble never pops it out. That is a
feel decision, and it is the one thing in this release most likely to change
after the team has it in their hands.

**What this replaces:** the home screen used to open straight onto goods with
services below the fold. The September complaint — services arriving too late
— is answered by a control rather than by moving sections around.

The landing lists are now called **Top picks** and **Popular services**,
because they are eight items, and "Goods" promised the whole catalogue.

## 3. Filters you can tell apart

With a switch, a Filters button and a row of chips all filled green, nothing
on the screen said which was a choice and which was already chosen. **An
unselected filter is now an outline on white; a selected one is a solid
fill.** Same colour, different weight. Measured 6.07:1 for the text and the
outline, and the chip is exactly the same size in both states, so nothing
shifts when you pick one.

Filters live on the Goods and Services screens. The landing screen has none,
because there is nothing there to filter yet.

## 4. Smaller things, all of them consistency fixes

- **The struck-through price was as loud as the real one.** It had no rule of
  its own and inherited the price's 20px at weight 800. It is now 13px,
  regular weight, grey — which is exactly what the desktop does.
- The filter green moved from the darkest green to the brighter action green,
  which is the green the desktop uses for the same controls.
- "See all" had been an unstyled browser button, 56×24, since the phone build
  was written. No tap-size sweep had ever run on a screen that showed one.

## Checked before publishing

- **Five scripted passes in a real browser at 390px**: buying, booking, both
  routes into Become a seller, the offers carousel, and the switch. No page
  errors, no console errors.
- **No external requests at all**, verified by watching the network. Manrope
  400/700/800 confirmed loaded.
- **Nothing under 44px. No sideways scroll** at 390px or 320px.
- The switch returns correctly at three different scroll depths, survives an
  eight-cycle ±20px wobble without reappearing, and never hides at all under
  `prefers-reduced-motion`.
- Five builds, **20 of 20 static checks each**; shared-component drift clean;
  `check-tokens.py` in step; `check-prototype.py` reports nothing lost;
  `sync-check.py` says every generated file is current with its source.
- The QR code in this folder was decoded back and matched against the intended
  URL before it was committed.

### Faults these checks found, and what each one was

Worth recording, because none of them were visible in a screenshot:

1. **The offers slot rendered completely empty, with no error.** The guard
   tested `window.CAMPAIGNS`, and the data is a `var` inside a closure — never
   on `window` — so the test was always false. A guard that cannot fail is not
   a guard.
2. **A dead end whose way out went nowhere.** "Nothing found" offered *Browse
   all goods*, which kept the search term and landed on 0 of 24.
3. **The pinned switch was not pinned.** A parent carried `overflow:hidden`,
   which silently makes it the scroll box for anything sticky inside it. The
   top of the page looked identical either way; the measurement caught it.
4. **A class name collision inside one stylesheet** gave the switch strip a
   carousel slide's padding — 110px where 54 was asked for.
5. **"It only comes back at the top."** Any downward pixel reset the return
   counter, and a finger scroll is never one clean direction, so the counter
   rarely completed. Momentum under 6px is now ignored.

## Still true, and still deliberate

Placeholder content throughout — sellers, prices, ratings, campaigns and
appointment times are not real offers, and the screens that could be mistaken
for one say so. The phone still has no sign-in, no seller dashboard and no
impact page; Orders and Account say they are not built.
