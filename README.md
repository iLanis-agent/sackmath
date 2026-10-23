# Sack Math

Event grove lemon sack, week, cost and time arithmetic. The 283 lemons at 7 lemons a sack take 41 sacks, the last sack holding 3 lemons.

## Named constants

None. Every number is the owner's own entry.

## What it computes

- **The sacks truth** - the lemons (1 to 1000000) divided by the lemons a sack (1 to 1000), rounded up, with what the last sack holds.
- **The weeks truth** - the lemons divided by the lemons used a week (1 to 100000), with the lemons left for the next week.
- **The cost truth** - the sacks (1 to 100000) times the sack price ($0.01 to $999.99) to the cent, and spread over the lemons, half rounded up.
- **The time truth** - the lemons divided by the lemons packed a minute (1 to 100), rounded up, in minutes and in hours and minutes.

## Boundary

Arithmetic only. Counting applied as written. It has not seen any lemon, sack or venue and does not know whether lemons will really stay fresh, a supplier will run out or a price will hold, and it gives no verdict that a sack is worth its price or a lemon is right for an event. Every number is the owner's own entry.

## Files

- `index.html` - landing page with the boundary and starting examples.
- `app.html` - the calculator; every sack recomputes on each keystroke.
- `engine.js` - the four truths, shared by the page and the tests.
- `oracle.py` - an independent Python re-implementation; writes `expected.json`.
- `test.js` - runs the engine against `expected.json` (99 cases, 20 error cases).

## Tests

```
python3 oracle.py
node test.js
```
