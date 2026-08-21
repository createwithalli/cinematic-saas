# Aether — Cinematic SaaS Template

**Ultra-realistic open-source SaaS starter** with 3D hover effects, Spline scenes, Framer Motion animations, WebGPU-ready architecture, full CRM, Calendar, end-to-end encrypted Messenger, and Web3 wallet patterns.

> Cinematic dark UI · Glassmorphism · Neon accents · Easy to extend for any product concept.

![License](https://img.shields.io/badge/license-MIT-cyan)
![Next.js](https://img.shields.io/badge/Next.js-15-black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)

## ✨ Features

| Feature | Description |
|---------|-------------|
| **3D & Spline** | Interactive Spline scenes + CSS 3D perspective hover cards |
| **Framer Motion** | Cinematic page transitions, staggered reveals, layout animations |
| **WebGPU Ready** | Headers & architecture prepared for WebGPU compute/render |
| **CRM** | Contacts table + mock API + Prisma schema for deals/pipeline |
| **Calendar** | Full month view with events, API route, date-fns |
| **Secure Messenger** | Chat UI inspired by popular apps + live AES-GCM encryption demo (Web Crypto) |
| **Web3** | Wallet connect mock ready to swap for wagmi / viem / WalletConnect |
| **Cinematic UI** | Dark mesh backgrounds, grain overlay, neon glow, glass panels |
| **Easy UX** | Responsive, keyboard-friendly, clear navigation, micro-interactions |

## 🚀 Quick Start

```bash
git clone https://github.com/createwithalli/cinematic-saas.git
cd cinematic-saas
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Optional: Prisma database

```bash
npx prisma generate
npx prisma db push
npx prisma studio
```

Then replace the mock API routes with real Prisma queries.

## 📁 Project Structure

```
src/
├── app/
│   ├── page.tsx              # Cinematic landing + Spline hero
│   ├── dashboard/            # Overview stats & recent deals
│   ├── crm/                  # Contacts table (API-backed)
│   ├── calendar/             # Month calendar + events
│   ├── messenger/            # Encrypted chat demo
│   ├── web3/                 # Wallet connect UI
│   └── api/
│       ├── contacts/         # GET/POST mock CRM
│       └── events/           # Calendar events
├── components/
│   ├── Navbar.tsx
│   ├── Sidebar.tsx
│   ├── Hero3D.tsx            # Spline + Framer
│   └── FeatureGrid.tsx
└── lib/
    └── utils.ts              # cn() + encrypt/decrypt helpers
prisma/
└── schema.prisma             # Contact, Deal, Event, Message models
```

## 🎨 Tech Stack

- **Framework**: Next.js 15 (App Router) + TypeScript
- **Styling**: Tailwind CSS v4 + custom cinematic tokens
- **Motion**: Framer Motion
- **3D**: `@splinetool/react-spline`
- **Icons**: Lucide React
- **Dates**: date-fns
- **Encryption**: Web Crypto API (AES-GCM)
- **DB (optional)**: Prisma + SQLite / PostgreSQL

## 🔄 Multi-Purpose Concepts

This single template can become:

1. **CRM SaaS** — Expand Prisma models, add pipeline kanban, email sequences
2. **Encrypted Messenger** — Add Socket.io / PartyKit, real E2E (Signal protocol), groups
3. **Web3 Dashboard** — Plug wagmi, on-chain analytics, NFT galleries with WebGPU
4. **Scheduling Product** — Full calendar + bookings + Zoom/Meet links
5. **Internal Tool** — Admin panels, analytics, team collaboration

Just delete the pages you don’t need and rename the rest.

## 🔒 Encryption Demo

The Messenger page uses the browser’s Web Crypto API:

```ts
import { encryptMessage, decryptMessage } from "@/lib/utils";

const { ciphertext, iv } = await encryptMessage("secret text", "password");
const plain = await decryptMessage(ciphertext, iv, "password");
```

In production, never send the password; use proper key exchange (X25519 etc.).

## 🖼 Customizing the 3D Scene

1. Create a scene in [Spline](https://spline.design)
2. Export → Code → React
3. Replace the `scene` prop in `Hero3D.tsx`

```tsx
<Spline scene="https://prod.spline.design/YOUR_SCENE/scene.splinecode" />
```

## 🌐 Deploy

### Vercel (recommended)

```bash
npx vercel
```

Or connect the GitHub repo in the Vercel dashboard.

### Other

Any Node host that supports Next.js works (Netlify, Railway, Fly.io, etc.).

## 📄 License

MIT — free for personal and commercial use. Attribution appreciated but not required.

## 🙌 Credits

- Spline for the beautiful 3D runtime
- Framer Motion team
- Vercel / Next.js
- The open-source community

---

Built with cinematic intent. Ship something that feels alive.
