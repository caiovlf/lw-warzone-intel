# Last War Warzone Intel

A static, English-language transfer outlook for the complete **1573–1636** group (64 servers). The site works without a backend or build step.

## Pages

- [`index.html`](index.html) / [`transfer_outlook_1573-1636.html`](transfer_outlook_1573-1636.html): current strength ranking, projected state, tier allocations, point estimates, and modeled point growth room.
- [`growth_1573-1636.html`](growth_1573-1636.html): server and player comparisons between the 23 September and 2 October 2026 saved snapshots.
- [`player_impact_1573-1636.html`](player_impact_1573-1636.html): strongest 50 tracked players per server, model influence, and one-player-at-a-time rank sensitivity.

The old `1605-1668` filenames redirect to the corrected group, preserving existing links and player-selection query strings.

## Publication

GitHub Pages publishes `main` from `/(root)`. The root [`CNAME`](CNAME) records `lw-warzone-intel.caiovlf.com`; `.nojekyll` is retained.

## Model and data

The 64-server group has a **fixed allocation of 16 Limited Open, 32 Semi-Open, and 16 Fully Open**. Within the model, rank #1 is strongest: ranks 1–16 fill Limited, 17–48 Semi, and 49–64 Fully. The model ranks servers using equal weights for within-group percentiles of their top-10 and top-50 players' average hero power. A server crossing a state boundary displaces another, so the counts remain fixed on both dates.

The historical transfer record for the preceding **1509–1572** group comes from the supplied Excel workbook's *Warzone Scoring* and *Server Strength* sheets. Its 7 September point distribution provides the point proxy. The historical August top-three alliance ranking reproduced 50 of its 64 observed September labels. An older-group backtest of the point proxy had a mean absolute error of about 382 points; the point forecast and its headroom are rough estimates, especially near cutoffs. The game's actual Warzone Score formula and future cutoffs are unavailable.

The current 2 October figures use [LWServers rankings](https://lwservers.com/data/snapshots/1573-1700/rankings.json?v=2026-10-02T04%3A03%3A05.713Z) and per-server player JSON. The growth comparison uses 23 September files saved locally at that date. The API's `v=` value is a cache-busting query parameter, not a historical archive; requesting the September URL today may return newer data. Both snapshots are embedded in these static HTML files, and the site does not update automatically.

Player growth is matched by UID across all 128 servers in the API segment. A server's tracked hero-power change includes retained players and roster arrivals or departures. The player page's solo growth room changes one player's hero power at a time and re-ranks all 64 servers; percentages for different players cannot be added. The outlook page's point growth room is a separate proxy based on estimated points, so the two measures can differ.

Fixed tier allocations describe allowed intake by state, not vacant seats. Confirm the game's final classification and available seats in the transfer screen.
