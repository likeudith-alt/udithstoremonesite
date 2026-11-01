# UDIYA STORE — Local Browser Demo

This project keeps the existing UDIYA STORE storefront and purple/neon styling. The customer account, wallet, deposit request, purchase history and admin customer tools have been switched to **browser localStorage** so the demo needs no DATABASE_URL, Neon, Supabase, Netlify Blobs, or other database.

## Important limitation — demo only

This is NOT a secure multi-customer wallet and MUST NOT be used to accept real deposits or sell products for real money.

- All data is stored in the browser/device that created it. Other customers, phones, browsers and computers do not share the same accounts or balances.
- Browser storage can be edited, cleared or lost by the user. There is no server-side identity, durable database, atomic transaction guarantee, or reliable protection against duplicate/concurrent purchases.
- The demo admin password is present in public JavaScript (`ChangeMe123!`) and is not secure. Anyone who inspects the site can bypass it.
- Passwords are hashed locally for this demo, but browser-side hashing does not make the account system secure.
- Deposit receipt images and product images are stored as browser data URLs and may exceed local storage limits. Use small images.
- A successful demo purchase changes only the current browser's local demo balance. It does not process or verify any actual payment.

Do not publish this as a real-money wallet. A production wallet needs a trusted backend and transactional persistent database.

## Run locally

1. Extract the ZIP.
2. Import the folder into GitHub.
3. In Netlify, choose **Add new site → Import an existing project** and connect the GitHub repository.
4. Build command: leave blank. Publish directory: `public`.
5. Deploy. No database environment variables are required for this demo.

You can also run `npm run dev` after installing dependencies.

## Demo admin

Open `/admin/` and use password `ChangeMe123!`. This password is public and only intended for local testing. Do not use it to protect a real admin panel.

## Reset demo data

Clear this site's browser localStorage to reset all demo accounts, balances, deposit requests and orders. This also deletes customer data on that browser.
