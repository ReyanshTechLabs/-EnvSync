 # 🔐 EnvSync

> Stop breaking apps because of missing `.env` variables.

---

## ⚡ Overview

**EnvSync** is a simple and powerful CLI tool that helps developers manage environment variables across projects.

It ensures your `.env` file stays consistent with `.env.example`, preventing common issues like missing variables, broken setups, and inconsistent environments.

---

## 🔥 Features

### ✅ Core Features

* Detect missing environment variables
* Detect extra/unused variables
* Compare `.env` with `.env.example`
* Clean CLI output

---

### 🚀 Advanced Features

* `envsync init` → Create `.env` from `.env.example`
* `envsync check` → Validate environment variables
* `envsync sync` → Auto-fix missing variables
* Type validation (number, string, boolean)
* Git hook support (prevent bad commits)
* Team-friendly workflow

---

## 📁 Required Files

### `.env.example` (tracked in Git)

```env
API_KEY=
DB_URL=
PORT=
```

### `.env` (ignored in Git)

```env
API_KEY=abc123
PORT=3000
```

---

## 🚀 Installation

```bash
npm install -g envsync
```

or

```bash
npx envsync
```

---

## 🛠️ Commands

### 🔹 Initialize `.env`

```bash
envsync init
```

Creates `.env` from `.env.example`.

---

### 🔹 Check environment

```bash
envsync check
```

Example output:

```
❌ Missing variables:
- DB_URL

⚠️ Extra variables:
- UNUSED_KEY
```

---

### 🔹 Sync environment

```bash
envsync sync
```

Adds missing variables automatically to `.env`.

---

## 🧠 Validation (Optional)

You can define types in `.env.example`:

```env
PORT=number
DEBUG=boolean
API_KEY=string
```

EnvSync will validate values in `.env`.

---

## 🔄 Workflow

1. Clone project
2. Run:

```bash
envsync init
```

3. Add values to `.env`
4. Validate:

```bash
envsync check
```

---

## 🔗 Git Hook (Recommended)

Prevent broken commits:

```bash
envsync check
```

Use in pre-commit hook to ensure all variables exist.

---

## 💡 Why EnvSync?

Because:

* Missing `.env` variables waste time 😤
* Teams struggle with config sync 😵
* Debugging becomes painful 😑

EnvSync fixes all of that.

---

## 🌍 Use Cases

* Backend applications
* Frontend apps (React, Next.js)
* DevOps workflows
* Team collaboration

---

## 🤝 Contributing

Contributions are welcome!

* Add validation rules
* Improve CLI
* Add integrations

---

## ⭐ Support

If this helps you:

* Star ⭐ the repo
* Share 🚀
* Use it in your projects

---

## 💥 Vision

To make environment configuration **reliable, consistent, and effortless** for developers everywhere.
