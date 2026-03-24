<div align="center">

<!-- Animated header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,40:003d20,100:00ff88&height=220&section=header&text=Hey%20%F0%9F%91%8B%20I'm%20Utkal&fontSize=55&fontColor=ffffff&fontAlignY=38&desc=Linux%20Kernel%20Contributor%20%E2%80%A2%20AI%2FML%20Enthusiast%20%E2%80%A2%20Open%20Source%20%40%20GSoC%202026&descAlignY=58&descSize=15&animation=fadeIn" width="100%"/>

<!-- Typing SVG -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&repeat=true&width=650&lines=Building+AI+tools+that+make+sense+%F0%9F%A4%96;Sending+patches+to+linux-erofs+%F0%9F%90%A7;Exploring+deep+learning+architectures+%F0%9F%A7%A0;GSoC+2026+applicant+%E2%9A%A1;open+source+%3E+everything+else+%F0%9F%8C%90" alt="Typing SVG" />

<br/><br/>

<!-- Badges -->
![Linux Kernel](https://img.shields.io/badge/Linux_Kernel-Contributor-00ff88?style=flat-square&logo=linux&logoColor=white&labelColor=0d1117)
![GSoC](https://img.shields.io/badge/GSoC-2026_Applicant-4285f4?style=flat-square&logo=google&logoColor=white&labelColor=0d1117)
![AI/ML](https://img.shields.io/badge/AI%2FML-Enthusiast-bc8cff?style=flat-square&logo=pytorch&logoColor=white&labelColor=0d1117)
![Open Source](https://img.shields.io/badge/Open_Source-%E2%9D%A4%EF%B8%8F-ff6b6b?style=flat-square&labelColor=0d1117)

<br/>

[![Profile Views](https://komarev.com/ghpvc/?username=Utkal059&label=Profile+Views&color=00ff88&style=flat-square)](https://github.com/Utkal059)
[![GitHub followers](https://img.shields.io/github/followers/Utkal059?label=Followers&style=flat-square&color=00b4d8&labelColor=0d1117)](https://github.com/Utkal059)

</div>

---

## 🧑‍💻 About Me

```python
class Utkal:
    name       = "Utkal Singh"
    handle     = "@Utkal059"
    role       = ["Linux Kernel Contributor", "CS Student", "AI/ML Enthusiast"]
    gsoc       = "2026 Applicant → erofs / Linux kernel"

    passions   = ["artificial intelligence", "open source", "filesystems", "quantum computing"]
    currently  = ["deep learning architectures", "kernel internals", "CUDA programming"]

    tools      = ["C", "Python", "PyTorch", "Git", "Linux", "Bash", "Docker"]
    env        = "WSL Ubuntu + VS Code"

    fun_fact   = "Sent 70+ patches to linux-erofs in ~2 weeks 🐧"
    ask_me     = "filesystems · AI/ML · quantum computing · open source strategy"
```

---

## 🤖 AI/ML Interests

| Area | What I'm Exploring |
|------|-------------------|
| 🧠 **Deep Learning** | CNNs, Transformers, attention mechanisms |
| 🔬 **Research + OSS AI** | Reproducible ML, contributing to open AI tooling |
| ⚡ **Systems for ML** | Bridging low-level C systems knowledge with ML infra |
| 🌌 **Quantum Computing** | Multi-qubit gates, Bell states, quantum algorithms |

---

## 🛠️ Tech Stack

<div align="center">

**AI / ML**

[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)

**Systems & Kernel**

[![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://www.linux.org)
[![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com)
[![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/)

**Languages & Tools**

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)
[![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)](https://isocpp.org)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com)
[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com)

</div>

---

## 🔧 Open Source Contributions

### 🐧 Linux Kernel / erofs-utils
> Patches submitted via `git send-email` to **linux-erofs@lists.ozlabs.org**

| Patch | Location | Status |
|-------|----------|--------|
| `h_shared_count` validation | `fs/erofs/xattr.c` | ✅ Reviewed-by Gao Xiang |
| ZSTD decompression bug series | `fs/erofs/zdata.c` | 📬 Sent to mailing list |
| Deflate buffer overflow fix (64 MiB cap) | `lib/decompress.c` | ✅ Merged |
| NULL check after `strdup()` | `lib/tar.c` | ✅ Merged |
| Error code propagation fix | `lib/io.c` | ✅ First upstream patch |
| fsck xattr verification fix | `fsck/main.c` | ✅ Merged |
| Directory recursion depth limit | `lib/dir.c` | ✅ Merged |

### 🔬 MoganLab/mogan (Scientific Editor)
- **PR #2914** — `fix(typeset)`: suppress ghost borders in vertically-spanned table cells
- **PR #2915** — fix tab rendering in document editor

---

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Utkal059&show_icons=true&theme=merko&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=c9d1d9&rank_icon=github&include_all_commits=true" height="170"/>
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Utkal059&layout=compact&theme=merko&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=c9d1d9&langs_count=6" height="170"/>

<br/>

<img src="https://streak-stats.demolab.com?user=Utkal059&theme=dark&hide_border=true&background=0d1117&stroke=00ff88&ring=00ff88&fire=00b4d8&currStreakLabel=00ff88&sideLabels=c9d1d9&dates=8b949e" alt="GitHub Streak"/>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Utkal059&bg_color=0d1117&color=00ff88&line=00ff88&point=ffffff&area=true&hide_border=true" width="100%" alt="Contribution Graph"/>

</div>

---

## 🐍 Contribution Snake

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Utkal059/Utkal059/output/github-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Utkal059/Utkal059/output/github-snake.svg"/>
    <img alt="GitHub Contribution Snake" src="https://raw.githubusercontent.com/Utkal059/Utkal059/output/github-snake-dark.svg"/>
  </picture>
</div>

---

## 🏆 GitHub Trophies

<div align="center">
<img src="https://github-profile-trophy.vercel.app/?username=Utkal059&theme=darkhub&no-frame=true&no-bg=true&margin-w=6&column=6" alt="GitHub Trophies"/>
</div>

---

## 💬 Random Dev Quote

<div align="center">
<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark" alt="Dev Quote"/>
</div>

---

## 📬 Connect With Me

<div align="center">

[![Email](https://img.shields.io/badge/Email-singhutkal015%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:singhutkal015@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Utkal059-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Utkal059)
[![Kernel Mailing List](https://img.shields.io/badge/linux--erofs-mailing%20list-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://lore.kernel.org/linux-erofs/)

</div>

---

<div align="center">

*"First, solve the problem. Then, write the code."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ff88,60:003d20,100:0d1117&height=100&section=footer" width="100%"/>

</div>
