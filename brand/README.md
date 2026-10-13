# Uptown Tonight

Every deal Uptown, by the clock.

Uptown Tonight helps Miami underclassmen plan a night in Oxford: which bars they can get into, what each one is running, and when. The brand borrows two ideas. From transit apps like Citymapper it takes the idea that **the night is a route**: every bar is a line with its own color, and every deal is a stop with a time. From list apps like Beli it takes the idea that **plans are lists you share**: ranked, opinionated, easy to send to the group chat. It borrows those ideas only. It never borrows either app's logo, colors, icons or name.

## Content fundamentals

**Voice.** The friend who always knows the move. Short, specific, a little playful, never hype.

- **Time first.** Lead with when: "From 1pm", "5 to 8pm", "Until 4pm". People are planning around the clock.
- **Honest about freshness.** Every deal says when it was last seen. Missing info is said plainly: "Price not posted yet", never a guess.
- **Plain bar names.** Use the names students say: Brick, Corner, Skippers, Side. Full names in detail views.
- **No pressure to drink.** Never write "get wasted", "drink up" or anything that rewards volume. For the 18 to 20 view, lead with entry, covers, food and events. Never imply under-21s will drink.
- **No emoji in UI copy.** Personality comes from the type and the bar colors.

| Do | Don't |
| --- | --- |
| Brick's clock starts at 1pm. $1 pitchers for the first hour. | INSANE $1 PITCHERS AT BRICK!!! |
| Price not posted yet | $?? |
| Seen Sep 26 | Updated recently |
| Rented out for a private event. Closed to the public. | Brick is closed lol |

## Visual foundations

**Color.** A quiet, cherry-tinted neutral base (`surface-100`, `surface-200`, `surface-300`) with `ink` text. `brand` (Uptown Cherry) is the only loud color, and it appears once per region: the Live pill, the wordmark accent, the primary action. Each bar owns a `line-*` color that shows up only in its bullet and its route segments, the way a subway line does. Status colors (`signal-good`, `signal-warn`) only carry meaning and never decorate.

**Type.** Two faces. Bricolage Grotesque (`display`) is the personality: wordmark, day headings, rank numerals. Onest (`body`) does the work: card titles, prices, meta. Prices always use tabular numerals.

**Shape.** Soft and tappable. Cards use `radius-lg`, controls use `radius-md`, bullets use `radius-sm`, and anything that is a status is a pill. Cards get `shadow-card` and no border. Never a colored stripe down the side of a card; bar identity lives in the bullet.

**Layout.** Phone first, one column, 560px max. Order on every day view: age switch, week strip, day heading, notices, then the night in time-of-day sections (At the door, Daytime, Happy hour, Late night, Any time). Older unconfirmed reports collapse at the bottom.

**Motion.** Small and physical: cards press in slightly, the detail sheet slides up, the Live dot pulses. Everything respects reduced motion.

## Iconography

Simple 2px stroke line icons with round caps (chevron, check, dash, close). No icon font, no emoji. Bars have no logos in the app. Each bar is shown as its **bar bullet**: a `radius-sm` square in its `line-*` color with two white initials (BS, CB, SK, CH, LR, SB, 18).

## Logo

No logo yet. Until there is one, the wordmark is "Uptown Tonight" set in `display-xl`, with "Tonight" in `brand`, next to a small `brand` location dot.

## Bar lines

Each line color nods to something in the bar's own look (seen on its Instagram) without copying its logo. Bar logos stay out of the app until a bar shares one as a partner.

| Bar | Nickname | Bullet | Token | The nod |
| --- | --- | --- | --- | --- |
| Brick Street | Brick | BS | `line-brick` | Brick orange |
| Corner Bar | Corner | CB | `line-corner` | Brown from its mark |
| Skippers Pub | Skips | SK | `line-skippers` | Navy from its logo |
| Chanks | Chanks | CH | `line-chanks` | Red wall and lettering |
| Lil Rudys | Rudy's | LR | `line-rudys` | Maroon badge |
| Side Bar / The Woods | Side Bar | SB | `line-side` | Woods green |
| Bar 1868 | 1868 | 18 | `line-1868` | Vintage slate |
| O'Pub | O'Pub | OP | `line-opub` | Pub green |
| Calendula | Calendula | CA | `line-calendula` | Marigold gold |
| Al & Larry's | Al & Larry's | AL | `line-allarrys` | Placeholder purple |

A new bar gets a new line color that passes 4.5:1 against white. The reds (Chanks, Brick, Rudy's) are told apart by lightness and by their initials. In dark mode, bullets carry a faint white ring so the darkest lines still read as shapes.

The full bar profiles (address, hours, ages, Instagram, booking contact) live in the app's `deals.json`, not here.
