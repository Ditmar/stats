# 🌟 GitHub PR Ranking - stats

A lightweight web application that allows you to register and track GitHub repositories, displaying a ranking based on the number of **merged pull requests**.

## 🎯 Purpose

To provide a visual and simple way to:

* Register and manage GitHub repositories.
* Fetch and display statistics about merged pull requests.
* Compare collaboration levels across different repositories.

---

## 🛠️ Tech Stack

* **Astro** (frontend framework)
* **React** (UI components)
* **MUI** (Material UI for styling)
* **GitHub REST API v3** (data source)

> 🔎 No backend or database is used. All data is fetched live from the GitHub API.

---

## 📸 Preview

*Add a screenshot or demo GIF here*

---

## 🔍 How It Works

1. The user inputs a GitHub repository URL.
2. The app extracts the `owner` and `repo` names.
3. It calls the GitHub REST API to fetch all closed PRs.
4. Filters PRs with `merged_at != null`.
5. Displays a ranking of all registered repositories.

---

## ✨ Features

* ✅ Add a public GitHub repository
* ✅ Count merged pull requests using GitHub API
* ✅ Sort repositories by merged PR count
* 🚧 Save repository list to local storage (planned)
* 🚧 Show individual PRs (planned)

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/github-pr-ranking.git
cd github-pr-ranking
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the project

```bash
npm run dev
```

The app will be available at `http://localhost:4321`

> ⚠️ Rate limits: GitHub API allows 60 unauthenticated requests/hour per IP. Use a personal access token for higher limits.

---

## 📦 Project Structure (Astro)

```
/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── lib/github.ts   # GitHub API logic
│   └── styles/
├── astro.config.mjs
└── package.json
```

---

## 📌 Example GitHub API Query

```
GET https://api.github.com/repos/{owner}/{repo}/pulls?state=closed&per_page=100
```

Then filter each pull request where `merged_at != null`.

---

## 📃 License

MIT © 2025 — Kevin Rodríguez
