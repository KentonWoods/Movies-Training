# Movie Analytics Database

This is the dataset I use across my Tableau and BI tutorials. It's built on fun movie data — actual titles, studios, directors, actors, box office numbers, and review scores from 2015 through 2024.

I went with movies because everyone has opinions about them. When you're building a dashboard on *Barbie* vs *Oppenheimer* or comparing Marvel's box office to A24's, you actually care what the numbers say. That makes learning stick.

## What's in here

There are five tables, all pre-joined and pre-calculated so you can connect Tableau directly without writing SQL.

**MOVIE_DETAILS** — The main table. One row per movie (284 total) with everything flattened: title, studio, genre, content rating, director, lead actor, lead actress, budget, domestic and worldwide gross, opening weekend, critic score, audience score, and a bunch of calculated fields like ROI, net profit, performance tier, and the gap between critic and audience scores. This is the table I use for probably 80% of my videos.

**BOX_OFFICE_TRENDS** — Weekly box office revenue for every film. About 4,400 rows. Each row is one movie + one week, with that week's domestic and international gross, cumulative totals, theater count, per-theater average, and week-over-week change. Good for line charts, area charts, and anything where you want to show how a movie's revenue builds or drops off over time.

**STREAMING_PERFORMANCE** — Monthly streaming metrics by platform. Around 16,000 rows. Estimated views, hours watched, completion rate, and whether the movie was featured on the platform's homepage that month. Useful for comparing how movies perform theatrically vs on streaming, or for platform-level comparisons.

**STUDIO_SCORECARD** — Quarterly studio performance with targets. Each row is one studio + one quarter, showing films released, total revenue, average scores, hit rate, and how they tracked against their quarterly targets. This is the table I use for KPI dashboard tutorials with actual vs target comparisons.

**ACTOR_POWER_RANKINGS** — Actor-level aggregates. Total films, total and average worldwide gross, average scores, franchise vs original film split, and career span. Broken out by lead actor and lead actress. I use this for LOD expression tutorials where you want to compare an actor's average to a movie's performance to a genre's average.

## Where the data comes from

The core movie data — titles, studios, budgets, box office, rotten tomatoes scores, cast, directors — is sourced from publicly available information. The financials are approximate but close enough for dashboard work.

The time series data (weekly box office curves, monthly streaming numbers) is generated algorithmically from the real financial data. So a movie that grossed $700M domestic has a proportionally larger weekly curve than one that made $15M, and sequels drop off faster than prestige films — but the week-by-week numbers aren't exact actuals.

Awards, marketing budgets, and studio targets are also generated but grounded in the real data.

## How to use it

Use the CSV exports in this folder if you'd rather skip the Snowflake connection.


