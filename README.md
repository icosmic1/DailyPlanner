# Cosmic Planner — by Abhishek

A premium daily planner with push notifications, animations, sounds, and confetti. Single HTML file, no backend, no account needed.

## Features
- **Personalized greeting** — asks your name, greets by time of day
- **Cosmic splash screen** — first-time branded banner
- **Sound effects** — pops, ticks, whooshes, and a celebration fanfare (Web Audio API)
- **Confetti** — canvas particle burst on successful scheduling
- **Animations** — slide-in/out tasks, tag pulses, shimmer button, staggered cards
- **Glassmorphism** — frosted glass cards with gradient borders
- **Push notifications** via ntfy — with "Done / Not yet" action buttons
- **Motivational pushes** — tap "Not yet" and get a push 30 min later
- **Progress bar** — animated scheduling progress

## How It Works

```
Morning → Safari auto-opens your planner URL
    ↓
Personalized greeting: "Good morning, Abhishek!"
    ↓
Add tasks + times → Hit "Schedule My Day"
  (shimmer animation + tick sounds + progress bar)
    ↓
🎉 Confetti + fanfare!
    ↓
At each task time → iPhone push:
  "Hey Abhishek! Have you completed Exercise?"
    ↓
  [Done ✅]  →  "Great job!" notification
  [Not yet 😅] → Motivational push 30 min later
```

---

## Setup

### Step 1: Install ntfy on iPhone
1. App Store → search **"ntfy"** → install
2. Open ntfy → tap **+** → enter a unique channel name (e.g. `abhishek-cosmic-123`)
3. Tap **Subscribe**

### Step 2: Host the page
**Option A — Netlify Drop (30 seconds, free)**
1. Go to https://app.netlify.com/drop
2. Drag the `habit-reminder` folder → done
3. You get a URL like `https://random-name.netlify.app`

**Option B — GitHub Pages (free)**
1. Create repo, upload `index.html`
2. Settings → Pages → Source: main → Save
3. URL: `https://username.github.io/repo-name/`

### Step 3: iPhone Automation (daily at 8 AM)
1. **Shortcuts** app → **Automation** → **+**
2. Trigger: **Time of Day** → **8:00 AM** → **Daily**
3. **Run Immediately**: ON
4. Action: **Open URL** → paste your hosted URL
5. Done

### Step 4: Add to Home Screen (optional)
1. Open URL in Safari → Share → **Add to Home Screen**
2. Name it "Cosmic Planner" → Add

---

## Privacy
- No accounts, no tracking, no data collection
- Tasks stored in browser localStorage only
- ntfy channels are random strings (like passwords)
- Everything runs client-side

---

## Tech Stack
- Single HTML file (~700 lines)
- Web Audio API for sounds
- Canvas API for confetti
- CSS animations + glassmorphism
- ntfy.sh for push notifications
- Zero dependencies, zero build step
