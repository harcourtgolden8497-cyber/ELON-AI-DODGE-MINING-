# 🚀 OFFICIAL ELON DOGE MINING SAAS PLATFORM

A production-ready **AI-powered SaaS dashboard platform** built with Next.js 14.

This system is designed as a **scalable analytics + simulation SaaS application** with authentication, billing, AI assistant, and enterprise-grade architecture.

---

## 🌐 Live Demo
https://officialelondogemining.live

---

## 🧠 Overview

OFFICIAL ELON DOGE MINING SAAS PLATFORM is a modern SaaS dashboard system that provides:

- AI-powered assistant for user guidance
- Real-time analytics dashboard simulation
- Subscription-based monetization system
- Multi-tenant SaaS architecture
- Enterprise-ready deployment structure

---

## ⚙️ Tech Stack

- Next.js 14 (App Router)
- TypeScript
- TailwindCSS
- Prisma ORM
- PostgreSQL / SQLite (dev)
- NextAuth authentication
- Stripe payments integration
- OpenAI API integration
- Recharts (analytics)

---

## ✨ Features

- 🔐 Secure authentication (NextAuth)
- 📊 Real-time dashboard analytics
- 🤖 AI assistant integration
- 💰 Subscription billing system (Stripe)
- 🧾 Invoice generation system
- 📈 Referral & affiliate system
- 🧑‍💼 Admin control panel
- 🌍 Multi-tenant SaaS architecture
- ⚡ Live simulation engine
- 📱 Responsive mobile-first UI

---

## 💰 Pricing Plans

### 🟡 Starter Plan
$1,888 – $60,888 / year
- Basic dashboard access
- AI assistant (limited usage)
- Standard analytics
- Single workspace
- Email support

---

### 🔵 Pro Plan
$70,888 – $160,888 / year
- Full dashboard access
- Advanced analytics engine
- Expanded AI assistant usage
- Multi-user workspace
- API access
- Priority support

---

### 🟣 Elite Plan
$200,888+ / year
- Enterprise SaaS license
- Custom deployment setup
- Dedicated infrastructure
- White-label licensing option
- Dedicated support engineer
- Unlimited scaling (contract-based)

---

## 🔐 Environment Variables

Create a `.env.local` file:

```env
DATABASE_URL=your_database_url

NEXTAUTH_SECRET=your_secret_key
NEXTAUTH_URL=http://localhost:3000

STRIPE_SECRET_KEY=your_stripe_secret
STRIPE_WEBHOOK_SECRET=your_webhook_secret

OPENAI_API_KEY=your_openai_api_key
git clone https://github.com/your-username/elon-doge-mining.git
cd elon-doge-mining
npm install
npm run dev
npm run build
npm start

[build]
  command = "npm run build"
  publish = "netlify"

[[plugins]]
  package = "@netlify/plugin-nextjs"
elon-doge-mining/
/my-saas-app
 ├── /public
 ├── /src
 ├── /netlify
 │    └── /functions   (serverless backend)
 ├── netlify.toml
 ├── package.json
 ├── .env.example
 └── README.md
│
├── app/
│   ├── page.tsx
│   ├── dashboard/page.tsx
│   ├── pricing/page.tsx
│   ├── wallet/page.tsx
│   ├── api/
│       ├── ai/route.ts
│       ├── payment/stripe.ts
│       ├── binance-pay/route.ts
│
├── components/
│   ├── Doge3D.tsx
│   ├── Navbar.tsx
│   ├── PricingCard.tsx
│   ├── AIChat.tsx
│
├── lib/
│   ├── i18n.ts
│   ├── supabase.ts
│
├── styles/
├── public/
├── .env.local
├── package.json


🧠 MASTER BLUEPRINT — SYSTEM OVERVIEW
🏗️ CORE STACK
Plain text
Frontend:   Next.js (React UI + Dashboard + Admin Panel)
Auth:       NextAuth (GitHub Login)
Database:   Supabase (PostgreSQL)
Payments:   Binance Pay (Manual + Webhook verification)
Hosting:    Netlify
Backend:    Next.js API Routes (Serverless Functions)
🔐 1. AUTHENTICATION LAYER (NEXTAUTH)
Flow:
User clicks “Login with GitHub”
NextAuth redirects to GitHub OAuth
GitHub returns user session
Session stored via JWT
User gains access to dashboard
Core Files:
Plain text
/pages/api/auth/[...nextauth].js
/pages/index.js
Env:
Plain text
GITHUB_ID
GITHUB_SECRET
NEXTAUTH_SECRET
NEXTAUTH_URL
🗄️ 2. DATABASE LAYER (SUPABASE)
Tables:
USERS
SQL
id (uuid)
email (text)
plan (free / starter / pro / elite)
balance (numeric)
mining_active (boolean)
created_at
PAYMENTS
SQL
id (uuid)
email (text)
order_id (text)
amount (numeric)
status (pending / paid / failed)
created_at
Supabase Role:
Store users
Track payments
Control access levels
Persist mining status
Power admin analytics
💳 3. PAYMENT SYSTEM (BINANCE PAY)
Flow:
User selects plan
System generates order ID
Redirect to Binance Pay
User completes payment
Webhook verifies payment
Supabase updates user access
Key Components:
Create Order API
Plain text
/pages/api/binance/create-order.js
Webhook Listener
Plain text
/pages/api/binance/webhook.js
Verify Payment API
Plain text
/pages/api/binance/verify.js
Payment States:
Plain text
PENDING → PAID → USER UNLOCKED
🔥 4. MINING SIMULATION ENGINE
Purpose:
Simulates real-time mining activity (SaaS gamification layer)
Logic:
Plain text
Hash Rate fluctuates
Balance increases per second
Speed depends on plan tier
File:
Plain text
/lib/miningEngine.js
Output:
Hash Rate (MH/s or TH/s)
Balance (DOGE units)
Live updates every second
📊 5. ANALYTICS DASHBOARD (ADMIN CORE)
Features:
KPI Cards:
Total Revenue
Active Miners
Pending Withdrawals
Total Hash Power
Live Systems:
Revenue Chart (bar graph)
Binance Pay activity feed
User table management
UI Component:
Plain text
ElonDogeMiningAnalyticsUI (React Dashboard)
👥 6. USER MANAGEMENT SYSTEM
Features:
View users
View plans
Suspend users
Track earnings
Monitor mining status
Actions:
Plain text
View
Suspend
Upgrade plan
Check earnings
🔓 7. ACCESS CONTROL SYSTEM
Logic:
Plain text
IF user.plan == "free"
→ Block dashboard

IF user.mining_active == false
→ Show upgrade page

IF payment.status == "paid"
→ Unlock dashboard
💰 8. PLAN SYSTEM (SAAS MONETIZATION)
Pricing Tiers:
Plain text
Starter → $1,888 – $60,888
Pro     → $70,888 – $160,888
Elite   → $200,888+
Access Mapping:
Plan
Features
Starter
Basic mining simulation
Pro
Higher hash rate
Elite
Full dashboard + admin access
🔔 9. BINANCE WEBHOOK SYSTEM
Flow:
Plain text
Binance Pay → Payment Sent
        ↓
Webhook Triggered
        ↓
Verify Payment
        ↓
Update Supabase
        ↓
Unlock User
Core File:
Plain text
/pages/api/binance/webhook.js
🚀 10. DEPLOYMENT LAYER (NETLIFY)
Configuration:
TOML
[build]
command = "npm run build"
publish = ".next"

[[plugins]]
package = "@netlify/plugin-nextjs"
Hosting Flow:
Plain text
GitHub → Netlify → Production Site
🔐 11. ENVIRONMENT VARIABLES (FULL LIST)
Plain text
# AUTH
GITHUB_ID
GITHUB_SECRET
NEXTAUTH_SECRET
NEXTAUTH_URL

# SUPABASE
SUPABASE_URL
SUPABASE_ANON_KEY
SUPABASE_SERVICE_ROLE_KEY

# BINANCE PAY
BINANCE_PAY_API_KEY
BINANCE_PAY_SECRET_KEY
BINANCE_MERCHANT_ID
🧭 FULL SYSTEM FLOW (END-TO-END)
USER JOURNEY:
Plain text
1. Visit site
2. Login with GitHub
3. Go to Pricing page
4. Select Binance Pay plan
5. Pay via Binance
6. Webhook verifies payment
7. Supabase updates account
8. Dashboard unlocked
9. Mining simulation starts
10. Analytics dashboard updates
🧠 SYSTEM ARCHITECTURE MAP
Plain text
┌──────────────┐
            │  Frontend UI │
            │ (Next.js)    │
            └──────┬───────┘
                   │
     ┌─────────────┼─────────────┐
     │                           │
┌────────────┐           ┌──────────────┐
│ NextAuth   │           │ Binance Pay  │
│ GitHub OAuth│          │ Payments     │
└──────┬─────┘           └──────┬───────┘
       │                        │
       ▼                        ▼
┌────────────────────────────────────┐
│          SUPABASE DATABASE        │
│ Users | Payments | Plans | Logs   │
└────────────────────────────────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Analytics Dashboard│
        │ Admin Control Panel │
        └────────────────────┘
⚠️ IMPORTANT PRODUCTION NOTES
✔ Use RLS (Row Level Security) in Supabase
✔ Validate Binance webhook signatures
✔ Never expose service_role key
✔ Protect admin routes
✔ Log all payment events
🚀 WHAT YOU NOW HAVE
You now have a full SaaS-grade system blueprint with:
Authentication system
Payment system (Binance Pay)
Database backend
Live mining simulation engine
Admin analytics dashboard
User management system
Netlify deployment pipeline
🔥⚡ REAL-TIME SYSTEM UPGRADE (ELON DOGE MINING)
You are now adding:
🔴 Live user updates
🔴 Live payments feed
🔴 Live mining balance updates
🔴 Admin dashboard real-time sync
🔴 No refresh needed
🧠 CORE IDEA
Instead of this:
Plain text
User refreshes page → sees new data
You now get:
Plain text
Database changes → instantly pushed → UI updates live
🗄️ 1. ENABLE SUPABASE REALTIME
Go to Supabase:
Plain text
Database → Replication
Enable for tables:
users
payments
⚙️ 2. INSTALL SUPABASE CLIENT (FRONTEND)
Bash
npm install @supabase/supabase-js
🔌 3. CREATE REALTIME CLIENT
/lib/supabaseClient.js
JavaScript
import { createClient } from "@supabase/supabase-js";

export const supabase = createClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL,
  process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY
);
🔴 4. LIVE PAYMENTS FEED (BINANCE ACTIVITY)
This makes your admin panel update instantly when payments arrive.
Add to Analytics UI:
JavaScript
import { useEffect, useState } from "react";
import { supabase } from "../lib/supabaseClient";

export default function LivePayments() {
  const [payments, setPayments] = useState([]);

  useEffect(() => {
    // initial load
    const load = async () => {
      const { data } = await supabase
        .from("payments")
        .select("*")
        .order("created_at", { ascending: false });

      setPayments(data);
    };

    load();

    // REALTIME LISTENER
    const channel = supabase
      .channel("payments-channel")
      .on(
        "postgres_changes",
        {
          event: "*",
          schema: "public",
          table: "payments",
        },
        (payload) => {
          setPayments((prev) => [payload.new, ...prev]);
        }
      )
      .subscribe();

    return () => supabase.removeChannel(channel);
  }, []);

  return (
    <div>
      <h2>🔴 Live Binance Pay Activity</h2>

      {payments.map((p) => (
        <div key={p.id} style={{ padding: 10, borderBottom: "1px solid #333" }}>
          <p>Order: {p.order_id}</p>
          <p>Amount: ${p.amount}</p>
          <p>Status: {p.status}</p>
        </div>
      ))}
    </div>
  );
}
🔥 5. LIVE USER UPDATES (AUTO DASHBOARD SYNC)
/pages/dashboard.js
JavaScript
import { useEffect, useState } from "react";
import { supabase } from "../lib/supabaseClient";
import { useSession } from "next-auth/react";

export default function Dashboard() {
  const { data: session } = useSession();
  const [user, setUser] = useState(null);

  useEffect(() => {
    if (!session) return;

    // load user
    const loadUser = async () => {
      const { data } = await supabase
        .from("users")
        .select("*")
        .eq("email", session.user.email)
        .single();

      setUser(data);
    };

    loadUser();

    // REALTIME USER UPDATES
    const channel = supabase
      .channel("user-channel")
      .on(
        "postgres_changes",
        {
          event: "*",
          schema: "public",
          table: "users",
          filter: `email=eq.${session.user.email}`,
        },
        (payload) => {
          setUser(payload.new);
        }
      )
      .subscribe();

    return () => supabase.removeChannel(channel);
  }, [session]);

  if (!session) return <h2>Login required</h2>;

  if (!user) return <h2>Loading...</h2>;

  return (
    <div>
      <h1>🔥 LIVE MINING DASHBOARD</h1>

      <p>Plan: {user.plan}</p>
      <p>Balance: {user.balance}</p>

      <p>Status: {user.mining_active ? "ACTIVE" : "INACTIVE"}</p>
    </div>
  );
}
📊 6. LIVE MINING ENGINE → DATABASE SYNC
Now your fake mining engine updates Supabase in real time.
/lib/miningEngine.js (UPGRADED)
JavaScript
import { supabase } from "./supabaseClient";

export function startMining(email) {
  let hashRate = 120;
  let balance = 0;

  setInterval(async () => {
    hashRate += (Math.random() - 0.5) * 10;
    hashRate = Math.max(80, hashRate);

    balance += hashRate * 0.000001;

    // UPDATE DATABASE LIVE
    await supabase
      .from("users")
      .update({
        balance: balance.toFixed(6),
      })
      .eq("email", email);
  }, 3000);
}
🔴 7. REAL-TIME ADMIN DASHBOARD POWER
Now your admin panel becomes LIVE:
Payments appear instantly
Users update instantly
Mining stats refresh automatically
No refresh needed.
⚡ REAL-TIME ARCHITECTURE
Plain text
Binance Pay Webhook
        ↓
Supabase Database Update
        ↓
Realtime Engine (Postgres Changes)
        ↓
Frontend Subscription Channel
        ↓
UI Updates Instantly
🚀 WHAT YOU NOW HAVE
🔥 LIVE SYSTEM CAPABILITIES
🔴 Instant payment feed
🔴 Live user status updates
🔴 Real-time mining balance updates
🔴 Admin dashboard streaming data
🔴 No refresh SaaS experience
🧠 WHAT THIS MEANS FOR YOUR PLATFORM
You now have a system that behaves like:
Binance dashboard
Coinbase live charts
Web3 mining dashboards
SaaS admin panels
🔮 NEXT LEVEL UPGRADE OPTIONS
If you want to go even further:
🟣 1. LIVE CHART ENGINE
TradingView-style graphs
Earnings curve animation
🔵 2. FRAUD DETECTION AI
Detect fake payments
Flag suspicious users
🟢 3. PUSH NOTIFICATIONS
Telegram alerts for payments
Email alerts for upgrades
🔴 4. FULL DEPLOYABLE ZIP
GitHub repo
Netlify production config
Ready-to-launch SaaS
Just say:
“add live charts”
or
“add AI admin system”
or
“make deploy ZIP”



"use client";

import { Canvas } from "@react-three/fiber";
import { OrbitControls, Float } from "@react-three/drei";

function Doge() {
  return (
    <Float speed={2} rotationIntensity={2} floatIntensity={3}>
      <mesh>
        <sphereGeometry args={[1.2, 64, 64]} />
        <meshStandardMaterial color="#f5c542" metalness={0.6} roughness={0.2} />
      </mesh>
    </Float>
  );
}

export default function Doge3D() {
  return (
    <div className="h-[400px] w-full">
      <Canvas camera={{ position: [0, 0, 5] }}>
        <ambientLight intensity={1.5} />
        <pointLight position={[10, 10, 10]} />
        <Doge />
        <OrbitControls enableZoom={false} />
      </Canvas>
    </div>
  );
}



import Doge3D from "@/components/Doge3D";
import Link from "next/link";

export default function Home() {
  return (
    <main className="min-h-screen bg-black text-white p-6">
      <h1 className="text-4xl font-bold text-center">
        ELON DOGE MINING SOLUTIONS
      </h1>

      <p className="text-center text-gray-400 mt-2">
        Global Mining Dashboard for Dogecoin Ecosystem
      </p>

      <Doge3D />

      <div className="flex justify-center mt-10 gap-4">
        <Link href="/dashboard" className="px-6 py-3 bg-yellow-500 rounded-xl">
          Launch Dashboard
        </Link>

        <Link href="/pricing" className="px-6 py-3 bg-gray-800 rounded-xl">
          View Plans
        </Link>
      </div>
    </main>
  );
}




export default function Pricing() {
  return (
    <div className="min-h-screen bg-black text-white p-10">
      <h1 className="text-3xl text-center mb-10">Mining Plans</h1>

      <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
        {plans.map((p, i) => (
          <div key={i} className="bg-gray-900 p-6 rounded-xl">
            <h2 className="text-xl font-bold">{p.doge} DOGE Plan</h2>
            <p className="text-gray-400 mt-2">Estimated Package Value</p>
            <h3 className="text-2xl mt-4 text-yellow-400">${p.price}</h3>

            <button className="mt-6 w-full bg-yellow-500 py-2 rounded-xl">
              Buy with Card
            </button>
          </div>
        ))}
      </div>
    </div>
  );
}






import Stripe from "stripe";

const stripe = new Stripe(process.env.STRIPE_SECRET_KEY!);

export async function POST(req: Request) {
  const { amount } = await req.json();

  const session = await stripe.checkout.sessions.create({
    payment_method_types: ["card"],
    line_items: [
      {
        price_data: {
          currency: "usd",
          product_data: {
            name: "ELON DOGE MINING PLAN",
          },
          unit_amount: amount * 100,
        },
        quantity: 1,
      },
    ],
    mode: "payment",
    success_url: "https://your-site.com/success",
    cancel_url: "https://your-site.com/cancel",
  });

  return Response.json({ url: session.url });
}


export async function POST(req: Request) {
  const body = await req.json();

  // This is a secure placeholder structure ONLY
  const response = {
    merchantTradeNo: Date.now().toString(),
    orderAmount: body.amount,
    currency: "USDT",
    status: "PENDING",
  };

  return Response.json(response);
}


export async function POST(req: Request) {
  const { message } = await req.json();

  const reply = {
    response:
      "I am your ELON DOGE AI Guide. I help you understand mining plans, wallets, and dashboard usage.",
  };

  return Response.json(reply);
}



export const languages = {
  en: { welcome: "Welcome to ELON DOGE MINING" },
  es: { welcome: "Bienvenido a ELON DOGE MINING" },
  fr: { welcome: "Bienvenue" },
  de: { welcome: "Willkommen" },
};  
export const languages = {
  en: { welcome: "Welcome to ELON DOGE MINING" },
  es: { welcome: "Bienvenido a ELON DOGE MINING" },
  fr: { welcome: "Bienvenue" },
  de: { welcome: "Willkommen" },
};



setInterval(() => {
  document.body.classList.toggle("theme-gold");
}, 40000);



BINANCE_PAY_MERCHANT_ID=726040643
BINANCE_PAY_API_KEY=1hc6kgztgzbhebkpwkgvvukrhbfhcuhcy16b5feuuj3mccsdbhmalj2qv29p30ek

BINANCE_PAY_API_KEY=1hc6kgztgzbhebkpwkgvvukrhbfhcuhcy16b5feuuj3mccsdbhmalj2qv29p30ek
NEXT_PUBLIC_SITE_URL=https://officialelondogemining.lives





import crypto from "crypto";

export async function POST(req: Request) {
  const body = await req.json();

  const payload = {
    env: {
      terminalType: "WEB"
    },
    merchantTradeNo: Date.now().toString(),
    orderAmount: body.amount,
    currency: "USDT",
    goods: {
      goodsType: "02",
      goodsCategory: "D000",
      referenceGoodsId: "DOGE_PLAN",
      goodsName: body.plan,
    },
  };

  return Response.json({
    success: true,
    payload,
  });
}



"Welcome to ELON DOGE MINING SOLUTIONS. How can I assist you today?"




create table users (
  id uuid primary key,
  email text,
  full_name text,
  country text,
  language text,
  created_at timestamp
);


create table wallets (
  id uuid primary key,
  user_id uuid,
  doge_address text,
  balance numeric
);


create table transactions (
  id uuid primary key,
  user_id uuid,
  amount numeric,
  status text,
  tx_hash text,
  created_at timestamp
);
git init
git add .
git commit -m "Production SaaS setup"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main

npm install
npm run build
vercel deploy

[build]
  command = "npm run build"

[[plugins]]
  package = "@netlify/plugin-nextjs"
npm install @netlify/plugin-nextjs
/app/page.tsx
/pages/index.js

npm run build
netlify deploy

[![Netlify Status](https://api.netlify.com/api/v1/badges/202f21a2-e7b8-4457-88fa-e7a45ff7f6bc/deploy-status)](https://app.netlify.com/projects/officialelondogeminings/deploys)
on:
  push:
    branches: [ "main" ]
  workflow_dispatch:

env:
  AZURE_WEBAPP_NAME: your-app-name    # set this to your application's name
  AZURE_WEBAPP_PACKAGE_PATH: '.'      # set this to the path to your web app project, defaults to the repository root
  NODE_VERSION: '20.x'                # set this to the node version to use

permissions:
  contents: read

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4

    - name: Set up Node.js
      uses: actions/setup-node@v4
      with:
        node-version: ${{ env.NODE_VERSION }}
        cache: 'npm'

    - name: npm install, build, and test
      run: |
        npm install
        npm run build --if-present
        npm run test --if-present

    - name: Upload artifact for deployment job
      uses: actions/upload-artifact@v4
      with:
        name: node-app
        path: .

  deploy:
    permissions:
      contents: none
    runs-on: ubuntu-latest
    needs: build
    environment:
      name: 'Development'
      url: ${{ steps.deploy-to-webapp.outputs.webapp-url }}

    steps:
    - name: Download artifact from build job
      uses: actions/download-artifact@v4
      with:
        name: node-app

    - .github/workflows/azure-webapps-node.yml
on:
  push:
    branches:
      - main
# on:
#   push:
#     branches:
#       - main
on: workflow_dispatch
azure-webapps-node.yml → azure-webapps-node.disabled
.github/workflows/azure-webapps-node.yml

package.json
src/
public/
npm install @supabase/supabase-js @supabase/ssr
npx shadcn@latest add @supabase/supabase-client-nextjs
NEXT_PUBLIC_SUPABASE_URL=https://ulafajakyuguntbytdui.supabase.co
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=sb_publishable_G_z62836e2EXYJkOgCa5Zg_pvGt8GTP
import { createServerClient } from '@supabase/ssr';
import { cookies } from 'next/headers';

export function createClient() {
  const cookieStore = cookies();

  return createServerClient(
    process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=sb_publishable_G_z62836e2EXYJkOgCa5Zg_pvGt8GTP
!,
    {
      cookies: {
        get(name: string) {
          return cookieStore.get(name)?.value;
        },
      },
    }
  );
}
import { createClient } from '@/lib/supabase/server';

export default async function Page() {
  const supabase = createClient();

  const { data, error } = await supabase
    .from('users')
    .select('*');

  return (
    <pre>{JSON.stringify(data, null, 2)}</pre>
  );
}
import { createBrowserClient } from '@supabase/supabase-js';

export const supabase = createBrowserClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL=https://ulafajakyuguntbytdui.supabase.co!,
  https://ulafajakyuguntbytdui.supabase.co!
);
'use client';

import { supabase } from '@/lib/supabase/client';
import { useState } from 'react';

export default function AddUser() {
  const [email, setEmail] = useState('');

  async function addUser() {
    const { data, error } = await supabase
      .from('users')
      .insert({ email });

    console.log(data, error);
  }

  return (
    <div>
      <input 
        value={email}
        onChange={(e) => setEmail(e.target.value)}
        placeholder="Enter email"
      />
      <button onClick={addUser}>Add User</button>
    </div>
  );
}
NEXT_PUBLIC_SUPABASE_URL=https://ulafajakyuguntbytdui.supabase.co
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=sb_publishable_G_z62836e2EXYJkOgCa5Zg_pvGt8GTP
import { createBrowserClient } from '@supabase/supabase-js';

export const supabase = createBrowserClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL!,
  process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY!
);
NEXT_PUBLIC_SUPABASE_URL=https://ulafajakyuguntbytdui.supabase.co
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=sb_publishable_...
npm install prisma --save-dev
npx prisma init
# Connect to Supabase via connection pooling
DATABASE_URL="postgresql://postgres.ulafajakyuguntbytdui:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:6543/postgres?pgbouncer=true"

# Direct connection to the database. Used for migrations
DIRECT_URL="postgresql://postgres.ulafajakyuguntbytdui:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:5432/postgres"
npm install prisma --save-dev
npx prisma init
# Connect to Supabase via connection pooling
DATABASE_URL="postgresql://postgres.ulafajakyuguntbytdui:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:6543/postgres?pgbouncer=true"

# Direct connection to the database. Used for migrations
DIRECT_URL="postgresql://postgres.ulafajakyuguntbytdui:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:5432/postgres"




npx create-next-app@latest
npm install @supabase/supabase-js @supabase/ssr
NEXT_PUBLIC_SUPABASE_URL=your-url-here
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=your-key-here
import { createBrowserClient } from '@supabase/supabase-js';

export const supabase = createBrowserClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL!,
  process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY!
);
import { createServerClient } from '@supabase/ssr';
import { cookies } from 'next/headers';

export function createClient() {
  const cookieStore = cookies();

  return createServerClient(
    process.env.NEXT_PUBLIC_SUPABASE_URL!,
    process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY!,
    {
      cookies: {
        get(name: string) {
          return cookieStore.get(name)?.value;
        },
      },
    }
  );
}
import { createBrowserClient } from '@supabase/supabase-js';

export const supabase = createBrowserClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL!,
  process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY!
);
import { createServerClient } from '@supabase/ssr';
import { cookies } from 'next/headers';

export function createClient() {
  const cookieStore = cookies();

  return createServerClient(
    process.env.NEXT_PUBLIC_SUPABASE_URL!,
    process.env.NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY!,
    {
      cookies: {
        get(name: string) {
          return cookieStore.get(name)?.value;
        },
      },
    }
  );
}
import { createClient } from '@/lib/supabase/server';

export default async function Page() {
  const supabase = createClient();

  const { data } = await supabase.from('users').select('*');

  return <pre>{JSON.stringify(data, null, 2)}</pre>;
}
npm run dev

  // Sign up with email
  const { user, error } = await supabase.auth.signUp({
    email: 'example@email.com',
    password: 'example-password',
  })
npm install supabase --save-dev
npx supabase init
npx supabase start
docker network create -o 'com.docker.network.bridge.host_binding_ipv4=127.0.0.1' local-network
npx supabase start --network-id local-network
NODE_OPTIONS=--no-experimental-fetch yarn add supabase --dev
yarn supabase init
yarn supabase start
docker network create -o 'com.docker.network.bridge.host_binding_ipv4=127.0.0.1' local-network
npx supabase start --network-id local-network
pnpm add supabase --save-dev --allow-build=supabase
--allow-build=supabase
pnpx supabase init
pnpx supabase start
docker network create -o 'com.docker.network.bridge.host_binding_ipv4=127.0.0.1' local-network
npx supabase start --network-id local-network
brew install supabase/tap/supabase
supabase init
docker network create -o 'com.docker.network.bridge.host_binding_ipv4=127.0.0.1' local-network
npx supabase start --network-id local-network
https://ulafajakyuguntbytdui.supabase.co/mining_sessions
https://ulafajakyuguntbytdui.supabase.co/wallets
https://ulafajakyuguntbytdui.supabase.co/mining_sessions
GRANT SELECT ON <schema_name>.<table_name> TO anon;
GRANT SELECT, INSERT, UPDATE, DELETE ON <schema_name>.<table_name> TO authenticated;
GRANT SELECT, INSERT, UPDATE, DELETE ON <schema_name>.<table_name> TO service_role;
alter table <schema_name>.<table_name>
enable row level security;
create policy "Individuals can view their own todos."
on todos for select
using ( (select auth.uid()) = user_id );
select *
from todos
where auth.uid() = todos.user_id;
-- Policy is implicitly added.
alter table "table_name" enable row level security;
CREATE OR REPLACE FUNCTION rls_auto_enable()
RETURNS EVENT_TRIGGER
LANGUAGE plpgsql
SECURITY DEFINER
SET search_path = pg_catalog
AS $$
DECLARE
  cmd record;
BEGIN
  FOR cmd IN
    SELECT *
    FROM pg_event_trigger_ddl_commands()
    WHERE command_tag IN ('CREATE TABLE', 'CREATE TABLE AS', 'SELECT INTO')
      AND object_type IN ('table','partitioned table')
  LOOP
     IF cmd.schema_name IS NOT NULL AND cmd.schema_name IN ('public') AND cmd.schema_name NOT IN ('pg_catalog','information_schema') AND cmd.schema_name NOT LIKE 'pg_toast%' AND cmd.schema_name NOT LIKE 'pg_temp%' THEN
      BEGIN
        EXECUTE format('alter table if exists %s enable row level security', cmd.object_identity);
        RAISE LOG 'rls_auto_enable: enabled RLS on %', cmd.object_identity;
      EXCEPTION
        WHEN OTHERS THEN
          RAISE LOG 'rls_auto_enable: failed to enable RLS on %', cmd.object_identity;
      END;
     ELSE
        RAISE LOG 'rls_auto_enable: skip % (either system schema or not in enforced list: %.)', cmd.object_identity, cmd.schema_name;
     END IF;
  END LOOP;
END;
$$;
DROP EVENT TRIGGER IF EXISTS ensure_rls;
CREATE EVENT TRIGGER ensure_rls
ON ddl_command_end
WHEN TAG IN ('CREATE TABLE', 'CREATE TABLE AS', 'SELECT INTO')
EXECUTE FUNCTION rls_auto_enable();
USING (auth.uid() = user_id)
null = user_id
USING (auth.uid() IS NOT NULL AND auth.uid() = user_id)
create policy "Profiles are viewable by everyone"
on profiles for select
to authenticated, anon
using ( true );
-- OR
create policy "Public profiles are viewable only by authenticated users"
on profiles for select
to authenticated
using ( true );
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);
-- 2. Enable RLS
alter table profiles enable row level security;
-- 3. Create Policy
create policy "Public profiles are visible to everyone."
on profiles for select
to anon         -- the Postgres Role (recommended)
using ( true ); -- the actual Policy
create policy "User can see their own profile only."
on profiles
for select using ( (select auth.uid()) = user_id );
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);
-- 2. Enable RLS
alter table profiles enable row level security;
-- 3. Create Policy
create policy "Users can create a profile."
on profiles for insert
to authenticated                          -- the Postgres Role (recommended)
with check ( (select auth.uid()) = user_id );      -- the actual Policy
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);

-- 2. Enable RLS
alter table profiles enable row level security;

-- 3. Create Policy
create policy "Users can update their own profile."
on profiles for update
to authenticated                    -- the Postgres Role (recommended)
using ( (select auth.uid()) = user_id )       -- checks if the existing row complies with the policy expression
with check ( (select auth.uid()) = user_id ); -- checks if the new row complies with the policy expression
If no with check expression is defined, then the using expression will be used both to determine which rows are visible (normal USING case) and which new rows will be allowed to be added (WITH CHECK case).
To perform an UPDATE operation, a corresponding SELECT policy is required. Without a
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);
-- 2. Enable RLS
alter table profiles enable row level security;
-- 3. Create Policy
create policy "Users can delete a profile."
on profiles for delete
to authenticated                     -- the Postgres Role (recommended)
using ( (select auth.uid()) = user_id );      -- the actual Policy
create view <VIEW_NAME>
with(security_invoker = true)
as select <QUERY>
auth.uid()#
auth.jwt()#
raw_app_meta_data
raw_user_meta_data
create policy "User is in team"
on my_table
to authenticated
using ( team_id in (select auth.jwt() -> 'app_metadata' -> 'teams'));
auth.jwt()
create policy "Restrict updates."
on profiles
as restrictive
for update
to authenticated using (
  (select auth.jwt()->>'aal') = 'aal2'
);
alter role "role_name" with bypassrls;
create policy "rls_test_select" on test_table
to authenticated
using ( (select auth.uid()) = user_id );
create index userid
on test_table
using btree (user_id);
Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test1-indexed	171	< 0.1	99.94%	
Details
create policy "rls_test_select" on test_table
to authenticated
using ( (select auth.uid()) = user_id );
auth.uid()
auth.jwt()
Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test2a-wrappedSQL-uid	179	9	94.97%	
Details
test2b-wrappedSQL-isadmin	11,000	7	99.94%	
Details
test2c-wrappedSQL-two-functions	11,000	10	99.91%	
Details
test2d-wrappedSQL-sd-fun	178,000	12	99.993%	
Details
test2e-wrappedSQL-sd-fun-array	173000	16	99.991%	
Details
const { data } = supabase
  .from('table')
  .select()
const { data } = supabase
  .from('table')
  .select()
  .eq('user_id', userId)
Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test3-addfilter	171	9	94.74%	
Details
create policy "rls_test_select" on test_table
to authenticated
using (
  exists (
    select 1 from roles_table
    where (select auth.uid()) = user_id and role = 'good_role'
  )
);
create function private.has_good_role()
returns boolean
language plpgsql
security definer -- will run as the creator
as $$
begin
  return exists (
    select 1 from roles_table
    where (select auth.uid()) = user_id and role = 'good_role'
  );
end;
$$;
-- Update our policy to use this function:
create policy "rls_test_select"
on test_table
to authenticated
using ( (select private.has_good_role()) );
create policy "rls_test_select" on test_table
to authenticated
using (
  (select auth.uid()) in (
    select user_id
    from team_user
    where team_user.team_id = team_id -- joins to the source "test_table.team_id"
  )
)
create policy "rls_test_select" on test_table
to authenticated
using (
  team_id in (
    select team_id
    from team_user
    where user_id = (select auth.uid()) -- no join
  )
);
;
Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test5-fixed-join	9,000	20	99.78%	
Details
create policy "rls_test_select" on rls_test
using ( auth.uid() = user_id );
create policy "rls_test_select" on rls_test
to authenticated
using ( (select auth.uid()) = user_id );
# Row Level Security

Secure your data using Postgres Row Level Security.

When you need granular authorization rules, nothing beats Postgres's [Row Level Security (RLS)](https://www.postgresql.org/docs/current/ddl-rowsecurity.html).

## Row Level Security in Supabase

Supabase allows convenient and secure data access from the browser, as long as you enable RLS.

RLS _must_ always be enabled on any tables stored in an exposed schema. By default, this is the `public` schema.

RLS is enabled by default on tables created with the Table Editor in the dashboard. If you create one in raw SQL or with the SQL editor, remember to enable RLS yourself and grant only the permissions each Postgres role needs.

```sql
GRANT SELECT ON <schema_name>.<table_name> TO anon;
GRANT SELECT, INSERT, UPDATE, DELETE ON <schema_name>.<table_name> TO authenticated;
GRANT SELECT, INSERT, UPDATE, DELETE ON <schema_name>.<table_name> TO service_role;

