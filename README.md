<!-- ░░ SILENT PRELOAD ░░ -->
<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,100:0d1117&height=4&section=header" />
</div>

<div align="center">

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=700&size=13&pause=1200&color=00FF88&center=true&vCenter=true&width=720&lines=%E2%96%BA+initializing+rishabh_tripathi_agent...;%E2%96%BA+loading+identity+module...+%5BOK%5D;%E2%96%BA+mounting+experience+context...+%5BOK%5D;%E2%96%BA+spinning+up+tool+executor...+%5BOK%5D;%E2%96%BA+agent+ready.+awaiting+query." alt="init" /></a>

</div>

---

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║   🤖  AGENT RUN  ──  rishabh_tripathi_agent  ──  session/2026.05            ║
║   ─────────────────────────────────────────────────────────────────────     ║
║   status        ●  ACTIVE  →  OneClarity.ai  ·  Pune, India 🇮🇳             ║
║   objective     resolve: "who built this profile and what can they do?"     ║
║   model         rishabh-v2026  |  context: 20 yrs  |  temp: 0.95 🔥         ║
║   tools         [get_identity, get_experience, list_projects,               ║
║                  get_capabilities, fetch_achievements, render_metrics]      ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

<br/>

<!-- ════════════════ STEP 1 ════════════════ -->

```python
# ── [STEP 1 / 6]  ·  identity ────────────────────────────────────────────────
thought = "Start with core identity. Load the profile module."
action  = agent.tool_call("get_identity")
```

