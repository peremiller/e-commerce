# B20 Shop — e-commerce

A self-contained e-commerce storefront in a single `index.html` — no build step,
no dependencies, works offline. Live at **https://peremiller.github.io/e-commerce/**

Implements the `b20_ecommerce` database design (see [`sources/b20_ecommerce.sql`](sources/b20_ecommerce.sql)):

| SQL table | In the app |
|---|---|
| `categories` | Category filter chips in the Shop tab |
| `items` | Product catalog (name, price, description, image, category) |
| `orders` | Orders tab — 12-char `transaction_code`, purchase date, status, payment mode |
| `orders_items` | Line items (item, quantity, price at purchase) inside each order |
| `statuses` | Pending → Processing → Shipped → Delivered / Cancelled |
| `payment_modes` | Cash on Delivery, Credit/Debit Card, GCash, Bank Transfer |
| `users` | Account tab profile (name, username, email, delivery address) |

## Features

- 🛍 Product catalog with search + category filters, item detail view
- 🛒 Cart with quantity steppers and live total (₱)
- ✅ Checkout: delivery address + payment mode → order with transaction code
- 📦 Order history with status progression and cancellation
- 👤 Profile that prefills checkout; JSON export/import backup
- 📱 Mobile-first, automatic dark mode, all data in `localStorage`

## Run locally

Just open `index.html` in a browser — that's it.

## History

The original 2019 PHP/MySQL app was committed as a submodule pointer whose
source repository was never published, so only the SQL dump survived. This
rebuild reimplements the same schema as a static app that GitHub Pages can host.
