# Practical Journal Generator

A professional, 100% database-free, browser-based **Single Page Application (SPA)** designed for college Computer Science teachers and students to create, edit, preview, print, and export academic practical journals.

---

## 🌟 Key Features

* **100% Database-Free & Server-Free**: Runs entirely in the browser using HTML5, CSS3, Bootstrap 5, and Vanilla JavaScript. No PHP, Node.js, MySQL, or cloud backend required.
* **Preloaded Academic Subject**: Preloaded with **Prompt Engineering Practical** (Academic Year 2026-27) for **Yashwantrao Chavan Mahavidyalaya, Islampur**, containing Experiments 21 to 40.
* **Experiment 21 Pre-populated**: Full sample academic content pre-filled (Aim, Problem Analysis, Concept, Algorithm, Monospace Prompts, Sample Input, Expected Output, Observation, Conclusion, Viva Questions with Answers, and References).
* **Flexible Experiment Sizing**: Create practical journals for any number of experiments (5, 10, 15, 20, 30, 40, 50, etc.) with custom starting numbers (e.g., Practical 21 to 40).
* **Multiple Subject Templates**:
  * *Prompt Engineering Practical*
  * *Generic Practical*
  * *Programming Practical (C, C++, Java, Python)*
  * *AI / Machine Learning Practical*
  * Plus customizable sections per experiment
* **Dynamic Viva Q&A & References**: Add unlimited concept-checking questions with answers. Reorder, edit, and delete them freely.
* **Show/Hide Viva Answers**: Exam and student viva workbook toggle: hides answers and renders ruled blank lines (`Answer: ______________________`) for written tests.
* **Dynamic Custom Sections**: Add subject-specific sections such as *Theory*, *Hardware Requirements*, *Procedure*, *Dataset*, or *Results* with drag-and-drop reordering.
* **Live Auto-Save**: Seamless debounced auto-save (750 ms) to browser `LocalStorage` with visual status indicator (`Saving...` → `✓ Saved`).
* **Multi-Journal Management**: Store and switch between multiple subjects (e.g. *Prompt Engineering*, *Python Practical*, *Java Lab*, *DBMS*, *Machine Learning*).
* **Instant Search & Filter**: Real-time search across experiment numbers, titles, and section contents.
* **Batch Import Tools**:
  * Paste numbered text syllabus lists (e.g., `21. Basic Prompts...`) to auto-create experiments.
  * Upload CSV files (`experiment_number,title`).
* **Academic Cover Page & Index**: Auto-generated A4 cover page with college logo, student credentials, and dynamic index table.
* **Print & Client-Side PDF**: Professional `@media print` layout with strict A4 page breaks, clean academic typography, and one-click PDF export.
* **Offline PWA Support**: Includes `manifest.json` and `service-worker.js` for full offline availability.

---

## 🚀 Quick Start / Installation

**No build steps, no installation, and no dependencies are required.**

Simply double-click or open:

```text
index.html
```

in any modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari, Brave).

---

## 🌐 Hosting Instructions

Because this is a pure static client-side application, you can host it for free on any static web hosting platform:

### 1. GitHub Pages
1. Push this repository or folder to GitHub.
2. Go to **Settings** > **Pages**.
3. Under **Branch**, select `main` (or `master`) and directory `/ (root)`.
4. Click **Save**. Your site will be live within seconds at `https://<username>.github.io/<repo>/`.

### 2. Netlify
1. Log in to [Netlify](https://www.netlify.com/).
2. Drag and drop this folder directly into the **Netlify Drop** dashboard.
3. Your application is immediately published on a secure global CDN with HTTPS.

### 3. Cloudflare Pages
1. In Cloudflare dashboard, go to **Workers & Pages** > **Create application** > **Pages**.
2. Connect your Git repository or upload the static folder.
3. Leave build command blank and output directory as root `/`.
4. Click **Deploy site**.

### 4. Vercel
1. Install Vercel CLI (`npm i -g vercel`) or connect via GitHub on [vercel.com](https://vercel.com).
2. Run `vercel` in this folder, or import the GitHub repository.
3. Deploy as a static project.

---

## 💾 Backup & Data Persistence

### ⚠️ Important Storage Note
> **Data Security & Device Isolation**: All practical journals are saved directly to your browser's `LocalStorage`. Data is stored locally on that specific computer and browser profile. Clearing browser cache/cookies will delete local journals.

### Transferring or Backing Up Data:
1. **Export Current Journal**:
   * Navigate to **Export / Import** > click **Export Current Journal**.
   * Downloads a `.json` file containing all experiments, sections, viva questions, and references.
2. **Import Journal**:
   * Under **Export / Import**, click **Choose File** next to *Import Journal from JSON*.
   * Select your previously exported `.json` file to restore it immediately.
3. **Backup All Journals**:
   * Click **Backup All Journals** to download `practical-journal-backup.json` containing every journal in your browser database.
   * Click **Restore Backup** on any computer to restore all journals.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>S</kbd> | Save journal immediately |
| <kbd>Ctrl</kbd> + <kbd>P</kbd> | Open Print / PDF Preview |
| <kbd>Ctrl</kbd> + <kbd>F</kbd> | Focus Experiment search box |
| <kbd>Ctrl</kbd> + <kbd>Enter</kbd> | Navigate to next experiment in editor |
| <kbd>Tab</kbd> *(inside code editor)* | Inserts 4 spaces indentation (prevents losing focus) |

---

## 📁 Project Structure

```text
c:\AI_LAB/
│
├── index.html              # Main single page application
│
├── css/
│   ├── style.css           # Clean responsive academic interface styling
│   └── print.css           # A4 academic print stylesheet with strict page breaks
│
├── js/
│   ├── storage.js          # LocalStorage persistence & auto-save debouncing
│   ├── templates.js        # Practical journal templates (Prompt Eng, Programming, AI/ML)
│   ├── journal.js          # Journal model, preloaded default data, logo reader
│   ├── experiments.js      # Experiment CRUD, generation, viva questions, references
│   ├── preview.js          # A4 cover page, contents index, viva toggle, print & PDF
│   ├── import-export.js    # JSON export/import, CSV parser, batch text list parser
│   ├── settings.js         # User preferences and formatting toggles
│   └── app.js              # Application controller, routing, shortcuts, modals
│
├── assets/
│   ├── images/             # Image assets directory
│   └── icons/              # App SVG icon
│       └── icon.svg
│
├── manifest.json           # PWA Web App Manifest
├── service-worker.js       # Offline cache service worker
└── README.md               # User manual and documentation
```

---

## 🎓 Academic Integrity & General Purpose Use

While this application comes preloaded with the **Prompt Engineering Practical** for Yashwantrao Chavan Mahavidyalaya, Islampur (Experiments 21–40), it is a **universal tool** suitable for any discipline:

* C / C++ Programming
* Java & Object-Oriented Programming
* Python Programming & Data Structures
* Database Management Systems (DBMS)
* Operating Systems & Linux
* Computer Networks & Web Technology
* Big Data & Hadoop
* Artificial Intelligence & Machine Learning
* Mobile Application Development

To create a new journal for any subject, click **+ New Journal** on the Dashboard, select your preferred template, and start writing!
