## 🚀14/03/2025 - Building My Own GitLab & GitHub Workflows: A Journey in Source Control
## 🚀14/03/2025 - Building My Own GitLab & GitHub Workflows: A Journey in Source Control

## **Introduction**

Today was one of those days where **everything clicks into place**.  
After years of working with code, scripts, and configs in networking and System Engineering — sometimes organized, sometimes messy — I decided to **get serious** about **source control, automation, and managing my own projects and dotfiles**.

And let me tell you — **setting up my own self-hosted GitLab**, has been **a game-changer**. Here’s a breakdown of what I did, what I learned, and what’s next.

---

## **Why I Did This**

- I wanted **better control over my own work**, without always relying on third-party hosted repos.
- I needed a way to **work across multiple devices** (my laptop, Linux rig, home servers) without getting lost in different versions.
- I was tired of "where did I put that config again?" — **version control for my entire lab and scripts** is now a must-have.
- Plus, I wanted to finally **understand Git and branches properly**, and **protect** important work.

---

## **Part 1: Spinning up a Self-Hosted GitLab**

First up, I decided to **host my own GitLab instance in Docker** on my `mon1` box. This means:
- Full control over **repos, branches, access control**.
- Ability to **self-host private work** (my scripts, Docker files, configs).
- Separating **personal/internal projects** from public-facing content on GitHub.

### **Key lessons:**

- Using Docker Compose makes deploying GitLab **manageable and reproducible**.
- **Mounting proper volumes** for GitLab data, configs, and logs means it’s safe and portable.
- Adding **SSH keys** for secure access and enabling **protected branches** adds a layer of professionalism to my lab.
- Getting familiar with **GitLab's UI** — setting **default branches**, **protected branches**, and **merge request workflows**.

---

## **Part 2: Understanding Branching (Properly, Finally)**

This was the real "aha" moment for me.

I used to just "commit to master" and hope for the best. Today, I learned how to **manage proper dev branches**:

- **Device-specific dev branches**:  
  - `dev-laptop`  
  - `dev-linux-rig`  

- **Protected "main" branches** that hold my **ready/working versions**.

### **Flow**:

- Make and test changes in a `dev-*` branch.
- When ready, create a **merge request to main** — for internal review and approval (even if it's just me for now!).

> 🌟 **Realizations**:
> - **Main is sacred** — only polished work gets merged.
> - Dev branches allow **freedom to experiment**.
> - **Merge requests simulate real team workflows** — future-proof if I collaborate later.

---

## **Part 3: Linking GitHub and GitLab (Public vs Private)**

Another big takeaway:  
- **GitHub** is my public face — for blogs, open-source, and polished work.
- **GitLab** is my private dev lab — for experiments, scripts, sensitive files (think: Docker Compose files, .bashrc, SSH config).

➡️ So I set up:
- **Private GitLab repo with branches (main/dev)**
- **GitHub as public-facing repo for finalized blog posts and docs**

### **Final workflow:**

1. Work in `dev-linux-rig` or `dev-laptop`.
2. Merge into `main` on GitLab when stable.
3. (Optional) Pull selected files and **push to GitHub** for public viewing.

---

## **Part 4: Managing Dotfiles and Automation Ideas**

- I set up **dotfiles repo** in GitLab for things like `.bashrc`, `.vimrc`, `.ssh/config`.
- Learned about the idea of **bare repos for dotfiles**, but keeping it simple for now.
- Thinking ahead:  
  - Use **cron jobs to auto-pull from Git** (keeping servers updated).
  - Explore **Ansible** for proper config management and deployment.

---

## **Wins from Today**

- ✅ **Self-hosted GitLab** — up, running, secure, accessible.
- ✅ **SSH keys and remotes managed**.
- ✅ **Proper branch strategy** — no more committing everything to master.
- ✅ **Protected branches and merge requests** in place.
- ✅ Started **thinking about automation** and **future scaling**.
- ✅ Realized I now have a **solid backup/versioning system for scripts and dotfiles**.
- ✅ **New blog workflow** (GitHub as polished, GitLab as dev space).

---

## **Reflections**

Looking back, I realized:

- I **used to be reactive** — scripts here, files there, always searching for "the latest version".
- Now, I'm **proactive and structured** — I know where things are, and I know how to collaborate (even if it's just me).
- **Git is powerful when you respect it** — understanding branches, remotes, and workflows opens up **so much control**.
- Setting up **my own GitLab** makes me independent of third-party services and lets me experiment.

---

## **What's Next?**

- [ ] Add **automation** (cron or Ansible).
- [ ] Refine **GitHub blog** workflow (maybe mirror a dev branch?).
- [ ] Continue adding **dotfiles and scripts** — versioning *everything*.
- [ ] Explore **CI/CD pipelines** for future lab projects.
- [ ] Keep practicing **merge requests and protected branches**.

---

## **Final Thoughts**

If you're reading this and still managing your scripts and configs manually — **take the leap**.  
Set up a GitLab, learn proper branching, and **own your work**.

---

## **Bonus**: My New Git Habits

- **Branch for everything** — dev first, merge to main when ready.
- **Protect main** — no direct commits.
- **Use merge requests** — even for myself (practice for future teams).
- **SSH keys for all access** — secure and smooth.
- **Back everything up** — dotfiles, scripts, and Docker stuff included.

---

**Thanks for reading. Let's build cool things.** 🚀