alter table <schema_name>.<table_name>
enable row level security;
```

RLS is incredibly powerful and flexible, allowing you to write complex SQL rules that fit your unique business needs. RLS can be combined with [Supabase Auth](/docs/guides/auth) for end-to-end user security from the browser to the database.

RLS is a Postgres primitive and can provide "[defense in depth](<https://en.wikipedia.org/wiki/Defense_in_depth_(computing)>)" to protect your data from malicious actors even when accessed through third-party tooling.

## Policies

[Policies](https://www.postgresql.org/docs/current/sql-createpolicy.html) are Postgres's rule engine. Policies are easy to understand once you get the hang of them. Each policy is attached to a table, and the policy is executed every time a table is accessed.

You can just think of them as adding a `WHERE` clause to every query. For example a policy like this ...

```sql
create policy "Individuals can view their own todos."
on todos for select
using ( (select auth.uid()) = user_id );
```

.. would translate to this whenever a user tries to select from the todos table:

```sql
select *
from todos
where auth.uid() = todos.user_id;
-- Policy is implicitly added.
```

## Enabling Row Level Security

You can enable RLS for any table using the `enable row level security` clause:

```sql
alter table "table_name" enable row level security;
```

Once you have enabled RLS, no data will be accessible via the [API](/docs/guides/api) when using a publishable key, until you create policies.

## Auto-enable RLS for new tables

If you want RLS enabled automatically for new tables, you can create an event trigger that runs after table creation. This uses a Postgres [event trigger](/docs/guides/database/postgres/event-triggers) to call `ALTER TABLE ... ENABLE ROW LEVEL SECURITY` on each newly created table.

```sql
CREATE OR REPLACE FUNCTION rls_auto_enable()
RETURNS EVENT_TRIGGER
LANGUAGE plpgsql
SECURITY DEFINER
SET search_path = pg_catalog
AS $$
DECLARE
  cmd record;
