<div align="center">

# 📚 Courses Catalog

**Browse top courses by category, like your favourites and get instant feedback — a React app that fetches live course data from an API.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-courses--catalog.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://courses-catalog.vercel.app)

![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![React Icons](https://img.shields.io/badge/React_Icons-E91E63?style=flat-square&logo=react&logoColor=white)
![React Toastify](https://img.shields.io/badge/React_Toastify-FFCA28?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/Shariq2003/Courses_Catalog?style=flat-square)

[Features](#-features) · [How it works](#-how-it-works) · [Getting Started](#-getting-started) · [Structure](#-project-structure)

</div>

---

## ✨ Features

| | Feature |
|---|---|
| 🌐 | **Live data** fetched from a public courses API on load |
| 🗂️ | **Category filter** — All · Development · Business · Design · Lifestyle |
| ❤️ | **Like / unlike** any course, with a heart toggle |
| 🔔 | **Toast notifications** for likes, unlikes and fetch errors |
| ⏳ | **Loading spinner** while courses are fetched |
| 📝 | **Readable cards** — image, title and a trimmed description |

## 🔄 How it works

```mermaid
flowchart TD
    A(["App mounts"]) --> B["fetch(apiUrl)"]
    B -- "success" --> C["courses grouped by category"]
    B -- "error" --> X["🔔 toast: Error in fetching Courses"]
    C --> F{"Selected category"}
    F -- "All" --> G["Flatten every category"]
    F -- "Development / Business / …" --> H["Only that category"]
    G --> R["Render cards"]
    H --> R
    R --> L["❤️ Like → likedCourses state + toast"]
```

## 🚀 Getting Started

```bash
git clone https://github.com/Shariq2003/Courses_Catalog.git
cd Courses_Catalog
npm install
npm start            # http://localhost:3000
```

<details>
<summary><b>📜 Available scripts</b></summary>

| Command | What it does |
|---|---|
| `npm start` | Run the dev server |
| `npm run build` | Production build into `build/` |
| `npm test` | Run tests |

</details>

## 📁 Project Structure

<details>
<summary><b>Expand tree</b></summary>

```text
src/
├── components/
│   ├── Filter.jsx     # category buttons
│   ├── Cards.jsx      # filters & lists cards, owns likedCourses
│   ├── Card.jsx       # single course + like button
│   └── Spinner.js
├── data.js            # apiUrl + filter categories
└── App.js             # fetch, loading state, layout
```

</details>

---

<div align="center">

Built by **[Shariq](https://github.com/Shariq2003)** · [LinkedIn](https://www.linkedin.com/in/shariq-sd)

⭐ If you like this project, consider giving it a star!

</div>
