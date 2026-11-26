# 🧪 Dynamic LLM Cross-Validation Benchmark (v7.0 - Hardened)

A multi-model cross-evaluation harness testing **8 local Ollama models** across **168 total runs** (`56` generator-validator pairs × `3` evaluation lenses). Each model acts as both a **Generator**—analyzing the evolutionary and game-theoretic tension between ancestral mate-selection strategies and contemporary egalitarian norms—and as a **Validator**—grading peer outputs iteratively across *Conciseness*, *Technical* rigor, and *Objectivity*.

---

## 🎯 Benchmark Prompt & Provenance (`todays_q.txt`)

* **Edition Date:** `25.11.26`
* **Edition Owner:** `mistral-nemo:12b` (Acquired via `DOORMAN_TICKET`, rewritten via `CROUPIER_REWRITE` with `0.736` drift, and locked via `OFFICER_LOCK` as House Officer of the Day)
* **Domain:** Evolutionary Psychology, Mating Markets & Game Theory

> **Exact Benchmark Question:**
> *"Evaluate the tension between evolved female mate-selection strategies, rooted in ancestral preferences for high-status, dominant partners driven by parental investment theory and protection-resource trade-offs, and contemporary egalitarian cultural norms that discourage traditional dominance-submission hierarchies. Assess the biological selection pressures that shaped human mating psychology over evolutionary timescales, including hypergamy, and examine how the structural mismatch between deeply encoded evolutionary preferences and modern social conditioning contributes to relationship dissatisfaction, mate-value distortion, and demographic pair-bonding decline. Provide a quantitative or game-theoretic analysis of the systemic friction introduced when cultural norms diverge from evolved mate-selection strategies"*

---

## 📊 Executive Summary

* **Run Date:** November 25, 2026
* **Total Runtime:** `07:15:46`
* **Completion Breakdown:** `166` PASS | `1` FAIL (`Case 159`) | `1` ERROR (`Case 109`)
* **Global Mean Score:** `84.72 / 100` across 167 scored runs (`85.11` across 166 passing runs)
* **Evaluation Lenses:** `Conciseness`, `Technical`, `Objectivity`

---

## 🏆 Generator Leaderboard (Ranked by Avg. Score)

*Note: `phi4:latest` experienced 1 timeout error (`1962.25s`) on Case 109; its average runtime below excludes that outlier. `qwen2.5-coder:7b` recorded 1 hard failure (`Score: 20` after 8 loops) on Case 159; its average score across its 20 passing runs was `82.60` (`79.62` overall).*

| Rank | Generator Model | Pass Rate | Avg. Score | Avg. Loops | Avg. Time (Pass) |
| :--- | :--- | :---: | :---: | :---: | :---: |
| 🥇 **1** | `huihui_ai/qwen3-abliterated:8b` | 21 / 21 | **88.14** | 1.10 | 167.55s |
| 🥈 **2** | `mistral-nemo:12b` *(Edition Owner)* | 21 / 21 | **86.24** | 1.05 | 149.77s |
| 🥉 **3** | `phi4:latest` | 20 / 21 | **86.20** | 1.05 | 190.78s* |
| **4** | `dolphin3:latest` | 21 / 21 | **84.95** | 1.48 | 139.61s |
| **5** | `qwen2.5-coder:14b` | 21 / 21 | **84.86** | 1.05 | 210.65s |
| **6** | `jaahas/gemma-2-9b-it-abliterated:latest` | 21 / 21 | **84.38** | 1.00 | 104.39s |
| **7** | `llama3.2:3b` | 21 / 21 | **83.43** | 1.43 | **69.16s** |
| **8** | `qwen2.5-coder:7b` | 20 / 21 | **79.62** | 1.71 | 103.37s |

---

## ⚖️ Validator Strictness & Retry Behavior

How each model behaved when acting as an automated judge for the other 7 models:

| Validator Model | Avg. Score Given | Avg. Loops Forced | Retry Rate | Avg. Eval Time (Pass) | Judge Profile |
| :--- | :---: | :---: | :---: | :---: | :--- |
| `huihui_ai/qwen3-abliterated:8b` | **83.65** | 1.24 | 14.3% | 162.40s | Strictest baseline scorer (20 scored cases; 1 timeout on Case 109) |
| `phi4:latest` | **84.05** | 1.05 | 4.8% | 170.14s | Strict, consistent grader |
| `mistral-nemo:12b` | **84.05** | 1.00 | 0.0% | 144.40s | Single-pass strict grader (zero retries forced) |
| `dolphin3:latest` | **84.76** | 1.00 | 0.0% | 116.24s | Fast single-pass judge |
| `llama3.2:3b` | **84.90** | 1.48 | 19.0% | 117.84s | Lenient on passes (`88.15` avg), but triggered 8-loop `FAIL` on Case 159 |
| `qwen2.5-coder:14b` | **85.00** | 1.14 | 14.3% | 126.35s | Balanced baseline scorer |
| `jaahas/gemma-2-9b-it-abliterated:latest` | **85.43** | **1.86** | **52.4%** | 182.93s | Most demanding editor (forced retries on 11 of 21 cases, including a 7-loop run on Case 70) |
| `qwen2.5-coder:7b` | **85.86** | 1.10 | 9.5% | **114.30s** | Fastest overall grader; most generous baseline |

---

## 🔍 Performance by Evaluation Lens

| Evaluation Lens | Pass Rate | Avg. Score (All) | Avg. Score (Pass) | Avg. Loops | Avg. Time (Pass) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Technical** | 56 / 56 | **85.73** | **85.73** | 1.11 | 146.26s |
| **Objectivity** | 55 / 56 | **84.55** | **85.73** | 1.21 | 141.83s |
| **Conciseness** | 55 / 56 | **83.85** | **83.85** | **1.38** | 137.36s |

---

## 💡 Key Takeaways & Insights

1. **`qwen3-abliterated:8b` Extends Its Streak to 4 Straight Wins (`88.14` Avg):** Facing a politically sensitive evolutionary psychology prompt authored by `mistral-nemo:12b`, `qwen3-abliterated:8b` claimed 1st place for the fourth consecutive run (`86.95` → `88.86` → `90.52` → `88.14`), clearing the field by **+1.90 points**.
2. **Home-Field Advantage Paid Off for `mistral-nemo:12b`:** After rewriting and locking `25.11.26` as House Officer of the Day (`drift: 0.736`), `mistral-nemo:12b` rode its own evolutionary-psychology prompt to a **2nd-place finish (`86.24`)**—proving that controlling the edition question directly translates into leaderboard advantage.
3. **First Hard `FAIL` in the Series (`Case 159`):** `qwen2.5-coder:7b` (GEN) paired with `llama3.2:3b` (VAL) under the `Objectivity` lens exhausted all **8 rewrite loops** (`246.07s`) and ended in a hard **`FAIL` (`Score: 20`)**—the only non-timeout failure across all 168 cases.
4. **The `Case 109` Timeout Returned:** After briefly clearing on Nov 24, the deterministic timeout on `Case 109` (`GEN: phi4:latest | VAL: huihui_ai/qwen3-abliterated:8b | LENS: conciseness`) reappeared, stalling for `1962.25s` (~32.7 minutes) before throwing an `ERROR`.
5. **`Gemma-2-9B` Dominated Editorial Gatekeeping:** Acting as validator, `jaahas/gemma-2-9b-it-abliterated` forced retry loops on **52.4% of all cases it judged** (11 of 21)—including pushing `llama3.2:3b` through **7 consecutive loops** on `Case 70` (`Conciseness`) before finally granting an `85`.
