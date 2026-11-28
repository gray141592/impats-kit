# Building blocks and look

For the owner's AI. Use these, and only these, when you change `app.html`. Values come from `tokens.css`
(`var(--…)`); never write a colour, size or spacing as a raw number in new code.

## Look

- Dark only. Warm charcoal background, orange (`--color-primary`) for actions, selection, "New" and fact icons.
- Little text: icons and values instead of labels. One bold thing per screen: the photo.
- Apartment pages and lists have no boxes or dividing lines; hierarchy comes from type and spacing. Forms and the
  profile summary are the exception: there, each question or group is a card (`--color-surface`, a border,
  `--radius-l`).
- Text over a photo always sits on a small charcoal plate (`--color-photo-glass`), never on the bare photo.
- No all-caps labels.
- The font in this file is the system font. The real app uses Bricolage Grotesque; do not add a font.

## Blocks that exist (helpers in the code)

| Block | Helper or class | Notes |
|---|---|---|
| Button | `btn(label, action, { cls })` | Pill. Classes: none (orange), `secondary`, `danger`. Shows a busy label while sending. |
| Icon button | `.iconbtn` | Round. Can carry a small count badge (`.count-pill`). |
| Text field | `textField(label, path, options)` | Inside `.form`, fields that follow each other join into one card: label left, value right. An error shows under the field only when there is one. |
| Form | `.form` | Wrap a form's fields in it. It gives the card layout and the even spacing. |
| Question card | `<div class="field">` with `vhead(icon, '', title)` first | The card for one question: icon badge and title, then the control. Leave the value empty in a form. |
| Choice | `tiles(path, options, multi, unset)` | A row of segments, the chosen one filled orange: household, rooms, furnishing. `multi` allows several; `unset` lets a second tap unselect. |
| Value row | `vhead(icon, value, title)` inside `.vlist` | Icon left, value in the middle, title right. Used for the profile summary and in the viewing request sheet. |
| Chip | `.chip` | Pill toggle for lists: neighbourhoods, features. Selected is orange. `.chip.mini` for removable filter chips. |
| Slider | `slider(label, path, max, step, icon)` | One thumb (income, budget), the amount shown under the track. The filter sheet has two-thumb sliders (price, size). |
| Switch | `.switch` | On is orange. |
| Apartment card | `aptCard(a)` | Used in Apartments and Viewings. |
| Sheet | `SHEETS.<name>` with `sheetHead(title)` | Bottom sheet with a title and a close button. Open with `data-act="sheet" data-name="<name>"`. Add the class `tall` for a long form (Filters, Edit profile), with the button in `.sheet-foot`. |
| Toast | `toast(message, kind)` | Kinds: `info`, `success`, `error`. |
| Notice | `.notice`, `.notice.warn`, `.notice.error` | An inline message with an icon. |
| Empty or error state | `.center` with `ic(name, 'xl')` | Big icon in a soft orange circle, a short title, one line, an optional button. |
| Tab bar | `tabbar()` | Three tabs, icons only, with a sliding orange pill. Adding a tab changes the app's structure and the pill's width: say so in `CHANGES.md`. |

How the code works: one state object `S`, and `render()` redraws the screen. A tap on anything with
`data-act="name"` runs `A.name`. New state goes into `S`; new actions into `A`. Nothing contacts a server:
`request()` only waits and pretends.

## Icons

`ic('name')` draws an icon. The names are the keys of `PH` near the top of the script. To use another icon, add
a line to `PH`, for example `heart: 'heart'`, then call `ic('heart')`. Add `'fill'` as the second argument for
the filled version: `ic('heart', 'fill')`.

Only these icons are in the file. Any other name draws nothing.

In use today: `caret-left`, `caret-right`, `caret-down`, `x`, `sliders-horizontal`, `buildings`,
`calendar-blank`, `user`, `map-pin`, `eye`, `eye-slash`, `arrow-clockwise`, `play`, `file-pdf`, `lock`,
`sign-out`, `bell`, `check`, `wifi-slash`, `warning-circle`, `magnifying-glass`, `pencil-simple`,
`arrow-square-out`, `video-camera`, `squares-four`, `ruler`, `armchair`, `house`, `envelope-simple`, `users`,
`users-three`, `wallet`, `sun-horizon`, `elevator`, `stairs`, `bathtub`, `washing-machine`, `car`, `image`.

Extra, ready for new ideas: `heart`, `star`, `bookmark-simple`, `arrows-down-up`, `sort-ascending`, `caret-up`,
`note-pencil`, `chat-text`, `share-network`, `trash`, `plus`, `minus`, `check-circle`, `x-circle`, `info`,
`clock`, `funnel`, `phone`, `map-trifold`.

## Photos

The invented apartments use photos named `assets/photos/p1.jpg` to `assets/photos/p18.jpg`, and the logo is
`assets/icon.png`. They are embedded in the `KIT ASSETS` block at the end of the file. Use those names for new
invented apartments. Do not add other images.
