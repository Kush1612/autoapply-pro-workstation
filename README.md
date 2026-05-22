# ⚡ AutoApply Pro — Developer API Control Center

AutoApply Pro is a premium, single-screen **Developer API Control Center & Script Generator** designed to streamline candidate profile mapping and automated job application loops. This interactive dashboard assists developers in constructing, validating, and testing backend integration requests across 10 major portals.

## 🌐 Live Deployed Application
The application is fully live and hosted on the Google Cloud edge CDN:
👉 **[https://autoapply-pro-workstation.web.app](https://autoapply-pro-workstation.web.app)**

---

## 💻 Workstation Architecture

The interface is structured as a **3-column unified workspace**:

1. **Column 1: Configuration Pane (Left)**
   - **Load Developer Models:** Instantly pre-fill profiles with `.NET Dev`, `Java Dev`, `Full-Stack`, or `Fresher` configurations, or start with a clean **Blank/Custom** layout.
   - **Gmail Account Connector:** Simulate the Google API Consent flow to authorize credentials and listen for confirmation OTP codes/sync tokens.
   - **Candidate Profile & Specs:** Customize names, phone numbers, target roles (supports editable free-form text with datalists), qualifications, and technology stacks.

2. **Column 2: Portal Application Center (Middle)**
   - **Selected Portal Queue:** Manually select or deselect specific channels for direct posting.
   - **Granular API Testers:** Independently trigger simulated `⚡ Sign Up API` and `📮 Apply API` loops.
   - **Master Sequence Trigger:** Initiate the master automation sequence with automated progress bars and stat metrics.

3. **Column 3: Developer Terminal & API Playground (Right)**
   - **Live Terminal Console:** View real-time HTTP requests, response payloads, activation sync notifications, and visual countdowns.
   - **API Code Generator:** Dynamically compiles the active portal's parameters into copyable code blocks:
     - **cURL Request Command**
     - **Node.js Axios Script**
     - **Python Requests Script**
     - **JSON Payload & Raw Response Schema**

---

## 🚀 Key Features

- **No Invasive Page-Load Triggers:** The `Auto-run pipeline on load` toggle is unchecked by default to preserve a clean and self-directed user experience.
- **Visual Countdown Sequences:** Refreshes and pipeline starts display an interactive countdown inside the terminal logs.
- **Auto-Resolving OTP Dialogs:** During automated executions, a beautiful simulation modal extracts and auto-injects OTP activation tokens within a visual 3-second countdown.
- **Direct Tab-Opening Integrations:** Pre-fills queries and automatically launches candidate searches in a new browser tab for each active portal target.

---

## 📦 Local Installation & Setup

Since the application is purely client-side static HTML/CSS/JavaScript, you can run it directly:

1. Clone this repository:
   ```bash
   git clone https://github.com/Kush1612/autoapply-pro-workstation.git
   ```
2. Open `auto_job_portal.html` directly in your web browser, or serve it using a local developer server.

---

## 🌐 Firebase Hosting & Edge Deploy

This repository is pre-configured with static hosting configuration files:
- **`firebase.json`**: Configures static edge rewrite rules mapping `/` directly to `auto_job_portal.html`.
- **`.firebaserc`**: Hooks up the default hosting deployment context to the Firebase project: `autoapply-pro-workstation`.

To deploy changes live:
```bash
npx -y firebase-tools@latest deploy --only hosting
```
