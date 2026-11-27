# 💸 HisabKitab Pro — Smart Expense Splitter for Hostels & Trips (`SW-15`)

> **A zero-confusion, FinTech expense management & debt simplification web portal built for college hostels, roommates, and group trips.**

[![Track](https://img.shields.io/badge/Problem%20ID-SW--15-indigo)]()
[![Domain](https://img.shields.io/badge/Domain-FinTech%20%2F%20Databases-emerald)]()
[![Deployment](https://img.shields.io/badge/Architecture-Single--File%20Zero--Build-amber)]()

---

## 🎯 Problem Statement (`SW-15`)
Roommates and friends on trips share dozens of small expenses such as groceries, room rent, Wi-Fi, cabs, and food. Keeping track of who owes whom quickly leads to manual calculation errors, confusion, and awkward reminders.

**HisabKitab Pro** solves this by recording shared bills, scanning receipts via OCR, calculating exact net balances, and running a **Greedy Min-Cash-Flow Simplification Engine** to settle all group debts in the minimum number of UPI transfers.

---

## ✨ Key Features

### 1. Core Hackathon Requirements
* **Multi-Group & Persistent Storage:** Create separate groups (*Hostel Squad*, *Weekend Trip*, etc.), switch seamlessly, and persist all data via `localStorage` with JSON Backup Export/Import.
* **Flexible Expense Splitting (`Equal`, `Exact ₹`, `Percentage %`):** Real-time allocation validation guarantees every split reconciles accurately to the rupee before saving.
* **Clear "Who Owes Whom" & Audit Ledger:** Searchable, filterable transaction history by category, payer, and keywords.

### 2. Advanced & Bonus Features
* **Greedy Min-Cash-Flow Debt Simplification:** Reduces complex multi-way debt graphs into the absolute minimum number of settlement payments.
* **Smart Receipt OCR Scanner (`Tesseract.js`):** Upload a photo of any bill/receipt (or test with built-in sample receipts) to auto-detect the merchant and grand total.
* **Exact UPI QR Code Upload & Instant Settle:** Attach your personal or friend's real **GPay / PhonePe / Paytm QR screenshot** directly inside your profile or settlement card for instant scan-and-pay.
* **Real-Time Friend Sync (`Room Code` Sharing):** Generate a 6-character Room Code (`#room=HK-XXXX`) so friends on other devices can join your group and see expenses update live.
* **Start Fresh (`My Real Data` Wizard):** One-click onboarding wizard to clear demo numbers and set up your real profile, UPI ID, and friends directory.
* **Spending Analytics & Printable Monthly Statement:** Interactive SVG category donut chart, out-of-pocket vs. consumed share bars, Dark/Light mode toggle, and a print-ready PDF financial statement.

---

## 🗂️ Repository Structure

Because **HisabKitab Pro** uses a clean, zero-build architecture (Tailwind CSS + Vanilla JS + Tesseract.js + Firebase SDK), your entire repository only needs **3 files**:

```text
hisabkitab-pro-sw15/
├── index.html        # Complete application (Rename expense_splitter.html -> index.html)
├── README.md         # Project documentation, architecture & screenshots
└── LICENSE           # Optional MIT License
```

---

## 🚀 How to Upload & Host Live on GitHub Pages (Step-by-Step)

1. **Rename the HTML File:**
   - Download `expense_splitter.html` from the editor and rename it to **`index.html`** (GitHub Pages automatically serves `index.html` as your homepage).
2. **Create a New Repository on GitHub:**
   - Go to [github.com/new](https://github.com/new) and name it `hisabkitab-pro` (set visibility to **Public**).
3. **Upload Your Files:**
   - Click **Add file → Upload files**, drag in `index.html` and `README.md`, and click **Commit changes**.
4. **Enable Free Live Hosting (GitHub Pages):**
   - Go to your repository's **Settings → Pages**.
   - Under **Build and deployment → Branch**, select **`main`** and folder **`/ (root)`**, then click **Save**.
   - Within ~60 seconds, GitHub will give you a live HTTPS URL (`https://<your-username>.github.io/hisabkitab-pro/`) that you and your friends can open directly on your phones!

---

## 🛠️ Tech Stack
* **Frontend:** HTML5, Tailwind CSS, Responsive Mobile-First UI (Dark & Light Themes)
* **OCR Engine:** Tesseract.js v5 (Client-side receipt text extraction)
* **Algorithms:** Greedy Min-Cash-Flow Graph Settlement, Real-time Split Reconciliation
* **Storage & Sync:** Browser `localStorage`, BroadcastChannel API, Firebase Firestore Realtime Sync