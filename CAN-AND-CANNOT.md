# What an idea can include, and what needs a talk first

For the owner and for his AI. Written from how the Impats system really works.

"Talk first" does not mean no. It means: the idea is bigger than it looks, or it touches the law, money or other
people's data. Prototype it if you like, and Aco will come back with questions before anything else happens.

## How the system works, in five lines

- Clients use the phone app. They sign in with an account that Impats staff created for them. One account works
  on one phone.
- A client sees the published apartments, newest first, filters them, opens one, and asks for a viewing.
- Staff do not use the app. Staff work in Notion, as today.
- What staff change in Notion reaches the app within about an hour, between 08:00 and 20:00. Not instantly.
- What a client does in the app reaches Notion within moments.

## Can

Ideas like these fit the app as it is.

- Change what an apartment shows in the list or on its page, from information apartments already have: name,
  description, rent, photos, video, PDF, neighbourhood, address, size, rooms, furnished, features, available from.
- Change the order of things, the wording, or which information comes first.
- A new way to filter or sort the list, using that same information.
- A new piece of information on an apartment. Staff would fill it in for each apartment in Notion.
- A new question in the client's profile. Today the profile has: name, company, household (single, couple,
  family), income, budget (the rent they look for), rooms, furnished or not, notifications on or off. The client
  can edit these.
- Something a client keeps for themselves: saved apartments, a note, a choice that is remembered.
- A change to the viewing request: what the client is told, what they confirm, an extra question they answer.
- A new screen or a new tab for clients.
- A change to when a client gets a notification, or what it says. Today there is one: new apartments that match
  the client's preferred rooms.
- A new empty, loading or error message.

Good to know, even for these:

- A client only ever sees published apartments and their own profile and viewings.
- A viewing request today is "this client asked about this apartment". It has no status, and the client cannot
  cancel it. Staff may set a day and time in Notion; the client sees it and cannot choose or change it.
- The list in the app updates by itself. There is no refresh button, and none is needed.
- Every prototype idea gets a size from Aco (small, medium, large) before anything is built.

## Cannot without a talk first

### Money
- Payments, deposits, fees, invoices, anything where money moves in the app.

### The phone's permissions
The app may send notifications. It has no other permission. These each need one, and a new version in the app
stores:
- Location ("apartments near me", distance from where I am).
- Camera or photos (a client uploads a photo or scans a document).
- Calendar (put a viewing in the client's calendar).
- Contacts, microphone, Face ID or fingerprint.

### Other people's data
- Showing one client anything about another client: who else asked for a viewing, how many others are
  interested, names, comments, ratings.
- Chat or messages, between clients or between a client and staff.
- Clients uploading documents (passport, payslips, contracts, proof of income).
- Collecting more personal information than today, for example nationality, employer details, date of birth.
- Following what clients do in the app (which apartments they looked at, for how long) to show it to staff.

### Who can use the app
- People creating their own account. Today only staff create accounts.
- Signing in with Google, Apple or a code by e-mail or SMS. "Forgot password". Using one account on two phones.
- Anyone who is not a signed-in client: landlords, partners, the public, a website version.
- Different kinds of client that see different things.

### Staff work
- Anything staff would have to do in a new way. Staff have no app and no screen of ours yet; they have Notion.
- Clients choosing or changing a viewing time, staff confirming or declining a request, or a calendar of free
  slots. Today staff only set a day, in Notion.
- Clients cancelling a viewing request. It was left out on purpose for now.
- Staff being told about something right away (a new request, a message).
- Anything that must appear in the app at the very moment staff change it.

### Outside services
- Maps, routes, public transport.
- WhatsApp, e-mail or SMS sent by the app.
- Translation, an AI assistant, automatic texts.
- Data from property websites.

### The look and the language
- New colours, fonts, logo or a different style. The look was just approved.
- A light version. The app is dark only.
- Another language. The app is in English.
- A tablet or web version.

## Never, in any prototype

- Real clients: names, e-mail addresses, phone numbers, income, documents.
- Real passwords, access codes or links to Notion.
- Screenshots or exports from Notion.

Use invented people and invented apartments. The kit's `app.html` already has them.
