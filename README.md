# helix-web

Helix dashboard web app — charts, alerting rules UI, and workspace settings.

## Stack
React + TanStack Query. Charts are responsive with a pinch-to-zoom fallback on small screens.

## Performance
Dashboard p95 target < 800ms; feature-flag evaluation is cached for 60s in-process.