```json
{
  "✅  tool"       : "get_identity",
  "name"          : "Rishabh Tripathi",
  "alias"         : "rish-23072005",
  "role"          : ["AI Engineer", "Multi-Agent Systems", "Full-Stack Dev"],
  "education"     : "B.Tech CS · Specialisation AI & ML  ·  GLA University  ·  2026",
  "research"      : "IEEE Published — RL / DQN · Autonomous Fleet Management System",
  "currently_at"  : "OneClarity.ai  ·  AIML Engineer  ·  Pune",
  "exp_months"    : "18+  production AI engineering  ·  4 companies",
  "philosophy"    : "Build things that matter. Ship things that scale. 🚀"
}
```

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/rishabh-tripathi-403420210)
[![Medium](https://img.shields.io/badge/Medium-000000?style=flat-square&logo=medium&logoColor=white)](https://medium.com/@Rishabhtripathi)
[![X / Twitter](https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/@RISHABH05329095)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://youtube.com/@rishabhtripathi5124)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/tpsJ2Guq)
[![Email](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:rishabhtripathi.9984@gmail.com)
[![Profile Views](https://komarev.com/ghpvc/?username=rish-23072005&label=profile+reads&color=00ff88&style=flat-square)](https://github.com/rish-23072005)

</div>

<br/>

<!-- ════════════════ STEP 2 ════════════════ -->

```python
# ── [STEP 2 / 6]  ·  experience ──────────────────────────────────────────────
thought = "Four companies. 18+ months of production AI. Load the full log."
action  = agent.tool_call("get_experience", filter="production_only")
```

```json
{
  "✅  tool" : "get_experience",
  "entries" : [
    {
      "company"  : "OneClarity.ai",
      "role"     : "AIML Engineer",
      "location" : "Pune",
      "period"   : "Dec 2025 – Present  🟢",
      "shipped"  : [
        "Adaptive learning platform — multi-agent architecture (LangGraph context-graph)",
        "Sub-agents: content_delivery · assessment · sequencing — fully orchestrated",
        "Shared context-caching layer — cut redundant LLM API calls across modules",
        "Docker · AWS EC2/S3 · GitHub Actions CI/CD — zero-downtime rolling deploy"
      ]
    },
    {
      "company"  : "Aiventory",
      "role"     : "AI Project Lead",
      "location" : "Kolkata",
      "period"   : "Sep 2025 – Nov 2025",
      "shipped"  : [
        "AI-powered inventory mgmt system — Django · PostgreSQL · Docker",
        "LSTM time-series demand forecasting per SKU",
        "K-means segmentation + collaborative filtering recommendation engine"
      ]
    },
    {
      "company"  : "Liquid Minds",
      "role"     : "Machine Learning Engineer",
      "location" : "Bangalore",
      "period"   : "May 2025 – Aug 2025",
      "shipped"  : [
        "Production automation agents — n8n · LangChain · Zapier",
        "HR candidate screening pipeline agent — eliminated manual decisioning",
        "Marketing campaign + lead-gen workflow agent"
      ]
    },
    {
      "company"  : "Kode Vortex  (KV Tech)",
      "role"     : "AI & Full-Stack Intern",
      "location" : "Pune",
      "period"   : "Aug 2024 – Apr 2025",
      "shipped"  : [
        "MERN + Three.js — 3D UI components and WebGL visualisations",
        "AI exam proctoring portal — real-time body monitoring · SSL · live dashboard"
      ]
    }
  ]
}
```

<br/>

<!-- ════════════════ STEP 3 ════════════════ -->

```python
# ── [STEP 3 / 6]  ·  projects ────────────────────────────────────────────────
thought = "Four flagship builds. One IEEE paper. Surface the notable ones."
action  = agent.tool_call("list_projects", sort_by="impact", limit=4)
```

```json
{
  "✅  tool"    : "list_projects",
  "projects"  : [
    {
      "name"     : "🤖  HackEval — AI Hackathon Evaluation Agent",
      "period"   : "Aug – Sep 2025",
      "problem"  : "Hackathon judging is slow, inconsistent, and biased",
      "solution" : "End-to-end AI judge: PPT analysis + GitHub plagiarism detection + auto-leaderboard",
      "stack"    : ["LangChain", "AI Agents", "React", "AWS", "REST API"]
    },
    {
      "name"     : "🎙️  SmaranAI — Voice Calendar Assistant",
      "period"   : "May – Jun 2025",
      "problem"  : "Scheduling requires opening apps and typing",
      "solution" : "Speak naturally → Whisper STT → LangChain intent → CrewAI exec → Calendar synced",
      "stack"    : ["OpenAI Whisper", "LangChain", "CrewAI", "Google Calendar API", "TTS"]
    },
    {
      "name"     : "🚗  AutoFleet / Zyara — Autonomous Fleet Management  📄 IEEE",
      "period"   : "Feb – Mar 2025",
      "problem"  : "Fleet routing is computationally expensive and static",
      "solution" : "DQN-based RL agent for real-time route optimisation + dynamic task allocation",
      "stack"    : ["Reinforcement Learning", "DQN", "Python", "Simulation Engine"],
      "published": "IEEE Conference — GLA University · 2025"
    },
    {
      "name"     : "🧠  Adaptive Learning Platform  (prod @ OneClarity.ai)",
      "period"   : "Dec 2025 – Present",
      "problem"  : "One-size-fits-all e-learning doesn't adapt to the learner",
      "solution" : "LangGraph multi-agent system: discrete agents per learning function, shared context graph",
      "stack"    : ["LangGraph", "LangChain", "Docker", "AWS EC2/S3", "GitHub Actions"]
    }
  ]
}
```

<br/>

<!-- ════════════════ STEP 4 ════════════════ -->

```python
# ── [STEP 4 / 6]  ·  capabilities ────────────────────────────────────────────
thought = "Build the full capability map. Group by domain, rank by depth."
action  = agent.tool_call("get_capabilities", format="matrix")
```

```
╔══════════════════════════════════════════════════════════════════════════════╗
║  CAPABILITY MATRIX  ·  rishabh_tripathi_agent                               ║
╠════════════════════════════╦═══════════════════════════════════════════════╣
║  DOMAIN                    ║  TOOLS  &  FRAMEWORKS                         ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  🤖  Agentic  AI  [████ █]  ║  LangChain · LangGraph · CrewAI · n8n        ║
║                            ║  OpenAI · Whisper STT · HuggingFace · RAG     ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  🧠  ML  /  DL    [████ █]  ║  PyTorch · TensorFlow · Keras · scikit-learn ║
║                            ║  MLflow · LSTM · DQN · K-means · Pandas/NumPy ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  🌐  Full-Stack   [████░░]  ║  React · Next.js · Three.js · WebGL           ║
║                            ║  Node.js · Django · FastAPI · Flask · MERN    ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  ☁️  Cloud/DevOps  [███░░░]  ║  AWS (EC2 · S3) · Docker · GitHub Actions    ║
║                            ║  GCP · Vercel · Nginx · CI/CD pipelines        ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  🗄️  Data  /  DB   [███░░░]  ║  PostgreSQL · MongoDB · MySQL · Power BI      ║
║                            ║  Plotly · Matplotlib · SciPy                  ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  ⚡  Languages    [████░░]  ║  Python · JavaScript · Go (learning)          ║
║                            ║  HTML/CSS · Bash · SQL                        ║
╠════════════════════════════╬═══════════════════════════════════════════════╣
║  🔗  Web3         [██░░░░]  ║  Web3.js  ·  Blockchain integrations          ║
╚════════════════════════════╩═══════════════════════════════════════════════╝
```

<br/>

<!-- ════════════════ STEP 5 ════════════════ -->

```python
# ── [STEP 5 / 6]  ·  achievements ────────────────────────────────────────────
thought = "Surface the credentials. IEEE, IBM, 4 companies, hackathons."
action  = agent.tool_call("fetch_achievements")
```

```json
{
  "✅  tool"         : "fetch_achievements",
  "achievements"   : [
    {
      "type"        : "📄  Research",
      "title"       : "IEEE Published — RL-based Autonomous Fleet Management",
      "detail"      : "DQN route optimisation · GLA University · 2025",
      "status"      : "VERIFIED"
    },
    {
      "type"        : "🎓  Certification",
      "title"       : "IBM — Python for Data Science, AI & Development",
      "issuer"      : "IBM Cognitive Class  ·  Verified on Credly",
      "status"      : "VERIFIED"
    },
    {
      "type"        : "🏆  Competitions",
      "title"       : "Consistent Top-8 Hackathon Finisher",
      "detail"      : "Multiple national-level events · HackEval creator",
      "status"      : "ACTIVE"
    },
    {
      "type"        : "🏢  Industry",
      "title"       : "4 Companies · 18+ Months Production AI",
      "detail"      : "OneClarity.ai  ·  Aiventory  ·  Liquid Minds  ·  KV Tech",
      "status"      : "ACTIVE"
    }
  ]
}
```

<br/>

<!-- ════════════════ STEP 6 ════════════════ -->

```python
# ── [STEP 6 / 6]  ·  metrics ─────────────────────────────────────────────────
thought = "Fetch the GitHub performance metrics. Render live."
action  = agent.tool_call("render_metrics", username="rish-23072005")
```

<div align="center">

<img height="175em" src="https://github-readme-stats.vercel.app/api?username=rish-23072005&show_icons=true&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00cfff&text_color=c9d1d9&rank_icon=github&include_all_commits=true" />
<img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rish-23072005&layout=donut-vertical&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=c9d1d9&langs_count=8" />

<br/>

<img width="70%" src="https://streak-stats.demolab.com?user=rish-23072005&theme=dark&hide_border=true&background=0d1117&stroke=1a2d4a&ring=00ff88&fire=ff6b35&currStreakLabel=00ff88&sideLabels=00cfff&dates=555&sideNums=ffffff&currStreakNum=ffffff" />

<br/>

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=rish-23072005&bg_color=0d1117&color=00ff88&line=00cfff&point=ff6b35&area=true&area_color=00ff8815&hide_border=true&custom_title=COMMIT+GRAPH)](https://github.com/rish-23072005)

![trophy](https://github-profile-trophy.vercel.app/?username=rish-23072005&theme=onestar&no-frame=true&no-bg=true&margin-w=6&column=7)

</div>

<br/>

<!-- ════════════════ FINAL ANSWER ════════════════ -->

```python
# ── FINAL ANSWER ──────────────────────────────────────────────────────────────
thought  = "All tools executed. Context complete. Synthesising final answer."
response = agent.generate_final_answer()
```

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║  FINAL ANSWER                                                                ║
║  ──────────────────────────────────────────────────────────────────────      ║
║                                                                              ║
║  Rishabh Tripathi is an AI Engineer with 18+ months of production            ║
║  experience across 4 companies, specialising in multi-agent systems,         ║
║  LLM infrastructure, and full-stack AI products.                             ║
║                                                                              ║
║  He designs systems where agents think, coordinate, and ship —               ║
║  the same way this profile was just rendered.                                ║
║                                                                              ║
║  ──────────────────────────────────────────────────────────────────────      ║
║  "Don't just consume technology. Create with it."                            ║
║                                               — Rishabh Tripathi             ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

```
  run completed  ·  6 / 6 steps  ·  all tools resolved  ✅
  rishabh_tripathi_agent — session/2026.05 — terminated cleanly.
```

<!-- FOOTER -->
<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,100:0d1117&height=4&section=footer" />
</div>
