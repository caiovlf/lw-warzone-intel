# Last War Warzone Intel

A static, English-language transfer outlook for Last War servers **1605–1636** and **1637–1668**. The site is self-contained and works without a backend or build step.

## Pages

- [`index.html`](index.html) — entry point for GitHub Pages, showing the transfer outlook.
- [`transfer_outlook_1605-1668.html`](transfer_outlook_1605-1668.html) — server rankings, projected opening states, seat allocations, Warzone Points estimates, and point-based growth room.
- [`player_impact_1605-1668.html`](player_impact_1605-1668.html) — top 50 tracked players on each requested server, model influence, and solo player-growth scenarios.

## GitHub Pages

The site entry point is `index.html`. The custom domain `lw-warzone-intel.caiovlf.com` is recorded in the root [`CNAME`](CNAME) file. GitHub Pages should publish from **`main`** and **`/(root)`**.

[GitHub's custom-domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) explains DNS and HTTPS certificate setup.

## Data and interpretation

The snapshot is dated **23 September 2026**. The historical classifications, Warzone Points, thresholds, and seat rules come from the supplied *Copy of Coordinates List Tools by Wolfy and Team.xlsx* workbook, using its **Warzone Scoring** and **Server Strength** sheets. Current player and server figures come from [LWServers rankings](https://lwservers.com/data/snapshots/1573-1700/rankings.json?v=2026-09-23T04%3A02%3A35.142Z) and per-warzone [player snapshots](https://lwservers.com/data/snapshots/1573-1700/players/1616.json?v=2026-09-23T04%3A02%3A35.142Z).

The model ranks servers within their full 64-server scoring cohorts: 1573–1636 and 1637–1700. It gives equal weight to the within-cohort percentile ranks of the top-10 and top-50 players' average hero power. Projected categories use the 16 Fully Open / 32 Semi-Open / 16 Limited Open split observed in the historical data. Numeric points are mapped from comparable historical ranks onto the July transfer scale.

The player page's **solo growth room** increases one player's hero power at a time and recomputes all 64 rankings until that server's modeled category changes. Every row is a separate scenario; growth percentages for different players cannot be added. The outlook page's **point-based growth room** uses historical category thresholds, so the two measures can differ near a boundary.

These are independent estimates. The game's Warzone Score formula, next transfer standards, future cohort assignment, and current unfilled seats are unavailable. The fixed tier numbers describe historical category allocations, not open vacancies. The pages contain a dated snapshot and do not update automatically.

