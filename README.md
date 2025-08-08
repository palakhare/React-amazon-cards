# Amazon-style Product Cards (React)

A small, reusable React component set and demo showing **Amazon-style product listing cards** — ideal for product grids, marketplaces, and e‑commerce UI prototypes. The components are lightweight, responsive, and easy to plug into any React app or showcase in a GitHub repo.

---

## 🚀 Features

* Clean, responsive product card layout (image, title, brand, price, rating, badges).
* Supports variants: compact grid card, detailed list card, and horizontal card.
* Optional elements: `Prime` badge, `Old Price` / discount, star rating, review count, CTA buttons.
* Accessible markup (ARIA labels, keyboard focusable buttons) and semantic HTML.
* Easy theming via CSS variables or Tailwind utility classes.
* Tiny footprint — focuses on UI only (no cart or backend logic included).

---

## 🧩 Tech Stack

* React (hooks)
* CSS / Tailwind-ready styles
* Prop-driven components (no external state)

---

## 📦 Installation

1. Clone the repo or copy the component files into your project.

```bash
git clone <your-repo-url>
cd amazon-cards-react
npm install
npm start
```

2. Or install as local component in an existing React app.

---

## ⚙️ Usage

Import the card and pass a `product` object and optional callbacks.

```jsx
import ProductCard from "./components/ProductCard";

const product = {
  id: "B07EXAMPLE",
  title: "Wireless Bluetooth Headphones",
  brand: "Acme Audio",
  image: "/images/headphones.jpg",
  price: 49.99,
  oldPrice: 79.99,
  rating: 4.5,
  reviews: 1245,
  prime: true,
  features: ["40h battery", "Active noise-canceling"],
};

<ProductCard
  product={product}
  onAddToCart={(p) => console.log("add", p.id)}
  onWishlist={(p) => console.log("wishlist", p.id)}
/>
```

### Props

* `product` **(required)** — object with `id`, `title`, `brand`, `image`, `price`, optional `oldPrice`, `rating`, `reviews`, `prime`, `features`.
* `onAddToCart(product)` — callback when Add to Cart clicked.
* `onWishlist(product)` — callback when Wishlist/Save clicked.
* `variant` — one of `'grid' | 'list' | 'horizontal'` (default: `'grid'`).
* `className` — extra CSS classes to style the root card.

---

## 🎨 Theming & Styling

* The demo uses plain CSS variables; swap in Tailwind classes if you prefer.
* Variables provided: `--card-bg`, `--card-border`, `--accent`, `--muted`.
* Use `variant` prop for quick layout changes.

---

## ♿ Accessibility

* Images include `alt` text.
* Buttons have `aria-label` attributes.
* Keyboard order follows visual order; interactive regions are focusable.

---

## 🧪 Tests

No heavy test suite included — feel free to add unit tests (React Testing Library / Jest) for interaction callbacks and snapshot tests.

---

## 📸 Screenshots

Include screenshots in `/assets` and link them in your README to show grid/list/horizontal layouts.

---

## 🤝 Contribute

PRs welcome — open issues for feature requests (lazy load images, server-side pricing, currency formatting, i18n).

---

## 📄 License

MIT © Your Name

---

If you want, I can also generate:

* a short repository description (one-liner) for GitHub's repo description field,
* a `ProductCard` single-file React component example,
* or a demo-ready `index.html` + `index.jsx` you can drop into a CodeSandbox.

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
