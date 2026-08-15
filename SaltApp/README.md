# Salt 🧂 — Daily Challenge & Companion Guide

An interactive, high-fidelity faith-streak prototype built around custom companion guides, gamified progression systems, real-time sentiment analysis, and a comprehensive administrative control dashboard. 

Built with HTML5, CSS3, vanilla JavaScript, and [Phosphor Icons](https://phosphoricons.com/).

---

## 🌟 Key Features

### 1. Interactive Companion Guides (Salty, Aura, Pax)
- **Breathing Mascot Center**: Persistent companion peeker snapping vertically along phone bezels with snapped visual adaptation.
- **Personality Dialogues**: Character dialogues matching Salty (energetic), Aura (scripture-inspired), and Pax (high-accountability).
- **Suggestions System**: Inline expandable dropdown panels displaying personality-specific actionable tips to help users complete their daily acts.
- **Easter Eggs & Inactivity**: Rapid-tap tickle animations with chimes, alongside 15-second inactivity detectors triggering guide cues.

### 2. Gamified Progression & Streak Defense
- **Streak Aura (Halo)**: Glowing ambient backing overlay scaling and shifting colors based on active streak tiers (Ember 0-3, Amber 4-9, Volt green 10+).
- **Daily Bread Drops**: Bouncing badge triggers glassmorphic modal scrolls delivering daily scriptures and unlocking collectible **Streak Shields** (streak protection).
- **Companion Logbook Board**: Profile dashboard tracking lifetime accomplishments (Acts Supported, Bread Eaten, Gists Shared) with level-up animations.

### 3. Real-Time Sentiment & Feeds
- **Contextual Sentiment Analyzer**: Monitors inputs inside the Gist testimony editor to swap the guide's avatar dynamically (Celebrating vs Reflective) in real time.
- **Gist Corner Feed**: Translucent iOS 18 glass navigation tab switcher to post, react to, and read community testimonies.

### 4. Admin Control Console (Login: `teeutos@gmail.com`)
- **Live Challenge Creator**: Write, tag, and publish Today's challenge, scripture references, and tags on the fly.
- **🪄 Suggest Prompt Generator**: Instantly fills creator forms with random acts of kindness for admin review.
- **Auto-Push Scheduler**: Daily countdown clock reset automatically pushes new challenges live from a pre-seeded pool if manual updates are missed.
- **Feed Moderation Mode**: Appends red trash can delete triggers to all cards in the testimony feed with fade-out animations.

---

## 🚀 How to Run Locally

Since this is a self-contained, client-side static HTML prototype, running it requires no server setups:

1. Clone or download this repository.
2. Ensure the `salt_ui_prototype.html` file and all companion `.jpg` images are stored in the same folder.
3. Open `salt_ui_prototype.html` in any browser (Chrome, Edge, Firefox, Safari).

---

## 📦 How to Deploy

You can deploy this directory instantly to static hosting platforms:

### Option A: Netlify Drag-and-Drop
1. Zip this entire folder (containing the HTML, README, and all `.jpg` assets).
2. Go to [Netlify Drop](https://app.netlify.com/drop).
3. Drag and drop the `.zip` file. It will be live under a public URL within 10 seconds!

### Option B: GitHub Pages
1. Push this folder to a public repository on GitHub.
2. Go to **Settings → Pages** in your repository.
3. Select the `main` branch as the build source and click **Save**. Your site will be published at `https://<your-username>.github.io/<repo-name>/`.