BEGIN
  FOR cmd IN
    SELECT *
    FROM pg_event_trigger_ddl_commands()
    WHERE command_tag IN ('CREATE TABLE', 'CREATE TABLE AS', 'SELECT INTO')
      AND object_type IN ('table','partitioned table')
  LOOP
     IF cmd.schema_name IS NOT NULL AND cmd.schema_name IN ('public') AND cmd.schema_name NOT IN ('pg_catalog','information_schema') AND cmd.schema_name NOT LIKE 'pg_toast%' AND cmd.schema_name NOT LIKE 'pg_temp%' THEN
      BEGIN
        EXECUTE format('alter table if exists %s enable row level security', cmd.object_identity);
        RAISE LOG 'rls_auto_enable: enabled RLS on %', cmd.object_identity;
      EXCEPTION
        WHEN OTHERS THEN
          RAISE LOG 'rls_auto_enable: failed to enable RLS on %', cmd.object_identity;
      END;
     ELSE
        RAISE LOG 'rls_auto_enable: skip % (either system schema or not in enforced list: %.)', cmd.object_identity, cmd.schema_name;
     END IF;
  END LOOP;
END;
$$;

DROP EVENT TRIGGER IF EXISTS ensure_rls;
CREATE EVENT TRIGGER ensure_rls
ON ddl_command_end
WHEN TAG IN ('CREATE TABLE', 'CREATE TABLE AS', 'SELECT INTO')
EXECUTE FUNCTION rls_auto_enable();
```

Note that this applies to tables created after the trigger is installed. Existing tables still need RLS enabled manually.

When a request is made without an authenticated user (e.g., no access token is provided or the session has expired), `auth.uid()` returns `null`.

This means that a policy like:

```sql
USING (auth.uid() = user_id)
```

will silently fail for unauthenticated users, because:

```sql
null = user_id
```

is always false in SQL.

To avoid confusion and make your intention clear, we recommend explicitly checking for authentication:

```sql
USING (auth.uid() IS NOT NULL AND auth.uid() = user_id)
```

## Authenticated and unauthenticated roles

Supabase maps every request to one of the roles:

- `anon`: an unauthenticated request (the user is not logged in)
- `authenticated`: an authenticated request (the user is logged in)

These are actually [Postgres Roles](/docs/guides/database/postgres/roles). You can use these roles within your Policies using the `TO` clause:

```sql
create policy "Profiles are viewable by everyone"
on profiles for select
to authenticated, anon
using ( true );

