# Code_alpha_project_ecommerce_site-
# 🍫 ChocoLuxe — Chocolate E-Commerce Website

A full-stack e-commerce web app for browsing and ordering premium chocolates and gift hampers, built with **Next.js**, **TypeScript**, **PostgreSQL**, and **Drizzle ORM**.

## Features

- 🛍️ **Product Catalog** — browse chocolates and gift hampers from brands like Lindt, Godiva, Ferrero Rocher, Toblerone, and more
- 🛒 **Shopping Cart** — add products to cart and manage quantities
- 🔐 **Authentication** — user registration, login, and session-based auth
- 📦 **Order Management** — place orders and view order history
- 🎨 **Responsive UI** — built with Tailwind CSS
- 🗄️ **PostgreSQL Database** — schema and queries managed with Drizzle ORM

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Next.js](https://nextjs.org/) 16 (App Router) |
| Language | TypeScript |
| Database | PostgreSQL |
| ORM | Drizzle ORM |
| Styling | Tailwind CSS |
| Auth | Custom JWT-based auth (`jose`, `bcryptjs`) |

## Project Structure

```
src/
├── app/
│   ├── api/
│   │   ├── auth/          # login, register, logout, current user
│   │   ├── orders/        # order creation & retrieval
│   │   └── health/        # health check endpoint
│   ├── cart/               # cart page
│   ├── login/ register/    # auth pages
│   ├── orders/              # order history page
│   ├── products/[id]/      # product detail page
│   └── page.tsx             # homepage
├── components/              # Navbar, ProductCard, ProductGrid, CartProvider, etc.
├── db/
│   ├── schema.ts            # Drizzle schema (users, products, orders, order_items)
│   └── index.ts              # DB connection
└── lib/
    ├── auth.ts               # auth helpers
    ├── cart.ts               # cart logic
    └── seed.ts                # database seed script
```

## Getting Started

### Prerequisites

- Node.js 18+
- A running PostgreSQL instance

### 1. Clone the repository

```bash
https://github.com/Laiyba1609/Code_alpha_project_ecommerce_site-/tree/main
cd <code_alpha_project_ecommerce_site>
```

### 2. Install dependencies

```bash
npm install
```
### 3. Set up the database

Push the schema to your database:

```bash
npx drizzle-kit push
```

Seed sample products:

```bash
npx tsx src/lib/seed.ts
```

### 4. Run the development server

```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to view the app.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Build for production |
| `npm run start` | Start the production server |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | Run TypeScript type checking |

## Database Schema

- **users** — id, name, email, password hash
- **products** — id, name, brand, category (chocolate/hamper), description, price, image, stock, featured, country
- **orders** — id, user, customer info, address, total, status
- **order_items** — line items linking orders to products

## License

This project is available for personal and educational use. Add your preferred license here (e.g., MIT).

---

Built with 🍫 and Next.js.
