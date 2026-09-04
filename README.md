<div align="center">

<img src="https://camo.githubusercontent.com/db6e1ee851dadb9be2f58b3c2583ac7b70711a1003abd8ad70cdcccf03dfacbf/68747470733a2f2f726561646d652d747970696e672d7376672e6865726f6b756170702e636f6d3f666f6e743d466972612b436f64652673697a653d3234266475726174696f6e3d333030302670617573653d3130303026636f6c6f723d3336424346372663656e7465723d74727565267643656e7465723d747275652677696474683d363030266c696e65733d57656c636f6d652b746f2b6d792b4769744875622b50726f66696c65213b4353452b53747564656e742b2537432b4453412b456e74687573696173743b4c6561726e696e672b436c6f75642b436f6d707574696e672b2532362b446576656c6f706d656e743b4275696c64696e672532432b4c6561726e696e672b616e642b47726f77696e672b45766572792b4461792b254630253946253941253830" alt="Typing SVG" />

</div>

<h1 align="center">Hi 👋, I'm Sumit Shukla</h1>
<h3 align="center">🚀 B.Tech CSE Student | 💻 Aspiring Software Developer | ☁️ Cloud Computing Enthusiast</h3>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Sumit261codes&label=Profile%20Views&color=0e75b6&style=flat" alt="profile views" />
</p>

<div align="center">

```bash
~/ whoami
```

Hi, I'm Sumit Shukla. I build things that sit somewhere between DSA, backend dev,
and cloud computing, and I solve problems for fun.

</div>

<p align="center">
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN-HANDLE" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:YOUR-EMAIL@example.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://your-portfolio-site.example.com" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  <a href="https://leetcode.com/YOUR-LEETCODE-HANDLE" target="_blank">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" />
  </a>
  <a href="https://codeforces.com/profile/YOUR-CODEFORCES-HANDLE" target="_blank">
    <img src="https://img.shields.io/badge/Codeforces-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" />
  </a>
</p>

---

### 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,java,python,mysql,html,css,js,aws,git,github,vscode,linux" />
</p>

---

### 📊 3D Contribution Graph

<p align="center">
  <img src="https://raw.githubusercontent.com/Sumit261codes/Sumit261codes/output/profile-3d-contrib/profile-night-rainbow.svg" alt="3D contribution graph" />
</p>

---

<p align="center">⭐ Feel free to explore my repositories and follow my coding journey!</p>
<p align="center"><i>Learning. Building. Improving. Repeating.</i></p>
name: 3D Profile Contribution Graph

on:
  schedule:
    - cron: "0 0 * * *" # runs once a day
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: actions/checkout@v4
      - uses: yoshi389111/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: Sumit261codes
      - name: Commit and push
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add -A .
          git commit -m "generate 3d contribution graph" || echo "no changes"
          git push origin output
