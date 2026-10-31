# THE ANNA.EX — India's Food Exchange

A dark, stock-market-inspired food marketplace prototype. Demand-based pricing is calculated from the number of units sold per dish in a rolling 30-minute window.

## Run locally
Open `index.html` in a modern browser. No build step is required.

## Demo features
- Market overview with index, dish prices, percentage movement and recent trade activity.
- Ten sample dishes with category filters and search.
- Basket and demo checkout. Prices are recorded on each order and remain locked.
- Customer order lookup on the same browser.
- Restaurant demo dashboard with order status controls.

## Demo owner login
- Email: `owner@anna.ex`
- Password: `anna123`

## Pricing rules
- 0–1 units in the previous 30 minutes: -2%
- 2–3 units: 0%
- 4–5 units: +2%
- 6–8 units: +4%
- 9–11 units: +6%
- 12+ units: +8%

Market price is capped at 110% of the base price. The market index is the average percentage movement across the ten listed dishes.

## Important limitations
This is a front-end prototype. Data is stored in the current browser using localStorage, so it is not shared between customers or devices. Customer details and the owner demo login are not secure authentication. Checkout does not collect payment. A production launch needs a shared database, secure authentication, server-side price calculation, payment integration, order validation, and appropriate privacy/security controls.

## Publish with GitHub Pages
In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then save. GitHub Pages will provide the published site URL after deployment completes.
