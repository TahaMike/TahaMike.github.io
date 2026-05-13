# 🚀 AI-Driven QA Portfolio | Mohammad Taha

A high-performance, modern portfolio built with **React**, **Vite**, and **Tailwind CSS v4**. This project showcases my journey as a B.Tech IT graduate and QA Specialist, focusing on the intersection of manual testing, AI implementation, and software excellence.

**🌐 Live Demo:** https://TahaMike.github.io)

---

## 🛠️ Tech Stack

* **Framework:** React 18 (TypeScript)
* **Build Tool:** Vite 7 (High-performance HMR)
* **Styling:** Tailwind CSS v4 (Using the new Oxide engine)
* **Animations:** Framer Motion
* **Icons:** Lucide React
* **Deployment:** GitHub Pages (Manual & automated workflows)

---

## 🧠 Development Challenges & QA Solutions

Building this portfolio served as a real-world testing ground for environment configuration and integration.

### 1. The Virtual Environment (venv) Conflict
* **Problem:** Running `npx tailwindcss init` inside a Python `venv` caused an "executable not found" error because the shell was prioritizing the virtual environment's path over the node_modules path.
* **Solution:** Identified the pathing conflict inherent in Mac/Vite environments. Resolved by manually configuring `tailwind.config.js` and later upgrading to **Tailwind v4** via the `@tailwindcss/vite` plugin to bypass legacy PostCSS dependencies.

### 2. Form Backend Integration (Serverless)
* **Problem:** GitHub Pages is a static hosting service, meaning there is no backend to process the "Contact Me" form data.
* **Solution:** Integrated the **Formspree API**. I refactored the frontend logic from a simple local state to an asynchronous `fetch` request with error handling (`async/await`), ensuring the UI provides real-time feedback (Sending/Success/Error states) to the user.

### 3. Production Pathing (Vite Build)
* **Problem:** Initially faced issues with assets not loading on the root domain (`TahaMike.github.io`).
* **Solution:** Configured the `base` property in `vite.config.ts` to `'/'` to ensure absolute pathing for the production-ready `dist` folder.

---

## 🏆 Key Achievements

* **Venv-Node Synergy:** Successfully managed a Node.js development workflow inside a Python-centric terminal environment.
* **CI/CD Awareness:** Implemented a build-and-deploy pipeline using `gh-pages` and manual asset management to ensure version control integrity.
* **QA Mindset:** Applied rigorous testing to the UI, ensuring smooth scrolling, mobile responsiveness, and cross-browser compatibility.
* **Modern CSS:** Utilized the latest Tailwind CSS v4 features, reducing bundle size and improving build speed by leveraging Rust-based engine optimization.

---

## 📂 Project Structure

```text
├── dist/               # Optimized production build
├── src/
│   ├── App.tsx         # Main portfolio logic & components
│   ├── index.css       # Tailwind v4 imports & custom styles
│   └── main.tsx        # React entry point
├── vite.config.ts      # Vite & Tailwind plugin configuration
└── package.json        # Project dependencies & scripts