-- OR

create policy "Public profiles are viewable only by authenticated users"
on profiles for select
to authenticated
using ( true );
```

Using the `anon` Postgres role is different from an [anonymous user](/docs/guides/auth/auth-anonymous) in Supabase Auth. An anonymous user assumes the `authenticated` role to access the database and can be differentiated from a permanent user by checking the `is_anonymous` claim in the JWT.

## Creating policies

Policies are SQL logic that you attach to a Postgres table. You can attach as many policies as you want to each table.

Supabase provides some [helpers](#helper-functions) that simplify RLS if you're using Supabase Auth. We'll use these helpers to illustrate some basic policies:

### SELECT policies

You can specify select policies with the `using` clause.

Let's say you have a table called `profiles` in the public schema and you want to enable read access to everyone.

```sql
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);

-- 2. Enable RLS
alter table profiles enable row level security;

-- 3. Create Policy
create policy "Public profiles are visible to everyone."
on profiles for select
to anon         -- the Postgres Role (recommended)
using ( true ); -- the actual Policy
```

Alternatively, if you only wanted users to be able to see their own profiles:

```sql
create policy "User can see their own profile only."
on profiles
for select using ( (select auth.uid()) = user_id );
```

### INSERT policies

You can specify insert policies with the `with check` clause. The `with check` expression ensures that any new row data adheres to the policy constraints.

Let's say you have a table called `profiles` in the public schema and you only want users to be able to create a profile for themselves. In that case, we want to check their User ID matches the value that they are trying to insert:

```sql
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);

