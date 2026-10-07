# Last War Warzone Intel

A static, English-language transfer outlook for the complete **1573–1636** group (64 servers). The site works without a backend or build step.

## Pages

- [`index.html`](index.html) redirects the domain root to [`transfer_outlook_1573-1636.html`](transfer_outlook_1573-1636.html), the canonical home for strength ranking, projected states, point estimates, modeled point growth room, and each server's Saving Flag. Tier allocations remain in server profiles.
- [`growth_1573-1636.html`](growth_1573-1636.html): server and player comparisons between the 23 September and 2 October 2026 saved snapshots, including overload-stage progression and compact saving signals.
- [`player_impact_1573-1636.html`](player_impact_1573-1636.html): strongest 50 tracked players per server, model influence, and one-player-at-a-time rank sensitivity.
- [`resource_saving_1573-1636.html`](resource_saving_1573-1636.html): daily-history saving signals for all 22,354 current players, a server watchlist, and the method and data-quality details behind each flag.
- [`mega_alliance_1616.html`](mega_alliance_1616.html): current server 1616 players ranked for a proposed Mega Alliance using THP and long daily kill-history participation.

The old `1605-1668` filenames redirect to the corrected group, preserving existing links and player-selection query strings.

## Publication

GitHub Pages publishes `main` from `/(root)`. The root [`CNAME`](CNAME) records `lw-warzone-intel.caiovlf.com`; `.nojekyll` is retained.

## Model and data

The 64-server group has a **fixed allocation of 16 Limited Open, 32 Semi-Open, and 16 Fully Open**. Within the model, rank #1 is strongest: ranks 1–16 fill Limited, 17–48 Semi, and 49–64 Fully. The model ranks servers using equal weights for within-group percentiles of their top-10 and top-50 players' average hero power. A server crossing a state boundary displaces another, so the counts remain fixed on both dates.

The historical transfer record for the preceding **1509–1572** group comes from the supplied Excel workbook's *Warzone Scoring* and *Server Strength* sheets. Its 7 September point distribution provides the point proxy. The historical August top-three alliance ranking reproduced 50 of its 64 observed September labels. An older-group backtest of the point proxy had a mean absolute error of about 382 points; the point forecast and its headroom are rough estimates, especially near cutoffs. The game's actual Warzone Score formula and future cutoffs are unavailable.

The current 2 October figures use [LWServers rankings](https://lwservers.com/data/snapshots/1573-1700/rankings.json?v=2026-10-02T04%3A03%3A05.713Z) and per-server player JSON. The growth comparison uses 23 September files saved locally at that date. The API's `v=` value is a cache-busting query parameter, not a historical archive; requesting the September URL today may return newer data. Both snapshots are embedded in these static HTML files, and the site does not update automatically.

Player growth is matched by UID across all 128 servers in the API segment. A server's tracked hero-power change includes retained players and roster arrivals or departures. The player page's solo growth room changes one player's hero power at a time and re-ranks all 64 servers; percentages for different players cannot be added. The outlook page's point growth room is a separate proxy based on estimated points, so the two measures can differ.

Saving signals compare robust hero-power growth slopes over 25 August–22 September and 22 September–2 October using locally saved LWS Pro daily-history responses. A strong slowdown with recent kills or overload activity is labeled “Possible saving”; it is not proof of held resources. All 22,354 current players have a saved response. The page distinguishes low prior growth, missing hero values within the window, and absent daily rows. Server flags weight the strongest 50 players by their modeled strength contribution. These flags do not alter the strength ranking or projected transfer state.

Growth also shows overload-stage changes between the two snapshots. Stage zero is treated as unrecorded because the API can use it as a placeholder. A server's overload gain totals players retained in that server who have positive stages on both dates. Overload is shown for context and is not part of the Warzone Score proxy.

The Mega Alliance view is a server 1616 planning shortlist based on the 6 October current player roster and saved LWS Pro daily kill history from 3 August to 2 October. THP contributes 60% of a player's fit score, long-period kill pace 15%, recent 28-day kill pace 10%, and the share of observed weeks with kill gains 15%. The percentile-based score is a planning choice, not a game formula. Only players with sufficient comparable history receive a fit score; missing data is labeled Unverified rather than inactive. The current player snapshot's kill total is not used in this score.

Fixed tier allocations describe allowed intake by state, not vacant seats. Confirm the game's final classification and available seats in the transfer screen.
