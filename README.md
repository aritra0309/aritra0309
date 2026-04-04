<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Hi+there%2C+I'm+Aritra!+%F0%9F%91%8B;Data+Science+Enthusiast;Python+Developer+I+Think?" alt="Typing SVG" />
</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=aritra0309&label=Profile%20Views&color=0e75b6&style=flat" alt="aritra0309" />
  <a href="https://github.com/aritra0309?tab=followers">
    <img src="https://img.shields.io/github/followers/aritra0309?label=Followers&style=social" alt="GitHub Followers" />
  </a>
</p>

---

## 🚀 About Me
I'm someone who just wants to make life easier.
- 🌱 Exploring **Large Language Models**, **Generative AI**, and **Agentic AI**
- 💡 Interested in almost anything, as long as it is not boring.
- 🛠️ Building with **Python** (I mean, some CLI agent is building it; I just guide and verify it)
- ⚡ Working on: automating my GitHub maintenance with a bot (I know Copilot can help, but I want local test-backed automation instead of assumption-based changes)
---

## 🛠️ Tech Stack

### Languages & Tools
<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache%20Hadoop-66CCFF?style=for-the-badge&logo=apachehadoop&logoColor=black" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</p>

### ML / AI Libraries
<p align="left">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white" />
</p>

---

