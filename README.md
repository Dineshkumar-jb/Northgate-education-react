<h1 align="center">
  <br>
  🎓 Northgate Education
  <br>
</h1>

<p align="center">
  <strong>A modern, full-featured education consultancy website</strong><br>
  Built with React 19 · Vite 8 · Firebase · EmailJS
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=white" alt="React 19" />
  <img src="https://img.shields.io/badge/Vite-8-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite 8" />
  <img src="https://img.shields.io/badge/Firebase-12-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img src="https://img.shields.io/badge/EmailJS-4-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="EmailJS" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Running Locally](#running-locally)
- [Building for Production](#-building-for-production)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Overview

**Northgate Education** is a professional, single-page React application for an overseas education consultancy. It provides prospective students with everything they need to begin their study-abroad journey — from exploring top university destinations and service offerings, to submitting an inquiry directly from the website.

The platform features a built-in AI-powered chatbot, animated alumni testimonials, exam guidance, a university showcase, and a fully integrated contact form backed by **Firebase Firestore** (for data persistence) and **EmailJS** (for instant email notifications).

---

## 🚀 Live Demo

> 🔗 **[View Live Site](https://nullframe.github.io/northgate-education-react)** _(update this link after deployment)_

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 **AI Chatbot** | Keyword-driven chatbot powered by a local JSON knowledge base |
| 📩 **Contact Form** | Fully validated form with Firebase Firestore logging + EmailJS email delivery |
| 🎓 **Alumni Slider** | Auto-scrolling testimonials carousel with real student stories |
| 🏫 **University Showcase** | Curated grid of top partner universities |
| 🌍 **Study Destinations** | Interactive destination cards with key country highlights |
| 📚 **Exam Guidance** | Dedicated section covering IELTS, TOEFL, SAT, PTE and more |
| 📱 **Fully Responsive** | Mobile-first design — looks great on all screen sizes |
| ⚡ **Performance-First** | Vite 8 bundler with lightning-fast HMR in development |
| 🔒 **Secure Config** | All API credentials managed via environment variables |

---

## 🛠 Tech Stack

### Frontend
- **[React 19](https://react.dev/)** — Latest React with concurrent features
- **[Vite 8](https://vite.dev/)** — Ultra-fast build tooling and dev server
- **Vanilla CSS** — Custom design system with CSS variables and animations

### Backend Services
- **[Firebase 12 (Firestore)](https://firebase.google.com/)** — NoSQL database for storing inquiry submissions
- **[EmailJS 4](https://www.emailjs.com/)** — Client-side email dispatch (no backend server required)

### Developer Tooling
- **[Oxlint](https://oxc.rs/docs/guide/usage/linter.html)** — Blazing-fast JavaScript linter written in Rust

---

## 📁 Project Structure

```
northgate-education-react/
├── public/                  # Static public assets
├── src/
│   ├── assets/              # Images, icons, and media
│   ├── components/          # All React UI components
│   │   ├── Navbar.jsx
│   │   ├── Hero.jsx
│   │   ├── About.jsx
│   │   ├── Services.jsx
│   │   ├── Universities.jsx
│   │   ├── Destinations.jsx
│   │   ├── Exams.jsx
│   │   ├── Alumni.jsx
│   │   ├── Testimonials.jsx
│   │   ├── Process.jsx
│   │   ├── Trust.jsx
│   │   ├── FAQ.jsx
│   │   ├── ContactForm.jsx
│   │   ├── Chatbot.jsx
│   │   ├── CtaBanner.jsx
│   │   ├── SatModal.jsx
│   │   ├── WhatsAppButton.jsx
│   │   └── Footer.jsx
│   ├── data/
│   │   └── chatbotKB.json   # Chatbot knowledge base
│   ├── firebase.js          # Firebase SDK initialization
│   ├── App.jsx              # Root component & layout
│   ├── App.css              # Global component styles
│   ├── index.css            # Design system & CSS variables
│   └── main.jsx             # React DOM entry point
├── .env.example             # Environment variable template
├── .gitignore
├── index.html               # Vite HTML entry point
├── package.json
└── vite.config.js
```

---

## 🏁 Getting Started

### Prerequisites

Make sure you have the following installed:

- **Node.js** `>= 18.x` — [Download here](https://nodejs.org/)
- **npm** `>= 9.x` (comes with Node.js)
- A **Firebase** project with Firestore enabled
- An **EmailJS** account with a configured service and template

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Dineshkumar-jb/northgate-education-react.git
   cd northgate-education-react
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

### Environment Variables

This project requires API credentials for Firebase and EmailJS. These are **never** committed to the repository.

1. Copy the example file:
   ```bash
   cp .env.example .env
   ```

2. Open `.env` and fill in your credentials:
   ```env
   # Firebase Web Client Credentials
   VITE_FIREBASE_API_KEY=your_firebase_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
   VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
   VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
   VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
   VITE_FIREBASE_APP_ID=your_firebase_app_id
   VITE_FIREBASE_MEASUREMENT_ID=your_firebase_measurement_id

   # EmailJS Credentials
   VITE_EMAILJS_PUBLIC_KEY=your_emailjs_public_key
   VITE_EMAILJS_SERVICE_ID=your_emailjs_service_id
   VITE_EMAILJS_TEMPLATE_ID=your_emailjs_template_id
   ```

> ⚠️ **Never commit your `.env` file.** It is already listed in `.gitignore`.

### Running Locally

```bash
npm run dev
```

The app will be available at **http://localhost:5173**

---

## 📦 Building for Production

```bash
npm run build
```

The optimized output will be generated in the `dist/` folder, ready to be served by any static hosting provider.

To preview the production build locally:
```bash
npm run preview
```

---

## 🚢 Deployment

This project is deployed via **GitHub Pages** using the `dist/` output.

### Deploy to GitHub Pages

1. Install the GitHub Pages deploy tool (if not already):
   ```bash
   npm install --save-dev gh-pages
   ```

2. Add the following to `package.json`:
   ```json
   "homepage": "https://Dineshkumar-jb.github.io/northgate-education-react",
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```

3. Deploy:
   ```bash
   npm run deploy
   ```

> 💡 Remember to configure your **Firebase Console** and **EmailJS** dashboard to allow requests from your GitHub Pages domain.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'feat: add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ for <strong>Northgate Education</strong>
</p>
