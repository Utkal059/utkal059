<div align="center">

<!-- ────────────────────────────────────────────────────────────────── -->
<!--                                                                    -->
<!--   utkal singh — kernel ⋅ systems ⋅ open source                     -->
<!--                                                                    -->
<!-- ────────────────────────────────────────────────────────────────── -->

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,45:0d2818,100:00ff88&height=180&section=header&text=Utkal%20Singh&fontSize=64&fontColor=ffffff&fontAlignY=42&desc=Linux%20kernel%20mainline%20contributor%20%E2%80%A2%20systems%20%E2%80%A2%20full-stack%20%E2%80%A2%20open%20source&descAlignY=66&descSize=14&animation=fadeIn" width="100%"/>

<br/>

<a href="https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/?qt=author&q=Utkal+Singh">
  <img src="https://img.shields.io/badge/Linux_Kernel-Mainline_(v7.1--rc1)-00ff88?style=for-the-badge&logo=linux&logoColor=black&labelColor=0d1117" alt="Linux Mainline"/>
</a>
<a href="https://gssoc.girlscript.org/profile/5234b52c-312e-47c6-9e95-f2194f95f76a">
  <img src="https://img.shields.io/badge/GSSoC_2026-Accepted-ff6ec7?style=for-the-badge&logo=opensourceinitiative&logoColor=white&labelColor=0d1117" alt="GSSoC 2026 Accepted"/>
</a>
<a href="https://lore.kernel.org/linux-erofs/?q=Utkal+Singh">
  <img src="https://img.shields.io/badge/erofs--utils-Merged_patches-fcc624?style=for-the-badge&logo=gnu&logoColor=black&labelColor=0d1117" alt="erofs-utils"/>
</a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=3500&pause=900&color=00FF88&center=true&vCenter=true&width=720&lines=Patch+merged+into+Linus+Torvalds'+tree+%E2%9C%93;Filesystems+%C2%B7+kernel+internals+%C2%B7+low-latency+systems;C+%E2%86%92+C%2B%2B+%E2%86%92+Python+%E2%86%92+TypeScript+%E2%86%92+back+to+C;Reading+source+is+more+fun+than+writing+it" alt="typing"/>

</div>

---

## ► whoami

```c
/* /proc/self/status */
struct contributor utkal = {
    .name        = "Utkal Singh",
    .handle      = "Utkal059",
    .institute   = "Thapar Institute of Engineering & Technology",
    .program     = "B.Tech CSE  (expected 2027)",
    .based_in    = "India",
    .focus       = { "linux filesystems", "low-latency systems",
                     "quant infrastructure", "open source" },
    .signed_off  = true,        /* in mainline since v7.1-rc1 */
};
```