## 📝 Project Blog (where I overshare my builds)
> A small diary for every repo: what I made, what went wrong, and what I learned.
### 📈 Nifty 50 Portfolio Optimizer
**Repo:** [nifty50-portfolio-optimizer](https://github.com/aritra0309/nifty50-portfolio-optimizer)
- **Why I made it:** I wanted to test whether one person can realistically predict the stock market with ML (short answer: not perfectly, but you can build a useful decision-support system).
- **What this repo does:** It uses LSTM-based forecasting on historical stock data and blends it with sentiment from company news. The news is passed through FinBERT, which outputs probabilistic sentiment scores (positive/negative/neutral), and those signals are used alongside price-based features for portfolio decisions.
- **Main challenge:** Data alignment. Stock prices are available daily, but news flow is irregular, so sentiment and price timelines do not naturally line up for every company on every day.
- **What I learned:** Building the model is only half the job; getting clean, synchronized data matters even more. I also learned that portfolio metrics must be unit-consistent (for example, return horizon vs. annualized volatility), or optimization can look smarter than it really is.
- **Next thing I want to add:** Standardize return/risk time horizons for a cleaner Sharpe ratio, improve the sentiment pipeline so its impact is consistently reflected in saved artifacts, and decouple the Nifty 50 ticker list from the artifact so index updates are automatic.
### 🔍 Hadoop Crime Project
**Repo:** [hadoop-crime-project](https://github.com/aritra0309/hadoop-crime-project)
- **Why I made it:** I built this to learn the Hadoop ecosystem hands-on (HDFS + Spark) using a real Indian crime dataset instead of toy examples, and to see how far I could take a full data pipeline from raw CSVs to forecasts and visualizations.
- **What this repo does:** It ingests district-level IPC crime data (2001–2014), normalizes schema differences across years, aggregates to state-year totals, clusters states by crime profile, forecasts trends to 2020 using model selection (Ridge/Polynomial/GBR), and exports interactive HTML outputs (Folium choropleth + state trend chart).
- **Main challenge:** Data and pipeline consistency: changing column names across files, weak state-name matching with GeoJSON, localhost-only HDFS paths, and dependency mismatch between code and requirements.
- **What I learned:** Reliable preprocessing and naming consistency matter more than model complexity. I also learned that forecasting on short historical windows needs careful validation and explicit assumptions.
- **Next thing I want to add:** Make config/path handling portable, use more of the available datasets, and add stronger forecast validation (Ridge regression on such a short time frame is not very reliable).
### 🎨 Drawing with LLM - PaliGemma 2
**Repo:** [drawing-with-llm-pali-gemma-2](https://github.com/aritra0309/drawing-with-llm-pali-gemma-2)
- **Why I made it:** I built this for the Kaggle "Drawing with LLMs" challenge to test whether I could turn plain-text prompts into valid SVGs with a real multimodal pipeline, not just a one-model demo.
- **What this repo does:** It runs an end-to-end flow: generate bitmap candidates with diffusion, convert them to compact SVGs (superpixels + contour simplification), and score outputs using VQA + aesthetic signals to choose the best final SVG.
- **Main challenge:** Combining diffusion, SVG conversion, and scoring under Kaggle GPU limits (OOM/retries), while handling artifact/path dependencies and metric quirks where tiny details can change leaderboard behavior.
- **What I learned:** This task is mostly a search-and-selection problem, not a one-shot generation problem. Generating one SVG per prompt is usually weaker than generating many candidates and ranking them with a metric-aligned scorer (my ranking suffered because of this). I also learned that OCR handling, text artifacts, and post-processing choices can matter as much as model choice.
- **Next thing I want to add:** A proper multi-candidate pipeline (32–64 images per prompt), SVG conversion + fast ranking for each candidate, OCR-aware scoring closer to the official metric, and a robust fast/quality mode so it stays reliable under Kaggle runtime constraints.
### 📚 ML Notebooks
**Repo:** [ML](https://github.com/aritra0309/ML)
- **Why I made it:** This repo is basically my ML origin story—early academic projects, Kaggle playground experiments, and random scripts that were too small to deserve their own repo. Some are beginner-level, and some include feature engineering, ensembling, and a bit of CUDA speed-up work.
- **What this repo does:** It is a collection of competition notebooks and personal ML experiments from my early days. Think of it as my training arc in public.
- **Main challenge:** Kaggle competition iteration can get intense fast—you start with one model and suddenly you are stacking XGBoost + CatBoost + LightGBM to squeeze out 0.002 more score.
- **What I learned:** XGBoost can carry you surprisingly far (like 95% of real-world tabular problems). Also, `RandomizedSearchCV` is a lifesaver when you do not want to brute-force every hyperparameter combination; it is a neat trick many beginners miss.
- **Next thing I want to add:** More Kaggle competitions—and hopefully one day, a Top 10 leaderboard finish.
### 🎬 YouTube Transcript Tool
**Repo:** [youtube-transcript-tool](https://github.com/aritra0309/youtube-transcript-tool)
- **Why I made it:** I wanted a simple CLI pipeline to fetch YouTube transcripts, translate them, and evaluate QA evidence without heavy infrastructure (I needed QA pairs for a RAG evaluation and did not want to manually process everything).
- **What this repo does:** It runs in 3 stages: transcript extraction, timestamp-preserving translation, and QA-evidence scoring with structured JSON/CSV/log outputs.
- **Main challenge:** Handling real-world input noise reliably—missing captions, translation provider failures, and keeping timestamps/output format consistent end-to-end.
- **What I learned:** Reliability and data formatting matter as much as scoring logic. A clean, repeatable pipeline is more valuable than overcomplicating the model side.
- **Next thing I want to add:** Nothing for now—project complete for my current use case.
### 🤖 GitHub Auto Maintainer
**Repo:** [github-auto-maintainer](https://github.com/aritra0309/github-auto-maintainer)
- **Why I made it:** Copilot helps with suggestions, but I wanted my own agentic maintainer that can observe GitHub events, reason with repo-specific rules, choose actions, and operate with full transparency and control.
- **What this repo does:** It currently provides the agent foundation layer: multi-provider LLM routing, normalized response contracts, retry logic for transient failures, and hook points for observability. The webhook-driven skill execution layer is the next step.
- **Main challenge:** Making autonomy safe and reliable—event verification, policy guardrails, deterministic tool behavior, and preventing low-signal or incorrect automated actions.
- **What I learned:** Honestly, I am learning almost everything in this project while building it—LLM routing, webhook security, event-driven orchestration, tool/action guardrails, and how to make an agent useful without making it noisy. That is exactly why this project is taking time: reliability is harder than generation.
- **Next thing I want to add:** Implement the full observe -> plan -> act loop: webhook ingestion + signature verification, skill planner, tool execution with validation checks, and human-review/dry-run modes before autonomous posting.

## 📊 GitHub Stats (Proof I Actually Ship Stuff)


<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=aritra0309&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="48%" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=aritra0309&theme=tokyonight&hide_border=true" width="48%" alt="GitHub Streak" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=aritra0309&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" width="48%" alt="Top Languages" />
</p>

---

## 🤝 Connect with Me

> Always happy to talk projects, ideas and opportunities

<p align="left">
  <a href="https://github.com/aritra0309" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-aritra0309-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
    <a href="mailto:aritrasarkar423@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-aritrasarkar423%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/aritra-s" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Aritra%20Sarkar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <i>✨ "I came for machine learning and stayed for debugging plot twists." ✨</i>
</p>



