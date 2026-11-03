# HOCO HUB Multi-Brand Store — v2

## What's included
- Premium dark storefront
- Brand filters (HOCO, Oraimo, Baseus, Anker demo entries)
- Search, category filter, price sorting
- Cart and checkout form preview
- Admin catalogue UI: add, edit, delete products
- Export/import product catalogue as JSON
- Responsive layout for mobile and desktop

## Important limitations
This is a front-end prototype. Admin changes are saved only in the current browser using localStorage. They do not sync across devices or browsers. There is no secure admin login, database connection, payment processing, order submission, stock synchronization, or customer notification yet. The checkout form is deliberately a demo and does not transmit customer information.

Do not use this prototype to collect real customer information or accept real orders until a backend, authentication, database policies and secure order flow are implemented and tested.

## Preview
Open `index.html` in a browser.

## Deploy static preview to Cloudflare Pages
1. Create a GitHub repository and upload `index.html`.
2. In Cloudflare Dashboard, go to Workers & Pages → Create → Pages → Connect to Git.
3. Select the repository. No build command is needed; set output directory to `/`.
4. Deploy. Cloudflare will issue a `*.pages.dev` URL if available.

## Next production steps
1. Create a Supabase project.
2. Add product, order and order-item tables, with carefully designed Row Level Security.
3. Add Supabase Auth for an owner/admin login. Never rely on a hidden frontend route or shared browser password for security.
4. Use a server-side function / Edge Function for order creation and validate prices from the database (never trust browser totals).
5. Connect image storage and upload real product photos.
6. Add delivery fee, payment methods, privacy notice, terms, returns policy and contact details.
7. Test on mobile and desktop before publishing.
