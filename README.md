Billing Software

A full-stack billing and invoicing web application built with React + Express.js + PostgreSQL. Supports real-time bill generation, product catalog management across categories, and Stripe payment integration with INR currency support.


Built as part of a full-stack development project — handles end-to-end billing workflow from product selection to payment processing.




🚀 Live Demo


(Add deployment link here — Replit / Render / Railway)




✨ Key Features


Real-time Bill Generation — totals update instantly as quantities change
Product Catalog — organized across 3 categories (Snacks, Grocery, Hygiene) with category-specific tax rates
Stripe Payments — secure INR checkout with payment intent API
Bill History — search and retrieve past bills by ID or bill number
Professional Invoice View — itemized breakdown with tax calculations
PostgreSQL Persistence — all bills saved and retrievable via REST API



🛠️ Tech Stack

LayerTechnologyFrontendReact 18, TypeScript, ViteUI ComponentsShadcn/ui, Radix UI, Tailwind CSSState / DataTanStack Query (React Query)FormsReact Hook Form + Zod validationRoutingWouterBackendExpress.js, Node.js (ESM)DatabasePostgreSQL + Drizzle ORMPaymentsStripe (INR currency)AuthPassport.js + Express Sessions


⚙️ How to Run Locally

Prerequisites


Node.js 18+
PostgreSQL database (or Neon serverless)
Stripe account (for payment features)


Setup

bash# Clone the repository
git clone https://github.com/akleshsoni/billing-software.git
cd billing-software

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Fill in: DATABASE_URL, STRIPE_SECRET_KEY, VITE_STRIPE_PUBLIC_KEY

Database

bash# Push schema to database
npm run db:push

Run

bash# Development (with hot reload)
npm run dev

# Production build
npm run build
npm start

Visit: http://localhost:5000


🔌 API Endpoints

MethodEndpointDescriptionGET/api/billsGet all billsGET/api/bills/:idGet bill by IDGET/api/bills/number/:billNumberGet bill by numberPOST/api/billsCreate new billPUT/api/bills/:idUpdate billDELETE/api/bills/:idDelete billPOST/api/create-payment-intentInitiate Stripe payment


🏗️ Architecture

billing-software/
├── client/               # React frontend (Vite)
│   └── src/
│       ├── components/   # CustomerDetails, ProductCategory, BillArea, BillingSummary
│       └── pages/        # Billing, Checkout, Payment Success
├── server/               # Express backend
│   ├── index.ts
│   └── routes.ts
├── shared/
│   └── schema.ts         # Drizzle ORM schema (Bills, Products)
├── package.json
└── drizzle.config.ts


🔑 Environment Variables

envDATABASE_URL=postgresql://...
NODE_ENV=development
STRIPE_SECRET_KEY=sk_...
VITE_STRIPE_PUBLIC_KEY=pk_...


📸 Screenshots


<img width="1919" height="1016" alt="Screenshot 2025-03-29 104610" src="https://github.com/user-attachments/assets/b5e66859-0e62-4ade-aafe-51f0ef21da4d" />





👤 Author

Aklesh Soni — Final-year CS Engineering Student

📧 akleshsoni37@gmail.com | 🌐 akleshsoni.netlify.app
