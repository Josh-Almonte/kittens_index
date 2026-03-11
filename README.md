# 🐱 Kittens Index

A beginner-friendly dummy repository used to practice basic GitHub operations — cloning, editing, committing, and pushing via SSH.

---

## 🎯 Purpose

This repo helps students learn:

- How to set up SSH access to GitHub
- How to **clone** a repository
- How to **make changes** locally
- How to **commit** and **push** changes back to GitHub
- How to **pull** the latest changes from a remote

---

## 🔑 Step 0 — Set Up SSH Access to GitHub

> Skip this section if you have already configured SSH for GitHub.

1. **Generate an SSH key pair** (if you don't have one):
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
   Press **Enter** to accept the default file location, then optionally set a passphrase.

2. **Copy your public key** to the clipboard:
   ```bash
   # macOS
   pbcopy < ~/.ssh/id_ed25519.pub

   # Linux
   cat ~/.ssh/id_ed25519.pub
   ```

3. **Add the key to GitHub:**
   - Go to **GitHub → Settings → SSH and GPG keys → New SSH key**
   - Paste your public key and save.

4. **Test the connection:**
   ```bash
   ssh -T git@github.com
   ```
   You should see: `Hi <username>! You've successfully authenticated...`

---

## 📥 Step 1 — Clone the Repository

Use SSH (not HTTPS) so that push/pull works without entering a password:

```bash
git clone git@github.com:Josh-Almonte/kittens_index.git
cd kittens_index
```

---

## ✏️ Step 2 — Make a Change

Open `kittens.md` and add your own kitten entry following the existing format.

---

## 💾 Step 3 — Commit Your Change

```bash
# See what changed
git status

# Stage your file(s)
git add kittens.md

# Commit with a meaningful message
git commit -m "Add my kitten to the index"
```

---

## 🚀 Step 4 — Push to GitHub

```bash
git push origin main
```

---

## 🔄 Step 5 — Pull the Latest Changes

Before starting work each session, always pull to get updates from the remote:

```bash
git pull origin main
```

---

## 📁 Repository Structure

```
kittens_index/
├── README.md        ← You are here
├── kittens.md       ← The kitten index (edit this!)
├── CONTRIBUTING.md  ← Detailed contribution workflow
└── .gitignore       ← Files Git should ignore
```

---

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for a step-by-step guide to the full fork → clone → edit → push → pull-request workflow.

---

## 📜 License

[MIT](LICENSE)