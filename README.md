# Last War Warzone Intel

A static, English-language transfer outlook for the complete **1573–1636** group (64 servers). The site works without a backend or build step.

## Pages

- [`index.html`](index.html) redirects the domain root to [`transfer_outlook_1573-1636.html`](transfer_outlook_1573-1636.html), the canonical home for strength ranking, projected states, point estimates, modeled point growth room, and each server's Saving Flag. Tier allocations remain in server profiles.
- [`growth_1573-1636.html`](growth_1573-1636.html): server and player comparisons between the 23 September and 8 October 2026 saved snapshots, including overload-stage progression and compact saving signals.
- [`player_impact_1573-1636.html`](player_impact_1573-1636.html): strongest 50 tracked players per server, model influence, and one-player-at-a-time rank sensitivity.
- [`resource_saving_1573-1636.html`](resource_saving_1573-1636.html): daily-history saving signals for all 22,485 current players, a server watchlist, and the method and data-quality details behind each flag.
- [`mega_alliance_1616.html`](mega_alliance_1616.html): server 1616 Top 100 Mega Alliance with 70% THP and 30% uploaded season-point percentiles, alliance composition, and a reallocation scenario for NvSP, NvEM and WaE.

The old `1605-1668` filenames redirect to the corrected group, preserving existing links and player-selection query strings.

## Publication

GitHub Pages publishes `main` from `/(root)`. The root [`CNAME`](CNAME) records `lw-warzone-intel.caiovlf.com`; `.nojekyll` is retained.

## Model and data

The 64-server group has a **fixed allocation of 16 Limited Open, 32 Semi-Open, and 16 Fully Open**. Within the model, rank #1 is strongest: ranks 1–16 fill Limited, 17–48 Semi, and 49–64 Fully. The model ranks servers using equal weights for within-group percentiles of their top-10 and top-50 players' average hero power. A server crossing a state boundary displaces another, so the counts remain fixed on both dates.

The historical transfer record for the preceding **1509–1572** group comes from the supplied Excel workbook's *Warzone Scoring* and *Server Strength* sheets. Its 7 September point distribution provides the point proxy. The historical August top-three alliance ranking reproduced 50 of its 64 observed September labels. An older-group backtest of the point proxy had a mean absolute error of about 382 points; the point forecast and its headroom are rough estimates, especially near cutoffs. The game's actual Warzone Score formula and future cutoffs are unavailable.

The current 8 October figures use [LWServers rankings](https://lwservers.com/data/snapshots/1573-1700/rankings.json?v=2026-10-08T04%3A04%3A00.395Z) and per-server player JSON. The growth comparison uses 23 September files saved locally at that date. The API's `v=` value is a cache-busting query parameter, not a historical archive; requesting the September URL today may return newer data. Both snapshots are embedded in these static HTML files, and the site does not update automatically.

Player growth is matched by UID across all 128 servers in the API segment. A server's tracked hero-power change includes retained players and roster arrivals or departures. The player page's solo growth room changes one player's hero power at a time and re-ranks all 64 servers; percentages for different players cannot be added. The outlook page's point growth room is a separate proxy based on estimated points, so the two measures can differ.

Saving signals compare robust hero-power growth slopes over 30 August–27 September and 27 September–7 October using locally saved LWS Pro daily-history responses. A strong slowdown with recent kills or overload activity is labeled “Possible saving”; it is not proof of held resources. All 22,485 current players have a saved response. The page distinguishes low prior growth, missing hero values within the window, and absent daily rows. Server flags weight the strongest 50 players by their modeled strength contribution. These flags do not alter the strength ranking or projected transfer state.

Growth also shows overload-stage changes between the two snapshots. Stage zero is treated as unrecorded because the API can use it as a placeholder. A server's overload gain totals players retained in that server who have positive stages on both dates. Overload is shown for context and is not part of the Warzone Score proxy.

The Mega Alliance view uses the saved 8 October server 1616 roster, historical THP growth within 3 August–7 October, and three uploaded season defeat-score lists (NvSP, NvEM and WaE). Scores earned across lists are summed by player UID; explicit user-confirmed row matches distinguish the two Kalelothran players. Actual alliance uses the separate Alliance field, confirmed corrections, then saved API/history origin. Blāze is confirmed as WaE.

The fit score is 70% THP percentile and 30% summed season-point percentile among scored eligible players. Total kills are context only and carry zero weight. The first 100 form the Mega Alliance: 52 NvSP, 17 NvEM, 29 WaE and 2 ECK0. Participation is each player's points divided by all uploaded points, including unresolved points; High/Medium/Low performance uses season-point percentile thirds. Missing scores are not imputed as zero. Eligibility still requires positive historical THP growth.

Reallocation retains those 52 NvSP players and adds the other 48. The second selection for NvEM contains 69 eligible scored players (20 NvSP, 26 WaE, 23 NvEM); 31 seats remain pending. Starting occupancy and reserve flows are planning assumptions, not verified current rosters: NvSP 52 after clearing nonselected members, NvEM supplied base 89, WaE 93 distinct uploaded identities versus the user-confirmed minimum 87. The original OCR missing-tag metadata is unavailable. The provisional reserve scenario can exceed WaE capacity and is explicitly labeled as requiring reconciliation. Downloadable CSVs contain the Top 100, second selection, named transfers and 36 identifiable NvSP releases.

Fixed tier allocations describe allowed intake by state, not vacant seats. Confirm the game's final classification and available seats in the transfer screen.


## Integrated Season 4 growth

Saving Signals now contains the Season 4 analysis in its Every tracked player table. Default mode is Season 4, with pre-season pace, baseline consistency, whole-season and recent pace, compact weekly ratios, the first persistent slow week, and a weekly chart on player selection. The same table can switch to the rolling analysis used by server flags. The former Season 4 filename redirects to Saving Signals and preserves server selection.

The season start is estimated as 7 September from the user reporting day 32 on 8 October for server 1616. Other servers use this date only as an explicit exploratory assumption. The pre-season reference is 8 August–6 September, the whole-season window is 7 September–7 October and the recent window is 27 September–7 October. Persistence requires two consecutive complete season weeks at no more than 75% of reference pace and a recent ratio no more than 75%. Baseline stability uses the median absolute deviation of at least three pre-season weekly rates divided by their absolute median, with a 35% cutoff. Saving candidates additionally require stable baseline, recent ratio at most 50%, and recent kills or overload growth. Partial week 5 does not establish persistence. These are planning signals, not proof of saved resources.

The 8 October refresh fetched all 128 server player snapshots in the segment and 22,491 history responses for 22,485 current players plus six September-only UIDs. Last complete history day is 7 October. The uploaded season point CSVs remain those provided on 7 October; they are not refreshed by the API. Tokens and raw histories are not published.