I work on **filesystems, kernel infrastructure, and the systems that sit underneath performance-critical software.** My day-to-day is split between sending patches to the [linux-erofs](https://lore.kernel.org/linux-erofs/) mailing list, reading source trees, and building the trading-infrastructure projects that taught me to care about microseconds in the first place.

---

## ★ Flagship — Linux mainline ( v7.1-rc1 )

> *A patch I authored shipped in the upstream Linux kernel, pulled by maintainer Gao Xiang into Linus Torvalds' tree.*

```diff
  Subject: [GIT PULL] erofs updates for 7.1-rc1
  From:    Gao Xiang <xiang@kernel.org>
  To:      Linus Torvalds <torvalds@linux-foundation.org>
  Date:    Mon, 13 Apr 2026 12:47:49 +0800

  ----------------------------------------------------------------
  Changes since last update:

   - Validate xattr h_shared_count to report -EFSCORRUPTED explicitly
     for crafted images
   - ... (other changes)

  ----------------------------------------------------------------
+ Utkal Singh (1):
+       erofs: harden h_shared_count in erofs_init_inode_xattrs()

   fs/erofs/xattr.c | 8 ++++++++
   1 file changed, 8 insertions(+)
```

**What it does** — On crafted/corrupted EROFS images, the original code could read past the end of the inline xattr buffer when `h_shared_count` was implausibly large. The patch validates the field against `xattr_isize` *before* the shared-entry loop and reports `-EFSCORRUPTED` cleanly instead of marching off the end of memory. It's a small diff with a big surface: every Android device that ships an EROFS root partition runs this code path.

📜 **Pull request thread:** [`adx1dXEp8xyWwgZ2@debian`](https://lore.kernel.org/linux-erofs/adx1dXEp8xyWwgZ2@debian/) ・ ack'd by [`pr-tracker-bot`](https://lore.kernel.org/linux-erofs/) on 2026-04-14

---

## ⚡ Selected merged contributions

A short list, picked for impact rather than count. Full mailing-list history: [lore.kernel.org/linux-erofs](https://lore.kernel.org/linux-erofs/?q=Utkal+Singh).

<table>
<tr>
  <th align="left" width="36%">Project</th>
  <th align="left" width="44%">Contribution</th>
  <th align="center" width="20%">Status</th>
</tr>

<tr>
  <td>
    <a href="https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/"><b>Linux kernel</b></a><br/>
    <sub><code>fs/erofs/xattr.c</code></sub>
  </td>
  <td>
    <code>erofs: harden h_shared_count in erofs_init_inode_xattrs()</code><br/>
    <sub>Pulled by maintainer to <code>tags/erofs-for-7.1-rc1</code> → Linus' tree.</sub>
  </td>
  <td align="center"><b>🟢 mainline</b></td>
</tr>

<tr>
  <td>
    <a href="https://git.kernel.org/pub/scm/linux/kernel/git/xiang/erofs-utils.git/"><b>erofs-utils</b></a><br/>
    <sub>userspace tooling for EROFS</sub>
  </td>
  <td>
    7+ merged patches across <code>lib/</code>, <code>fsck/</code>, and <code>dump/</code> — UB fix in <code>kite_deflate</code>, NULL checks after <code>strdup()</code>, ZSTD <code>-EIO</code> propagation, pthread resource leak, deflate buffer cap, recursion-depth limit, fsck xattr verification.
  </td>
  <td align="center"><b>🟢 merged</b></td>
</tr>

<tr>
  <td>
    <a href="https://github.com/checkpoint-restore/criu"><b>CRIU</b></a><br/>
    <sub>Checkpoint/Restore in Userspace</sub>
  </td>
  <td>
    <a href="https://github.com/checkpoint-restore/criu/pull/2982"><code>PR #2982</code></a> — fix nanosecond overflow when restoring POSIX timers; would silently corrupt timer state on long-running processes.
  </td>
  <td align="center"><b>🟢 merged</b></td>
</tr>

<tr>
  <td>
    <a href="https://github.com/mogan-org/mogan"><b>MoganLab / mogan</b></a><br/>
    <sub>scientific document editor</sub>
  </td>
  <td>
    <a href="https://github.com/mogan-org/mogan/pull/2914"><code>PR #2914</code></a> — suppress ghost borders in vertically-spanned table cells (typesetter fix). <a href="https://github.com/mogan-org/mogan/pull/2915"><code>PR #2915</code></a> — tab-close rendering glitch.
  </td>
  <td align="center"><b>🟢 merged</b></td>
</tr>

<tr>
  <td>
    <a href="https://gssoc.girlscript.org/"><b>GSSoC '26 — Atelier</b></a><br/>
    <sub>open-source contribution platform</sub>
  </td>
  <td>
    <code>ContributorProfileCard</code> — TypeScript / React / Tailwind component with XP system, badge styling, and level progression. Selected as <b>Contributor / Mentee</b> on the Open Source track.
  </td>
  <td align="center"><b>🟢 accepted</b></td>
</tr>

</table>

---

## 🌸 GSSoC 2026 — selected

> Accepted into **GirlScript Summer of Code 2026** as a *Contributor / Mentee* on the **Open Source Track** (May 2026).
>
> Public profile: [gssoc.girlscript.org/profile/5234b52c-…](https://gssoc.girlscript.org/profile/5234b52c-312e-47c6-9e95-f2194f95f76a)

```
┌───────────────────────────── GSSoC 2026 ─────────────────────────────┐
│  Role         Contributor / Mentee                                   │
│  Track        Open Source                                            │
│  Status       Accepted                                               │
│  Project      Open-Source-Contribution-Atelier                       │
│  Stack        TypeScript · React · Tailwind CSS                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## 🛠 Currently building

**[OrderFlow Backtester](https://github.com/Utkal059)** &nbsp;·&nbsp; *trading-infra portfolio piece*

A single repo spanning four languages and a real C++ ↔ Python boundary. Built to look and behave like the desks I want to work for.

| layer | what's there |
|---|---|
| **Core** | C++ limit order book ・ price-time-priority matching ・ tick-by-tick replay |
| **Bindings** | `pybind11` zero-copy, 18/18 unit tests passing |
| **Models** | GARCH(1,1) volatility · Almgren-Chriss slippage · XGBoost + SHAP |
| **API** | FastAPI + WebSocket streaming |
| **Frontend** | React / Vite / Tailwind — Bloomberg-terminal aesthetic |

**[Multi-threaded `fsck.erofs`](https://lore.kernel.org/linux-erofs/?q=multi-threaded+fsck)** — Sent the [RFC](https://lore.kernel.org/linux-erofs/) to the list and merged the prerequisite `--workers` flag and pthread-leak fixes upstream. Parallel inode verification design is live in the public archive.

---

## 🧰 Stack — what I actually use

```
systems          C       C++14/17    pthreads    Linux        Bash
                 git send-email      lore.kernel.org workflow

backend          Python  FastAPI     pybind11    asyncio
                 NumPy / Pandas      XGBoost     SHAP

frontend         TypeScript  React (Vite)  Tailwind CSS

tooling          WSL2 Ubuntu · VS Code · Docker · gdb · perf

learning next    Rust  ·  Go  ·  io_uring  ·  eBPF
```

---

## 📈 GitHub

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Utkal059&show_icons=true&theme=merko&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=c9d1d9&include_all_commits=true&rank_icon=github" height="170"/>
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Utkal059&layout=compact&theme=merko&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=c9d1d9&langs_count=8" height="170"/>

<img src="https://streak-stats.demolab.com?user=Utkal059&theme=dark&hide_border=true&background=0d1117&stroke=00ff88&ring=00ff88&fire=00b4d8&currStreakLabel=00ff88&sideLabels=c9d1d9&dates=8b949e" alt="streak"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Utkal059&bg_color=0d1117&color=00ff88&line=00ff88&point=ffffff&area=true&hide_border=true" width="100%" alt="contribution graph"/>

</div>

---

## ✉ Contact

```
$ whois utkal
  email      singhutkal015@gmail.com
  github     github.com/Utkal059
  linkedin   linkedin.com/in/utkal-singh03
  kernel     lore.kernel.org/linux-erofs/?q=Utkal+Singh
  gssoc      gssoc.girlscript.org/profile/5234b52c-312e-47c6-9e95-f2194f95f76a
```

<a href="mailto:singhutkal015@gmail.com"><img src="https://img.shields.io/badge/-singhutkal015%40gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white&labelColor=0d1117"/></a>
<a href="https://github.com/Utkal059"><img src="https://img.shields.io/badge/-@Utkal059-181717?style=flat-square&logo=github&logoColor=white&labelColor=0d1117"/></a>
<a href="https://www.linkedin.com/in/utkal-singh03/"><img src="https://img.shields.io/badge/-utkal--singh03-0a66c2?style=flat-square&logo=linkedin&logoColor=white&labelColor=0d1117"/></a>
<a href="https://lore.kernel.org/linux-erofs/?q=Utkal+Singh"><img src="https://img.shields.io/badge/-linux--erofs-fcc624?style=flat-square&logo=linux&logoColor=black&labelColor=0d1117"/></a>

---

<div align="center">

<sub>

`Signed-off-by: Utkal Singh <singhutkal015@gmail.com>`

</sub>

<sub><i>“Read the source. Fix the bug. Send the patch.”</i></sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ff88,55:0d2818,100:0d1117&height=80&section=footer" width="100%"/>

</div>
