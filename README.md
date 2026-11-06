# dineout-no-show-guard

Live demo: https://movinankith.github.io/dineout-no-show-guard/

I built this for the Swiggy Dineout GenAI challenge. It is a small dashboard for restaurant owners who lose money when guests book a table and never turn up.

## Why this problem

An empty table on a busy night can't be sold again. Reminders get ignored and overbooking is a gamble, so most restaurants just accept the loss. I wanted to see how much of it could be avoided with information Dineout already has.

## How it works

Every booking gets a risk score out of 100. The score comes from how early the guest booked, any earlier no-shows, whether it's their first visit, the size of the party, and whether they have confirmed. Tap a booking and it shows exactly which of these pushed the score up or down.

For risky bookings the app writes a short, polite message asking the guest to confirm. If nobody replies before the cut-off time, the table is released and given to the waitlisted guest who fits best. The top of the page keeps count of seats refilled and the revenue saved.

## Try it

Open the demo and press "Run the evening demo". It plays through a whole night using sample data. You can also change the average spend per head and the release time with the two sliders.

## Under the hood

It's a single HTML file with plain JavaScript and CSS. I kept the scoring rule-based on purpose, because an owner is more likely to trust a number they can see the reasons for. The messages here come from templates. In a real version I would connect a language model through a small backend, so the API key never sits in the page.

All names, bookings and restaurant details in the demo are made up.

Movin Ankith
