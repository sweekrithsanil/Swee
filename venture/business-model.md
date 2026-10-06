# Business model: game-style dashboards for small businesses

Started 2026-10-06. Idea came from the Instagram reel saved in
`../inspiration/reels.md` ("App or game?"): business software that looks and
plays like a strategy game, built fast with AI.

Everything marked **ASSUMPTION** is a guess to test, not a fact. Everything
marked **TODO** needs a real answer from Sweekrith before it counts.

## One line

We turn a small business's boring numbers (orders, stock, deliveries, bookings)
into a live, playable scene the owner actually enjoys opening every day.

Demo already built: **Kitchen Run** (a home kitchen with orders, scooters and
live sales). https://claude.ai/artifact/593eEmuyD5iqpVjQNNbsX3 (sample data).

## Who it's for

Start local, in Mangalore, where we can meet people in person.

| Segment | What the "game" shows | Why they'd care |
| --- | --- | --- |
| Home kitchens and caterers | Orders cooking, scooters out, daily sales | Replaces a messy WhatsApp + notebook |
| Bakeries and sweet shops | Stock on shelves, festival rush | Knows what to bake before Ganesh Chaturthi / Diwali |
| Small clinics and labs | Patients waiting, rooms in use | Calm, clear view of the day |
| Tuition centres | Batches, attendance, fees due | Parents see progress |
| Delivery and fish/vegetable suppliers | Trucks, routes, stock | Fewer missed deliveries |

TODO: pick the first one segment. Mom's business could be the first test
customer once we know what she sells.

## What we sell

1. **Free demo from their own data (the hook).** Owner sends last week's orders
   (photo of the notebook, WhatsApp export, or an Excel sheet). We send back a
   playable scene in 48 hours.
2. **Setup.** One-time, we connect their real orders and stock.
3. **Monthly plan.** Hosting, updates, and a weekly "how did the game go" summary
   sent on WhatsApp.
4. **Templates.** Once we've built the kitchen version, the bakery and clinic
   versions start at 70% done. This is where the margin comes from.

## Pricing (all ASSUMPTION, test with the first 5 customers)

| Item | Price |
| --- | --- |
| Demo | Free |
| Setup | ₹4,999 one-time |
| Monthly | ₹799 / month (Starter), ₹1,999 / month (adds WhatsApp summaries and stock alerts) |
| Custom scene (clinic, fleet) | ₹15,000+ one-time |

Check against what local owners say they would actually pay. TODO.

## Costs (ASSUMPTION, verify real prices before relying on these)

- AI building tools and hosting: TODO (check current plan prices).
- Voice and AI video generation for marketing: TODO (credits are used per video).
- WhatsApp Business messaging: TODO (Meta charges per conversation).
- Your time: the biggest cost. Template-first building keeps each new customer
  to a few hours.

Rough break-even logic: if costs per customer are small, 20 customers on the
Starter plan is about ₹16,000 / month. TODO: replace with real numbers after
the first 3 customers.

## Why it can work

- Owners don't open dashboards, but they do open something that feels like a
  game. Daily use is what keeps them paying.
- AI makes each scene fast to build, so a ₹800 plan can still be profitable.
- Local, in-language, WhatsApp-first (English, Kannada, Tulu) is something big
  software companies won't do for a 5-person Mangalore shop.

## Risks

- **Novelty wears off.** Mitigation: the scene must save real time (orders,
  reminders), not just look cool.
- **Owners won't type data in.** Mitigation: accept WhatsApp messages and photos
  of the notebook; no new habit required.
- **Price pressure.** Mitigation: sell the weekly summary and stock alerts, not
  the graphics.
- **Platform rules.** Don't automate comments, DMs or follows. See
  `distribution.md`.

## First 30 days

1. Pick one segment and 5 real businesses to show the demo to. TODO.
2. Turn Kitchen Run into a version that reads a real orders sheet.
3. Run the distribution loop in `distribution.md` for 4 weeks.
4. Success = 3 free demos delivered, 1 paying customer. If not, change the
   segment, not the idea.
