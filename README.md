# LA City Pools — Pool Relay preview

An unofficial working preview of the City of Los Angeles Department of Recreation and Parks
[Citywide Aquatics page](https://recreation.parks.lacity.gov/aquatics), with every year-round
pool's hours on one live [Pool Relay](https://www.poolrelay.com) schedule. Not a City of Los
Angeles website; every page says so in a ribbon across the top.

## What it shows

- **Find a pool** (`index.html`): which pools are in the water right now, for lap swim, rec swim,
  water fitness or lessons, on how many lanes and until when; by day for the next week; by area
  of the city or nearest to you; on a map. Read live from Pool Relay (`finder.js`).
- **Every pool, one day**: a Pool Relay day view, one row per pool.
- **A page per year-round pool** (`pools/*.html`): today's status, a lane calendar, the pool's
  facts, and what a swimmer runs into on the department's current page.

## The schedule behind it

Read from the department's 26 year-round pool pages and their fall 2026 brochures on
October 21, 2026: 18 pools entered (899 weekly series, Sep 6 – Jan 3), plus the John C. Argue
Swim Stadium already in Pool Relay. Lap and rec swim are cut into time blocks around lessons,
teams and classes so no lane is booked twice. **Lane assignments are our estimate** wherever a
pool doesn't publish them; lane counts are from the pool or from places2swim/swimmersguide, or
a standard 8 where none was found (each booking says which).

Not entered: Dymally High School Pool (hours with no dates, summer brochure only) and the pools
closed until further notice (Cleveland, Fremont, Hey Rookie, Peck, Roosevelt, Woodland Hills).

## Building

`python3 build.py` writes `index.html`, `pools.js` and `pools/*.html` from `pools-base.json`
(the department's pool list) and `site.json` (view tokens, notes, findings).