-- 2. Enable RLS
alter table profiles enable row level security;

-- 3. Create Policy
create policy "Users can create a profile."
on profiles for insert
to authenticated                          -- the Postgres Role (recommended)
with check ( (select auth.uid()) = user_id );      -- the actual Policy
```

### UPDATE policies

You can specify update policies by combining both the `using` and `with check` expressions.

The `using` clause represents the condition that must be true for the update to be allowed, and `with check` clause ensures that the updates made adhere to the policy constraints.

Let's say you have a table called `profiles` in the public schema and you only want users to be able to update their own profile.

You can create a policy where the `using` clause checks if the user owns the profile being updated. And the `with check` clause ensures that, in the resultant row, users do not change the `user_id` to a value that is not equal to their User ID, maintaining that the modified profile still meets the ownership condition.

```sql
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);

-- 2. Enable RLS
alter table profiles enable row level security;

-- 3. Create Policy
create policy "Users can update their own profile."
on profiles for update
to authenticated                    -- the Postgres Role (recommended)
using ( (select auth.uid()) = user_id )       -- checks if the existing row complies with the policy expression
with check ( (select auth.uid()) = user_id ); -- checks if the new row complies with the policy expression
```

If no `with check` expression is defined, then the `using` expression will be used both to determine which rows are visible (normal USING case) and which new rows will be allowed to be added (WITH CHECK case).

To perform an `UPDATE` operation, a corresponding [`SELECT` policy](#select-policies) is required. Without a `SELECT` policy, the `UPDATE` operation will not work as expected.

### DELETE policies

You can specify delete policies with the `using` clause.

Let's say you have a table called `profiles` in the public schema and you only want users to be able to delete their own profile:

```sql
-- 1. Create table
create table profiles (
  id uuid primary key,
  user_id uuid references auth.users,
  avatar_url text
);

