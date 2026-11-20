# 🏠 HOSTEL360 — The Smarter Way to Live

> One place for hostel complaints with a **48-hour accountability clock**, **one-tap SOS**, **daily water (TDS) monitoring**, and a **live health score for every hostel block**.

Built for **PromptWars**. Zero dependencies, zero build step: a single `index.html` you can open in any browser.

---

## 🔴 The Problem

- Hostel complaints vanish into WhatsApp groups and paper registers; nobody is accountable.
- Water quality is invisible until students fall sick.
- In an emergency (ragging, fire, medical) students make phone calls and hope someone picks up.
- Wardens have no single view of how each block is actually performing.

## ✅ The Solution

HOSTEL360 gives **students, staff, wardens and admins** one shared system where every issue has an owner, a deadline and an audit trail.

## ⭐ Signature Features

| # | Feature | What it does |
|---|---------|--------------|
| 1 | **Live Hostel Health Score** | Weighted 0–100 score per block: cleaning 20%, water 15%, complaint resolution 25%, food 20%, infrastructure 15%, feedback 5%. Resolution quality counts more than fewer complaints, so reporting is never punished. |
| 2 | **One-tap SOS** | Confirm-and-send alert (medical, ragging/safety, fire, security) to warden + staff with block and room, a false-alarm cancel, and an audit log. |
| 3 | **Water Intelligence** | Staff log daily TDS per block; trend chart with warning (300 ppm) and critical (500 ppm) thresholds; "reading missing today" flag. |
| 4 | **AI complaint assistant** | Type a problem in plain words, get category, priority, department, next action and duplicate warnings. *(Rule-based in this demo.)* |
| 5 | **Fair performance leaderboard** | Blocks ranked by health score; staff earn credits for on-time fixes. Warden approves awards. |

## 🧰 Everything Else

- **48-hour auto-escalation**: unresolved complaint → warden alerted, assigned staff lose credits (configurable), logged in audit.
- **Credit system**: +3 credits for on-time resolution, −5 for escalation (admin-configurable).
- **Complaint lifecycle**: Submitted → Acknowledged → Assigned → In Progress → Resolved, with student rating and reopen.
- **Privacy-aware routing**: *Staff behaviour* and *Peer complaints* go only to the warden, never shown to staff.
- **Mess**: weekly menu, online food ordering with time slots, "Ready for Collection" notification, one verified rating per order.
- **Facility booking**: basketball, tennis, gym, pool, gaming room, TV hall, with double-booking prevention.
- **Lost & Found**: post, search, claim, warden-verified hand-over.
- **Announcements and notifications** per role.
- **Dark mode**, responsive layout, keyboard-focus styles, `prefers-reduced-motion` support.

## 👥 Four Roles

| Role | Can do |
|------|--------|
| Student | File complaints, SOS, order food, book facilities, rate fixes, lost & found |
| Staff | See assigned tasks, log TDS, process food orders, earn credits |
| Warden | Overview, assign and escalate, handle SOS, leaderboard, announcements |
| Admin | Everything the warden can, plus thresholds/rules config and audit log |

## 🚀 Try It (30 seconds)

**Option A — Open locally**
1. Download or clone this repo.
2. Double-click `index.html`.

**Option B — Live on GitHub Pages**
1. Go to **Settings → Pages**.
2. Source: **Deploy from a branch** → `main` → `/ (root)` → **Save**.
3. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

### Demo logins (password for all: `demo123`)

| Role | Email |
|------|-------|
| Student (Aarav, Block A) | `student@hostel360.demo` |
| Staff (Ramesh) | `staff@hostel360.demo` |
| Warden (Dr. Iyer) | `warden@hostel360.demo` |
| Admin | `admin@hostel360.demo` |

The login page also has one-tap buttons for each role.

### 🎬 Suggested judge walkthrough (2 minutes)
1. **Student** → press **EMERGENCY SOS** → confirm.
2. **Student → Complaints** → type *"bathroom dirty for three days, nobody cleaned"* → watch the assistant classify it → submit.
3. Sign out → **Warden → Emergencies** → acknowledge the SOS.
4. **Warden → Complaints** → click **Simulate +49 hours** → see auto-escalation and credit deduction.
5. **Warden → Leaderboard** → approve a block award.
6. Toggle **dark mode** 🌙.

## 🏗️ Tech

- Vanilla HTML + CSS + JavaScript, **no framework, no build, no backend**
- State persisted in browser `localStorage`
- Inline SVG for health rings and TDS charts
- Accessible by design: ARIA labels, focus rings, reduced-motion support

## ⚠️ Honest Status (Demo Build)

- Data and sign-in live in your browser (`localStorage`); there is **no server**, no real SMS/push, and no real TDS sensors.
- The "AI assistant" is **rule-based**, not an LLM.
- TDS monitoring is an **indicator only**, not a drinking-water safety certification; lab testing is still required.
- Escalation runs when the app loads and on a 60-second tick.

## 🗺️ Roadmap

- [ ] Backend (Supabase / Firebase) with real authentication
- [ ] LLM-powered complaint triage (replace the rule-based assistant)
- [ ] IoT TDS sensor ingestion
- [ ] SMS / WhatsApp / push notifications
- [ ] Year-end credit report export for wardens
- [ ] Multi-hostel support

## 📁 Repo Structure

```
.
├── index.html     # the entire app
├── README.md
├── LICENSE
├── .gitignore
└── docs/
    └── HOSTEL360_Pitch.pptx
```

## 📄 License

MIT. See [LICENSE](LICENSE).
