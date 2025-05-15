## 👋 Hi, I'm Eshan Shah K

🎓 BCA Student | 💻 C & Web Dev Enthusiast | 🚀 Future ML Specialist & Entrepreneur  
📍 Kerala, India
name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
---

## 🔧 Tech Stack

- 🌐 Web: HTML, CSS, JavaScript (Learning)
- 💻 Programming: C (Strong), Learning JavaScript & Python
- ⚙️ Tools: VS Code, Git & GitHub
- 📱 Working on: Lecturer Evaluation Form Website

---

## 📚 Learning Journey

- 📘 Mastering C Programming & Advanced Concepts
- 🧠 Diving into Machine Learning (2025 Goal)
- 🛠️ Building my first remote-controlled Arduino car
- 📈 Learning Business & Entrepreneurship fundamentals

---

## 📌 Current Goals

- Become confident in **JS** & **Python**
- Build full-stack web apps using **JavaScript**
- Contribute to open-source & personal projects
- Prepare for **ML internships** by end of 2025

---

## 🧠 Fun Fact

> "I don't wait for opportunities — I build them."

---

## 📫 Let's Connect

- 💼 LinkedIn: 
- 📷 Instagram: [@eshan.shaah](https://instagram.com/eshan.shaah)
- 📬 Email: eshanshahk123@email.com

---

![Eshan's GitHub Stats](https://github-readme-stats.vercel.app/api?username=eshanshahk&show_icons=true&theme=radical)
