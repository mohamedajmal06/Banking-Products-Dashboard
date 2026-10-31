# Banking Products Dashboard

A single-screen dashboard that shows savings accounts, credit cards, loans and wealth products in one unified view.

## Features
- Product cards with name, category, status, two key metrics and a call-to-action button
- Category tabs with counts, live search and a status filter
- Details dialog, with a "Start application" action for available products
- Responsive layout, light and dark mode, keyboard focus and reduced-motion support

## Technology
Plain HTML, CSS and vanilla JavaScript. No build step and no dependencies.

## Run it
Open `index.html` in a browser. To host it, enable GitHub Pages (Settings, then Pages, then deploy from the `main` branch).

## Structure
- **Data layer:** the `PRODUCTS` array and `fetchProducts()` in `index.html` act as a mock API. To use a real endpoint, replace the body of `fetchProducts()` with `fetch("/api/products").then(r => r.json())`.
- **UI layer:** `state` holds the category, search and status. `filtered()` applies them and `render()` draws the cards. Adding a product only needs a new data row.