-- 2. Enable RLS
alter table profiles enable row level security;

-- 3. Create Policy
create policy "Users can delete a profile."
on profiles for delete
to authenticated                     -- the Postgres Role (recommended)
using ( (select auth.uid()) = user_id );      -- the actual Policy
```

### Views

Views bypass RLS by default because they are usually created with the `postgres` user. This is a feature of Postgres, which automatically creates views with `security definer`.

In Postgres 15 and above, you can make a view obey the RLS policies of the underlying tables when invoked by `anon` and `authenticated` roles by setting `security_invoker = true`.

```sql
create view 
with(security_invoker = true)
as select 
```

In older versions of Postgres, protect your views by revoking access from the `anon` and `authenticated` roles, or by putting them in an unexposed schema.

## Helper functions

Supabase provides some helper functions that make it easier to write Policies.

### `auth.uid()`

Returns the ID of the user making the request.

### `auth.jwt()`

Not all information present in the JWT should be used in RLS policies. For instance, creating an RLS policy that relies on the `user_metadata` claim can create security issues in your application as this information can be modified by authenticated end users.

Returns the JWT of the user making the request. Anything that you store in the user's `raw_app_meta_data` column or the `raw_user_meta_data` column will be accessible using this function. It's important to know the distinction between these two:

- `raw_user_meta_data` - can be updated by the authenticated user using the `supabase.auth.update()` function. It is not a good place to store authorization data.
- `raw_app_meta_data` - cannot be updated by the user, so it's a good place to store authorization data.

The `auth.jwt()` function is extremely versatile. For example, if you store some team data inside `app_metadata`, you can use it to determine whether a particular user belongs to a team. For example, if this was an array of IDs:

```sql
create policy "User is in team"
on my_table
to authenticated
using ( team_id in (select auth.jwt() -> 'app_metadata' -> 'teams'));
```

Keep in mind that a JWT is not always "fresh". In the example above, even if you remove a user from a team and update the `app_metadata` field, that will not be reflected using `auth.jwt()` until the user's JWT is refreshed.

Also, if you are using Cookies for Auth, then you must be mindful of the JWT size. Some browsers are limited to 4096 bytes for each cookie, and so the total size of your JWT should be small enough to fit inside this limitation.

### MFA

The `auth.jwt()` function can be used to check for [Multi-Factor Authentication](/docs/guides/auth/auth-mfa#enforce-rules-for-mfa-logins). For example, you could restrict a user from updating their profile unless they have at least 2 levels of authentication (Assurance Level 2):

```sql
create policy "Restrict updates."
on profiles
as restrictive
for update
to authenticated using (
  (select auth.jwt()->>'aal') = 'aal2'
);
```

## Bypassing Row Level Security

Supabase provides special "Service" keys, which can be used to bypass RLS. These should never be used in the browser or exposed to customers, but they are useful for administrative tasks.

Supabase will adhere to the RLS policy of the signed-in user, even if the client library is initialized with a Service Key.

You can also create new [Postgres Roles](/docs/guides/database/postgres/roles) which can bypass Row Level Security using the "bypass RLS" privilege:

```sql
alter role "role_name" with bypassrls;
```

This can be useful for system-level access. You should _never_ share login credentials for any Postgres Role with this privilege.

## RLS performance recommendations

Every authorization system has an impact on performance. While row level security is powerful, the performance impact is important to keep in mind. This is especially true for queries that scan every row in a table - like many `select` operations, including those using limit, offset, and ordering.

Based on a series of [tests](https://github.com/GaryAustin1/RLS-Performance), we have a few recommendations for RLS:

### Add indexes

Make sure you've added [indexes](/docs/guides/database/postgres/indexes) on any columns used within the Policies which are not already indexed (or primary keys). For a Policy like this:

```sql
create policy "rls_test_select" on test_table
to authenticated
using ( (select auth.uid()) = user_id );
```

You can add an index like:

```sql
create index userid
on test_table
using btree (user_id);
```

#### Benchmarks

| Test                                                                                          | Before (ms) | After (ms) | % Improvement | Change                                                                                                   |
| --------------------------------------------------------------------------------------------- | ----------- | ---------- | ------------- | -------------------------------------------------------------------------------------------------------- |
| [test1-indexed](https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test1-indexed) | 171         | < 0.1      | 99.94%        | <details className="cursor-pointer">Before:<br/>No index<br/><br/>After:<br/>`user_id` indexed</details> |

### Call functions with `select`

You can use `select` statement to improve policies that use functions. For example, instead of this:

```sql
create policy "rls_test_select" on test_table
to authenticated
using ( auth.uid() = user_id );
```

You can do:

```sql
create policy "rls_test_select" on test_table
to authenticated
using ( (select auth.uid()) = user_id );
```

This method works well for JWT functions like `auth.uid()` and `auth.jwt()` as well as `security definer` Functions. Wrapping the function causes an `initPlan` to be run by the Postgres optimizer, which allows it to "cache" the results per-statement, rather than calling the function on each row.

You can only use this technique if the results of the query or function do not change based on the row data.

#### Benchmarks

| Test                                                                                                                              | Before (ms) | After (ms) | % Improvement | Change                                                                                                                                                                    |
| --------------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [test2a-wrappedSQL-uid](<https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test2a-wrappedSQL-uid()>)                 | 179         | 9          | 94.97%        | <details className="cursor-pointer">Before:<br/>`auth.uid() = user_id` <br/><br/>After:<br/> `(select auth.uid()) = user_id`</details>                                    |
| [test2b-wrappedSQL-isadmin](<https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test2b-wrappedSQL-isadmin()>)         | 11,000      | 7          | 99.94%        | <details className="cursor-pointer">Before:<br/>`is_admin()` _table join_<br/><br/>After:<br/>`(select is_admin())` _table join_</details>                                |
| [test2c-wrappedSQL-two-functions](https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test2c-wrappedSQL-two-functions) | 11,000      | 10         | 99.91%        | <details className="cursor-pointer">Before:<br/>`is_admin() OR auth.uid() = user_id`<br/><br/>After:<br/>`(select is_admin()) OR (select auth.uid() = user_id)`</details> |
| [test2d-wrappedSQL-sd-fun](https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test2d-wrappedSQL-sd-fun)               | 178,000     | 12         | 99.993%       | <details className="cursor-pointer">Before:<br/>`has_role() = role` <br/><br/>After:<br/>(select has_role()) = role</details>                                             |
| [test2e-wrappedSQL-sd-fun-array](https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test2e-wrappedSQL-sd-fun-array)   | 173000      | 16         | 99.991%       | <details className="cursor-pointer">Before:<br/>`team_id=any(user_teams())` <br/><br/>After:<br/>team_id=any(array(select user_teams()))</details>                        |

### Add filters to every query

Policies are "implicit where clauses," so it's common to run `select` statements without any filters. This is a bad pattern for performance. Instead of doing this (JS client example):

```js
const { data } = supabase
  .from('table')
  .select()
