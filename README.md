
# Modern E-commerce Website – Next.js + Sanity + Stripe

This project is a fully functional e-commerce application built with *Next.js, **TypeScript, **Stripe, and **Sanity CMS*. It includes a product catalog, dynamic product pages, a shopping cart powered by React Context, and full payment integration using Stripe.

---

## 🛒 Key Features

- *Product Catalog from Sanity*:
  - Fetched via GROQ queries
  - Best-selling headphones featured on the homepage
- *Product Details Page*:
  - Image gallery with zoom
  - Quantity selector
  - Add to Cart functionality
  - Related product suggestions
- *Shopping Cart*:
  - Global state managed via React Context (context.tsx)
  - Cart total, item quantity, and state handlers included
- *Stripe Payment Integration*:
  - Secure checkout flow using Stripe Elements
  - Payment confirmation and webhook support
- *Sorting Functionality*:
  - Sort products by price (low to high / high to low)
- *Static Site Generation (SSG)*:
  - Product pages are statically generated using generateStaticParams
- *Modern UI*:
  - Built with Tailwind CSS and responsive by default

---

## 🛠 Tech Stack

- *Framework*: Next.js (App Router)
- *Language*: TypeScript
- *Styling*: Tailwind CSS
- *CMS*: Sanity.io
- *Payments*: Stripe
- *State Management*: React Context API

---

## 📁 Folder Structure

app/ ├── page.tsx                   → Homepage with product listing ├── context.tsx                → Shopping cart context ├── product/[slug]/page.tsx    → Product details page (SSG) ├── api/stripe/                → Stripe webhook & payment intent

comps/ ├── Home.tsx                   → Renders products + banners ├── Products.tsx               → Lists all products ├── Show.jsx                   → Displays a single product's details

lib/ ├── client.js                  → Sanity client setup

public/ ├── assets, logos, images...

styles/ ├── globals.css, Tailwind config

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/nextjs-ecommerce-sanity-stripe.git

# Install dependencies
npm install

# Set up environment variables (Stripe & Sanity)
cp .env.example .env.local

# Start development
npm run dev


---

🔐 Environment Variables

NEXT_PUBLIC_SANITY_PROJECT_ID=your_sanity_project_id
NEXT_PUBLIC_SANITY_TOKEN=your_sanity_token
STRIPE_SECRET_KEY=your_stripe_secret_key
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_public_key


---

🧠 Notes

Sanity is used as a headless CMS and fetches content server-side.

Stripe webhook support is included in api/stripe/webhook.

"Buy Now" is currently a placeholder button and can be customized.



---

📝 License

MIT — free to use and modify for personal or commercial use.
