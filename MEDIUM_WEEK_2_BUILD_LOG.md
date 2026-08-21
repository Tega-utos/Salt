# How I Built a Faith-Based Daily Habit App in a Week with AI

*Why most faith apps fail at real-world discipleship, and how we built **Salt**—a daily kindness ritual and testimony engine—from zero to production.*

---

![Cover Image: Salt App Interface & Crystal Logo](https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=1200&q=80)

Every morning, millions of believers open their phones, tap a daily devotion, skim a verse, check a box, and close the screen. 

Ten minutes later, on the subway or in a traffic jam, they cut someone off or ignore a coworker who is visibly overwhelmed.

Here is the quiet truth about the Christian tech ecosystem: **most faith apps are built for passive consumption, not real-world transformation.** They give you reading plans, audio prayers, and guilt-inducing streak counters. But Jesus didn’t say, *"You are the consumers of the earth."* He said, **"You are the salt of the earth."** (Matthew 5:13). Salt is only useful when it leaves the shaker and touches the food.

Over the last 7 days, I set out to build and ship **Salt**: a daily habit app that turns scripture into concrete, real-world acts of love, paired with a live community feed called the **Gist Corner** where believers share unfiltered testimonies of what happened when they stepped out in faith.

Here is the complete build log: the architecture, the UX decisions, the prompt workflows, and what building with AI actually looks like in practice.

---

## 1. The Core Product Thesis: Active Rituals > Passive Checklists

When designing Salt, I anchored on three core heuristics:

```
┌─────────────────────────────────────────────────────────┐
│                    THE SALT LOOP                        │
│                                                         │
│   [ 1. Daily Ritual ] ───► [ 2. Real Act of Love ]      │
│            ▲                              │             │
│            │                              ▼             │
│   [ 4. Companion Bread ] ◄─── [ 3. Share in Gist ]      │
└─────────────────────────────────────────────────────────┘
```

1. **One Clear Action per Day**: No choice overload. Every 24 hours at midnight, every user in the community receives the exact same real-world challenge (e.g., *“Pay someone’s fare today without letting them know,”* or *“Send a 60-second voice note of encouragement to someone you haven't spoken to this month”*).
2. **Deferred Authentication**: Nothing kills a habit app faster than forcing a user to fill out a 6-field registration form before they even see what the app does. In Salt, you can take the challenge, choose your companion guide, and explore the feed as a guest on Day 1. Auth is requested only when you want to post your first testimony or save multi-day streaks.
3. **The Gist Corner (Social Proof & Encouragement)**: Solitary habit tracking leads to drop-off. When you complete an act, you drop a "Gist"—a micro-reflection with Discord-style reaction pills (🔥, 🧂, 🙏, ❤️) and threaded replies.

---

## 2. The Tech Stack & Architecture

I built Salt as a single-page progressive web application (PWA) with zero build-step overhead, enabling immediate deployment to Vercel/GitHub Pages:

* **Frontend**: Vanilla ES6+ JavaScript, CSS3 Design Tokens, Phosphor Vector Icons, and HTML5 Canvas.
* **Procedural Visuals**: A custom procedural 3D coarse salt crystal engine rendered via HTML5 Canvas using vector geometry and specular light simulation.
* **Companion Mascot Engine**: Dynamic, zero-dependency SVG vector illustrations with built-in idle breathing, blinking, and celebrate animations (**Salty**, **Aura**, and **Pax**).
* **Backend & Auth**: **Supabase** (PostgreSQL, Row-Level Security, Realtime WebSockets, and Auth).

```
   ┌──────────────────────────────────────────────────────────┐
   │                       SALT APP                           │
   ├────────────────────────────┬─────────────────────────────┤
   │       User Client          │      Supabase Backend       │
   │  • Canvas 3D Crystal       │  • profiles table           │
   │  • SVG Vector Mascots      │  • gists table              │
   │  • Deferred Auth Flow      │  • daily_challenges table   │
   │  • Micro-sound SFX Engine  │  • Realtime Subscriptions   │
   └────────────────────────────┴─────────────────────────────┘
```

---

## 3. What Building with AI Actually Looked Like

There’s a lot of hype right now around "vibecoding"—the idea that you just type a sentence into an AI model and a billion-dollar SaaS pops out.

In reality, building a polished, shippable application with AI is an exercise in **ruthless editing and taste**. Here is where AI was a superpower, and where human intervention was required:

### Where AI Saved 20+ Hours
1. **Database Schema & RLS Policies**: Prompting the AI with my data model generated clean PostgreSQL tables (`profiles`, `gists`, `comments`, `reactions`), complete with Row-Level Security policies ensuring users can only edit or delete their own posts.
2. **Procedural SVG Companion Mascots**: Instead of relying on heavy, static AI image renders that clashed with the dark-mode UI, I used AI to write SVG vector generators that adapt dynamically to character emotions (`calm`, `celebrating`, `tickled`).
3. **Sound & Haptic Synthesis**: AI generated lightweight Web Audio API oscillators that synthesize tactile "pop", "coin collected", and "tickle" sounds without needing external `.mp3` assets.

### Where AI Failed (and Human Taste Had to Steer)
1. **Layout Leaks & CSS Specificity**: AI frequently dropped fixed-position overlay widgets into parent views without scoping them. We spent hours debugging a floating mascot widget that was bleeding through the splash screen on mobile viewports.
2. **Feature Creep**: Left to itself, AI will suggest adding a 5-tier subscription paywall, complex AI chatbots, and analytics dashboards before the core loop even works. I had to explicitly strip out premature monetization to keep the user experience pure.
3. **Typography & Spatial Hierarchy**: AI loves generic 16px margins. Making the app feel like a native iOS experience (optical kerning, glassmorphic bottom sheets, subtle button tactile depression) required hands-on CSS refactoring.

---

## 4. Key Lessons from Week 2

If you're building faith-based technology or indie hacking with AI tools, here are three principles worth remembering:

### 1. Build for the Flesh-and-Blood World
If your app only succeeds when users spend 45 minutes staring at their screens, you have built a digital distraction, not a spiritual tool. A great faith tool should prompt an action in the real world and get out of the way.

### 2. Don’t Gate Value Behind a Sign-Up Wall
Let users experience the dopamine of checking off their first act before you ask for their email address. Trust is earned in the first 30 seconds of interaction.

### 3. Polish Is Not Optional
Christian technology has historically had a reputation for subpar design. But excellence in craft is an act of stewardship. Fluid 60fps animations, cohesive typography, and clean audio feedback communicate that you care about the person on the other end of the glass.

---

## 5. What’s Next: Week 3 & Beyond

With **Salt** live and running on Supabase with real-time community reflections:

* **Week 3 Focus**: Collecting early user feedback, refining the Daily Bread reward drops, and implementing community moderation tools.
* **App 2 Kickoff**: Starting ideation on our second 90-day build (a scripture memorization spaced-repetition engine).

---

> *"Let your light shine before others, that they may see your good deeds and glorify your Father in heaven."* — Matthew 5:16

**Try Salt live**: [Link to your deployed site/GitHub]  
**Follow the journey on X**: [@YourHandle]  
**Connect on LinkedIn**: [Your LinkedIn Profile]

---

*This is Week 2 of my 90-Day Build-in-Public journey, where I'm shipping 3 faith-based apps in public and writing about faith, product design, and AI-assisted workflows.*
