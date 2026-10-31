# THE ANNA.EX — India's Flavour Exchange

A stock-market-inspired, single-restaurant ordering prototype. Dish prices respond to recent demand within a configured 90%–110% band around each dish’s base price.

## Live prototype

https://pranavrathi-4575.github.io/THE-ANNA.EX/

## Current features

- Customer sign-up and sign-in through Supabase Auth using email and password.
- Shared market feed for the restaurant's listed dishes, currently seeded with 11 sample listings.
- Demand-based dish pricing calculated by the backend over a rolling 30-minute window, with a 90%–110% base-price band.
- Menu search, category filters, basket and demo-order checkout.
- Order history for the signed-in customer.
- Merchant sign-in with restaurant-membership checks.
- Merchant order dashboard with controlled order-status transitions.
- Customer-facing order status and progress display.
- About, contact, FAQ and policy information pages.

## Current operating model

- Single-restaurant prototype using the restaurant slug `anna-ex-market`.
- Proposed fulfilment model: customer self-pickup.
- No home-delivery service is currently provided.
- Checkout creates an unpaid demo order. No payment gateway or payment collection is connected.
- Phone-number OTP verification is not currently implemented. Customer accounts use email-based authentication.
- The website is a demonstration prototype, not yet a live commercial ordering service.

## Technology

- Front end: HTML, CSS and vanilla JavaScript.
- Authentication, database and backend functions: Supabase.
- Hosting: GitHub Pages.

The browser uses a Supabase publishable key. Never put a Supabase service-role key, database password or other secret in frontend code or commit it to this repository.

## Known prototype limitations

- The market chart is illustrative, not a historical price chart.
- Demo checkout creates unpaid test records; order-status changes are simulations and do not trigger kitchen preparation or pickup.
- Current menu entries are sample data and must be replaced or approved by a participating restaurant before any pilot.
- Public-facing counts are populated from the connected restaurant menu after the market feed loads.

## Before accepting real customer orders

Complete and test the following before treating the site as a production service:

1. Onboard a restaurant and confirm its menu, prices, availability and pickup process.
2. Agree on who controls dish availability, pricing limits, order acceptance and cancellations.
3. Integrate a payment provider and implement verified payment states, failure handling and refunds.
4. Add phone verification only if it is genuinely needed for the restaurant's workflow.
5. Review Supabase Row Level Security policies, database functions, authentication settings and access permissions.
6. Test customer and merchant journeys on mobile and desktop, including invalid inputs, duplicate submissions, network failures and simultaneous orders.
7. Establish customer-support, privacy, retention, food-information and applicable legal/compliance processes.
8. Run a limited pilot and measure order completion, repeat usage, customer response to price changes and restaurant workload.

## Development

This is a static front end; no local build step is required. Open `index.html` in a browser for layout inspection. Backend-connected features require the configured Supabase project and its database schema/functions.

Do not use real customer data or accept real payments through the prototype until the production-readiness checks above are completed.
