# The app today: every screen and what it does

For the owner's AI. This is what `app.html` contains (the approved prototype of 2026-11-27). Screen names here
are the names to use in `CHANGES.md`. In the code, screens are in `SCREENS`, bottom sheets in `SHEETS`, actions
in `A`, the state in `S`, and the invented data in `APARTMENTS` and the accounts list.

The app has three tabs at the bottom: **Apartments**, **Viewings**, **Profile**. The tab bar shows icons only, no
labels; an orange pill slides to the chosen tab.

## Before the tabs

| Screen | What a client sees and can do |
|---|---|
| **Splash** | Logo and a spinner while the app starts. After 2 seconds: "Still loading". A failed start never signs the client out. |
| **Update required** | Shown when the installed version is too old. One button: open the store. |
| **Sign in** | Email and password (with a show/hide eye). Staff create the account; there is no sign-up and no "forgot password". "Trouble signing in? Contact Impats" opens the Contact sheet. Messages: wrong email or password (one message for both), account no longer active, account already in use on another phone, no connection. |
| **Profile completion** | Only at the first sign-in, three steps: About you (first name, last name, company optional) → Your household (household: single, couple or family; income) → What are you looking for (budget, rooms, furnishing, new-apartment alerts on or off). The client can sign out here but cannot skip it. |

## Apartments tab

| Screen | What a client sees and can do |
|---|---|
| **Apartments** | The list of published apartments, newest first. It updates by itself: there is no refresh. The header has only the title and the filter button; a small number on the button shows how many filters are on. There is no "N available" line. Active filters show as chips that can be removed, with "Clear all". Apartments that arrived since the list was last loaded come first with an orange ring and a "New" tag. States: loading, error with "Try again", nothing published, nothing matches (with "Reset all filters"), offline (shows the last saved list). |
| **Apartment card** (in the list and in Viewings) | The photo with: rooms, size, a furnished icon, the available date; a play badge if there is a video; the rent per month; "New" if new. Under the photo: the title, the neighbourhood, and, if the client asked for a viewing, "Viewing requested" or the viewing day staff set. |
| **Filters** (sheet) | A tall sheet with one card per question: Price (range), Area (neighbourhood chips), Rooms, Size (range), Furnishing (furnished or unfurnished; tapping the chosen one again unselects it, which means any), Extras (feature chips). The button at the bottom shows live how many apartments match. "Reset" clears the sheet. |
| **Apartment details** | Photos to swipe through, then the video if there is one. Neighbourhood, title, address, rooms, size, furnished or not, the description (three lines, expandable), feature icons (tap one to see its name), and "Apartment PDF". At the bottom: the rent, the available date, and "Request viewing". After a request the button is replaced by "Viewing requested" and the viewing day or a note about documents. |
| **Apartment PDF** | The apartment's PDF shown inside the app, with loading, an error with "Try again", and "open in another app". |
| **Request a viewing** (sheet) | "Request a viewing?" with the apartment title, the client's income next to the rent ("Your income", "Rent"), a note that an appointment follows after all required documents, then "Send request" or "Cancel". A request cannot be cancelled in the app. |

## Viewings tab

| Screen | What a client sees and can do |
|---|---|
| **Viewings** | The apartments the client asked to view, as the same cards. Tapping one opens its details. Empty: "No viewings yet" with a button to browse apartments. A viewing has no status. Staff may set a day and time; the client only sees it. |

## Profile tab

| Screen | What a client sees and can do |
|---|---|
| **Profile** | Initials, name, company, email. "About you": one card with Household and Income, with Edit. "Looking for": one card with Budget, Rooms and Furnishing. Each row: icon left, value in the middle, title right. Settings: new-apartment alerts on or off, Change password, Log out. A quiet "Delete account" link, and the version. |
| **Edit profile** (sheet) | A tall sheet over Profile with the same fields as profile completion, all at once. Save is fixed at the bottom; it closes the sheet and shows "Profile updated". The × or a tap outside throws the edits away. |
| **Change password** (sheet) | Current password, new password (at least 8 characters), repeat. |
| **Delete account** (sheet) | A confirmation, then back to Sign in with a notice. |
| **Contact Impats** (sheet) | The support email and phone. Both are placeholders for now. |

## Forms

Every form (sign in, profile completion, edit profile, change password, filters) uses the same layout:

- Text fields that follow each other form one card: a row per field, label left, value right.
- Every other question is its own card: an icon in a round orange-tinted badge and the title, then the control.
  The answer shows only in the control, never again in the title row.
- Choices (household, rooms, furnishing) are a row of segments; the chosen one is filled orange.
- Sliders (income, budget) show the amount under the track, between the lowest and highest value. Before the
  first move it says "Move the slider".
- An error message appears under its field only when there is one.

## Notifications

One kind: "N new apartments match your preferences". Tapping it opens Apartments with the new ones first. The
app asks for permission to send notifications when the client switches alerts on, not at the first launch.

## The DEMO panel

Beside the phone. It is not part of the app. It reaches every state:

- **Sign in as:** a new client, an existing client, wrong password, account on another phone, deactivated account.
- **Jump to** any screen, including four versions of the details screen (all media, Drive video, missing data,
  very long texts).
- **Network:** online, slow, offline, server error.
- **Data:** no apartments, no viewings or two viewings, viewing day set by staff on or off.
- **Events:** a new-apartments notification, staff deactivate the client, update required, video fails.
- **Display:** text size 100, 130 or 200 percent; small phone.

## What the app does not have

No search box, no sort control, no map, no saved or favourite apartments, no sharing, no chat, no call button,
no cancelling a viewing request, no choosing a viewing time, no sign-up, no "forgot password", no other language.