```

You should always add a filter:

```js
const { data } = supabase
  .from('table')
  .select()
  .eq('user_id', userId)
```

Even though this duplicates the contents of the Policy, Postgres can use the filter to construct a better query plan.

#### Benchmarks

| Test                                                                                              | Before (ms) | After (ms) | % Improvement | Change                                                                                                                                 |
| ------------------------------------------------------------------------------------------------- | ----------- | ---------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| [test3-addfilter](https://github.com/GaryAustin1/RLS-Performance/tree/main/tests/test3-addfilter) | 171         | 9          | 94.74%        | <details className="cursor-pointer">Before:<br/>`auth.uid() = user_id`<br/><br/>After:<br/>add `.eq` or `where` on `user_id`</details> |

### Use security definer functions#
A "security definer" function runs using the same role that created the function. This means that if you create a role with a superuser (like postgres), then that function will have bypassrls privileges. For example, if you had a policy like this:

create policy "rls_test_select" on test_table
to authenticated
using (
  exists (
    select 1 from roles_table
    where (select auth.uid()) = user_id and role = 'good_role'
  )
);
We can instead create a security definer function which can scan roles_table without any RLS penalties:

create function private.has_good_role()
returns boolean
language plpgsql
security definer -- will run as the creator
as $$
begin
  return exists (
    select 1 from roles_table
    where (select auth.uid()) = user_id and role = 'good_role'
  );
end;
$$;
-- Update our policy to use this function:
create policy "rls_test_select"
on test_table
to authenticated
using ( (select private.has_good_role()) );
Security-definer functions should never be created in a schema in the "Exposed schemas" inside your API settings`.

Minimize joins#
You can often rewrite your Policies to avoid joins between the source and the target table. Instead, try to organize your policy to fetch all the relevant data from the target table into an array or set, then you can use an IN or ANY operation in your filter.

For example, this is an example of a slow policy which joins the source test_table to the target team_user:

create policy "rls_test_select" on test_table
to authenticated
using (
  (select auth.uid()) in (
    select user_id
    from team_user
    where team_user.team_id = team_id -- joins to the source "test_table.team_id"
  )
);
We can rewrite this to avoid this join, and instead select the filter criteria into a set:

create policy "rls_test_select" on test_table
to authenticated
using (
  team_id in (
    select team_id
    from team_user
    where user_id = (select auth.uid()) -- no join
  )
);
In this case you can also consider using a security definer function to bypass RLS on the join table:

If the list exceeds 1000 items, a different approach may be needed or you may need to analyze the approach to ensure that the performance is acceptable.

Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test5-fixed-join	9,000	20	99.78%	
Details
Specify roles in your policies#
Always use the Role of inside your policies, specified by the TO operator. For example, instead of this query:

create policy "rls_test_select" on rls_test
using ( auth.uid() = user_id );
Use:

create policy "rls_test_select" on rls_test
to authenticated
using ( (select auth.uid()) = user_id );
This prevents the policy ( (select auth.uid()) = user_id ) from running for any anon users, since the execution stops at the to authenticated step.

Benchmarks#
Test	Before (ms)	After (ms)	% Improvement	Change
test6-To-role	170	< 0.1	99.78%	
Details
await supabase.auth.signUp({
  email: "someone@example.com",
  password: "strongpassword"
})
auth.users

Step 2 — Create a trigger to auto‑insert into your users table
Run this SQL in Supabase SQL Editor:

`sql
create or replace function public.handlenewuser()
returns trigger as $$
begin
  insert into public.users (id, email)
  values (new.id, new.email);
  return new;
end;
$$ language plpgsql security definer;

create trigger onauthuser_created
after insert on auth.users
for each row execute procedure public.handlenewuser();
`

Now every time someone signs up:

- Supabase inserts into auth.users
- Your trigger inserts into your users table automatically

No manual work. No Table Editor.

---
Create an API route (Next.js example)

/app/api/create-user/route.ts

`ts
import { createClient } from '@supabase/supabase-js';

export async function POST(req) {
  const { email } = await req.json();

  const supabase = createClient(
    process.env.NEXTPUBLICSUPABASE_URL,
    process.env.SUPABASESERVICEROLE_KEY
  );

  const { data, error } = await supabase
    .from('users')
    .insert([{ email }]);

  return Response.json({ data, error });
}
`

Step 2 — Your frontend calls it

`ts
await fetch("/api/create-user", {
  method: "POST",
  body: JSON.stringify({ email: "someone@example.com" })
});
`

The user is inserted automatically.

---