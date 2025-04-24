<div align="center">
  <!-- Animasi teks ketik -->
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=4000&pause=1000&color=58F768&center=true&width=500&lines=Hi+%F0%9F%91%8B%2C+I'm+Cyberstarszs;Full-Stack+Developer;Open+Source+Contributor" alt="Header Typing Animation" />
  
  <!-- GIF Header (Opsional) -->
  <img src="assets/images/header.gif" width="700" alt="Tech Header">
</div>

---

## 🧑💻 **About Me**
```javascript
const cyberstarszs = {
  code: ["JavaScript", "Python", "TypeScript"],
  tools: ["React", "Node.js", "Docker", "AWS"],
  architecture: ["microservices", "serverless", "AI/ML pipelines"],
  challenge: "Membuat 1000 commit dalam 1 tahun!",
  funFact: "Pernah deploy aplikasi saat gempa 5.9 SR 🌍"
};

---

### ⚙️ **.github/workflows/daily-commit.yml**
```yaml
name: Daily Auto-Commit
on:
  schedule:
    - cron: '0 12 * * *' # Setiap hari jam 12 siang UTC
  workflow_dispatch:

jobs:
  commit:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3
        with:
          persist-credentials: false

      - name: Update Daily File
        run: |
          echo "# Daily Commit - $(date)" >> daily-commit.md
          git config --global user.name "Cyberstarszs"
          git config --global user.email "github-actions@cyberstarszs.com"

      - name: Commit Changes
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          commit_message: '📅 Daily Commit: Keep the streak alive!'
          branch: main
