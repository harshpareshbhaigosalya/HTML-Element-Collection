# HTML Element Collection

<div align="center">
  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Artist%20Palette.png" alt="Artist Palette" width="100" height="100" />

  <h1 align="center">HTML Element Collection</h1>

A community-driven, open-source library of beautiful, reusable UI components built with plain HTML, CSS and vanilla JavaScript.

  <p align="center">
    <a href="https://github.com/Shubham713-lab/HTML-Element-Collection"><strong>Explore the Components »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Shubham713-lab/HTML-Element-Collection/issues/new?assignees=&labels=bug&template=bug_report.md&title=">Report Bug</a>
    ·
    <a href="https://github.com/Shubham713-lab/HTML-Element-Collection/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=">Request Feature</a>
  </p>
</div>

<div align="center">

![GitHub contributors](https://img.shields.io/github/contributors/Shubham713-lab/HTML-Element-Collection?color=blue\&style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/Shubham713-lab/HTML-Element-Collection?color=green\&style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/Shubham713-lab/HTML-Element-Collection?color=yellow\&style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/Shubham713-lab/HTML-Element-Collection?color=orange\&style=for-the-badge)
![MIT License](https://img.shields.io/github/license/Shubham713-lab/HTML-Element-Collection?color=red\&style=for-the-badge)

</div>

---

## 📖 Table of Contents

* [About The Project](#-about-the-project)
* [🚀 Getting Started](#-getting-started)
* [⚙️ Project Structure](#️-project-structure)
* [🔧 Component Template (Copy-Paste Ready)](#-component-template-copy-paste-ready)
* [🤝 How to Contribute](#-how-to-contribute)
* [📜 Contribution Guidelines](#-contribution-guidelines)
* [🧪 Testing Locally](#-testing-locally)
* [✨ Our Contributors](#-our-contributors)
* [📄 License](#-license)

---

## 🎯 About The Project

HTML Element Collection is a curated collection of small, self-contained UI components — buttons, cards, forms, loaders, modals and more — that are:

* **Vanilla-first:** no frameworks required — plain HTML, CSS and JavaScript.
* **Self-contained:** each component lives in its own folder and works standalone.
* **Accessible:** simple ARIA + keyboard support for interactive components.
* **Learner-friendly:** ideal for beginners to learn real-world component structure.

Use the components as-is or copy them into your projects.

---

## 🚀 Getting Started

### Prerequisites

* Git
* A modern web browser

### Quick start (fork → contribute)

```bash
# 1. Fork the repo on GitHub
# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/HTML-Element-Collection.git
cd HTML-Element-Collection

# 3. Create a branch for your component
git checkout -b feat/<your-component-name>
```

Add your component under `components/<your-component-name>/` and follow the component template below.

---

## ⚙️ Project Structure

```
HTML-Element-Collection/
├─ components/
│  ├─ button-fancy/
│  │  ├─ index.html
│  │  ├─ style.css
│  │  └─ script.js
│  └─ card-profile/
│     ├─ index.html
│     ├─ style.css
│     └─ script.js
├─ .github/
│  ├─ ISSUE_TEMPLATE/
│  └─ PULL_REQUEST_TEMPLATE.md
├─ demo/           # Optional demo pages that showcase multiple components together
├─ LICENSE
└─ README.md
```

---

## 🔧 Component Template (Copy-Paste Ready)

> Put each component inside `components/<component-name>/` with the three files below.

### `index.html`

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Component — My Component</title>
  <link rel="stylesheet" href="./style.css" />
</head>
<body>

  <!-- COMPONENT MARKUP -->
  <div class="my-component" role="region" aria-label="My sample component">
    <button class="my-component__btn">Click me</button>
    <div class="my-component__output" aria-live="polite"></div>
  </div>

  <script src="./script.js" defer></script>
</body>
</html>
```

### `style.css`

```css
:root {
  --accent: #6366f1; /* Indigo-500 */
  --radius: 10px;
}

.my-component {
  font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
  display: inline-block;
  padding: 1rem;
  border-radius: var(--radius);
  box-shadow: 0 6px 18px rgba(0,0,0,0.06);
}

.my-component__btn {
  background: linear-gradient(90deg, var(--accent), #8b5cf6);
  color: white;
  border: none;
  padding: 0.6rem 1rem;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 600;
}

.my-component__btn:focus {
  outline: 3px solid rgba(99,102,241,0.18);
}

.my-component__output {
  margin-top: 0.75rem;
  color: #374151;
}
```

### `script.js`

```js
const btn = document.querySelector('.my-component__btn');
const out = document.querySelector('.my-component__output');

btn.addEventListener('click', () => {
  out.textContent = 'Thanks for clicking — component works! ✨';
});
```

---

## 🤝 How to Contribute

We welcome contributions of any size. Follow these steps for a smooth PR:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feat/your-component-name`.
3. Add a folder inside `components/your-component-name/` with `index.html`, `style.css`, and `script.js`.
4. Ensure your component is **self-contained** and uses only relative imports.
5. Add a short README inside the component folder (`components/your-component-name/README.md`) that explains how to use it and any customization variables.
6. Commit & push: `git add . && git commit -m "feat: add my-component" && git push origin feat/your-component-name`.
7. Open a Pull Request against `main` and choose the appropriate PR template.

### PR Template (suggested contents)

* Title: `feat(component-name): short description`
* Description: what the component is and how to use it
* Screenshot/GIF: Add an animated gif or screenshot if possible
* Accessibility notes: keyboard controls, ARIA attributes used
* Checklist:

  * [ ] Component is self-contained
  * [ ] No external dependencies
  * [ ] Mobile responsive
  * [ ] Accessible

---

## 📜 Contribution Guidelines

* **One component per PR.** Keep PRs focused.
* **Naming:** Use kebab-case for folder names (e.g. `card-profile`).
* **Style:** Keep CSS scoped to the component — use a unique prefix to avoid collisions.
* **No build step:** Components should work by opening `index.html` in the browser.
* **Documentation:** Add `README.md` inside the component folder with usage and options.

---

## 🧪 Testing Locally

Open the component's `index.html` directly in the browser. For a nicer developer experience, you can use a simple static server. Example using `http-server`:

```bash
# Install once
npm i -g http-server

# Serve the project root
http-server -c-1 .
# Then open http://127.0.0.1:8080/components/<your-component-name>/
```

---

## ✨ Example Components (ideas)

* Fancy button
* Responsive card
* Toggle switch (accessible)
* Modal dialog (with focus trap)
* Toast notifications
* Form input with validation
* Skeleton loaders

If you want, I can create a few ready-made example components and open PR-ready code for you.

---

## ✍️ Style & Accessibility Tips

* Use semantic HTML (buttons, inputs, lists).
* Keyboard support: `Enter` / `Space` for buttons, `Esc` to close modals.
* Add `aria-label`, `role` and `aria-live` where applicable.
* Keep focus visible and logical.

---

## ✨ Our Contributors

A huge thank you to everyone who contributed!

<!-- contributors image auto-generated -->

<p align="center">
  <a href="https://github.com/Shubham713-lab/HTML-Element-Collection/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=Shubham713-lab/HTML-Element-Collection" alt="contributors" />
  </a>
</p>

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="right"><a href="#top">Back to Top ↑</a></p>
