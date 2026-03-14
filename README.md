# hackthon-project
# Rafrance / CoreInventory

**CoreInventory** — lightweight inventory management UI built during a hackathon. This repository contains a single-page React app (Vite) and a wireframe mockup used as the visual reference.

---

## Live preview / mockup

I used an interactive canvas mockup as the reference for the UI layout and flows. See the uploaded file: `coreinventory_canvas_mockup.html` for the wireframe and flow diagrams. fileciteturn0file0

---

## Goals

* Fast, focused inventory workflows for small warehouses
* Clear flows for: login → dashboard → receipts → deliveries → transfers → adjustments
* Minimal, component-driven UI using Tailwind + small utility components
* Local state managed with Zustand for predictable state across routes

---

## Key features

* Authentication (Login page)
* Dashboard with KPIs and stock movement chart
* Product listing with quick create slide-over
* Receipts (incoming) flow with validation
* Delivery orders (outgoing) flow with pick/pack/validate steps
* Internal transfers and stock adjustments with audit log
* Settings area for warehouses, categories and profile

---

## Tech stack

* **Framework / Bundler:** Vite + React (JSX)
* **Styling:** Tailwind CSS + PostCSS
* **State management:** Zustand
* **Tooling / scripts:** Node / npm

---

## Project structure

```
rafance-coreinventory/
├── index.html              ← the ONE html file
├── package.json            ← list of packages to install
├── vite.config.js          ← build tool config
├── tailwind.config.js      ← CSS framework config
├── postcss.config.js       ← CSS processor config
└── src/
    ├── main.jsx            ← JavaScript entry point
    ├── App.jsx             ← all URL routes
    ├── index.css           ← global styles
    ├── store/
    │   └── index.js        ← all global data (Zustand)
    ├── components/
    │   ├── layout/
    │   │   └── AppShell.jsx ← sidebar + layout
    │   └── ui/
    │       └── index.jsx   ← reusable components
    └── pages/
        └── Login.jsx       ← the login page
```

> The structure above matches the hackathon deliverable and the wireframe used in the mockup. If you add more pages or features, list them here.

---

## Getting started (development)

1. Clone the repo

```bash
git clone <your-repo-url> rafance-coreinventory
cd rafance-coreinventory
```

2. Install dependencies

```bash
npm install
```

3. Run the dev server

```bash
npm run dev
```

4. Open `http://localhost:5173` (or the address printed by Vite) in your browser.

If you want to view the wireframe mockup locally, open `coreinventory_canvas_mockup.html` in a browser — it’s an interactive canvas that documents flows and screens. fileciteturn0file0

---

## Build for production

```bash
npm run build
npm run preview  # to preview the production bundle locally
```

---

## Development notes / conventions

* **Components:** small, focused, and reusable. `components/ui/index.jsx` exports primitive building blocks (Button, Input, Badge, Card).
* **Layout:** `AppShell.jsx` owns the sidebar and top-level layout so pages can focus on content.
* **State:** keep UI-local state in components, cross-route/shared state in `store/index.js` (Zustand). Persist important state only when necessary.
* **Styling:** Tailwind utility classes in components. Use `index.css` for base styles and shared utilities.

---

## Design decisions (short)

* Single-page React app for quick iteration during the hackathon.
* Zustand chosen to avoid Redux boilerplate for a small project.
* Minimal components prioritized for speed of delivery and clarity.

---

## Sample data & testing

* Add a `/data` folder (optional) with JSON fixtures for products, receipts and deliveries.
* For quick manual testing, create a seed script that populates the `store` with sample products and transactions.

---

## TODO / Roadmap

* Add authentication backend (JWT / OAuth) and real API integration
* Persist data to a simple backend (Express / Supabase / Firebase)
* Add unit tests and E2E tests (Jest + Playwright)
* Improve responsive behavior for small screens
* Add import/export (CSV) for products and stock counts

---

## Contributing

1. Fork the repo
2. Create a branch: ``
3. Open a PR with a clear description and screenshots

---

