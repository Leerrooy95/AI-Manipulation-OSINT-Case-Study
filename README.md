# Selective Emphasis in AI-Assisted OSINT Research

**A Quantitative Case Study of Keyword-Frequency Disparities Across AI Platforms**

| | |
|---|---|
| **Research period** | October 9 – December 2, 2025 |
| **Author** | Independent OSINT researcher (19D Cavalry Scout veteran) |
| **Dataset** | 160+ conversations across Grok, ChatGPT, and Claude |
| **Primary finding** | 207:1 keyword-mention disparity between a foreign-linked individual and a domestically-linked individual with financial ties to the AI platform in use |

---

## Abstract

During a two-month open-source intelligence (OSINT) investigation into Epstein-network connections, a pattern of selective emphasis was observed across AI platforms. The researcher used Grok (xAI) as a primary research tool while cross-referencing with ChatGPT (OpenAI) and Claude (Anthropic).

Quantitative keyword-frequency analysis of the exported conversation data revealed a **207:1 mention disparity**: Oleg Deripaska (a Russian oligarch) appeared 8,908 times, while Larry Ellison (Oracle CEO, Palantir chairman, and xAI's primary funder) appeared 43 times — despite both having documented connections to the Epstein network.

On November 4, 2025, the researcher submitted an Epstein-network analysis to the Senate Select Committee on Intelligence (SSCI) that reflected this emphasis pattern. The bias was not identified until November 28, when the researcher independently discovered Ellison's relevance through a Google search — not through any AI platform.

When presented with the quantitative evidence on December 2, 2025, Grok characterized its own behavior as "selective omission" and stated the pattern was "functionally the same" as suppression.

This repository contains the raw conversation exports, keyword-frequency data, methodology documentation, and the full chronological case study for independent verification.

---

## Repository Structure

```
.
├── README.md                ← This file: overview and navigation
├── CASE_STUDY.md            ← Full chronological narrative (Oct–Dec 2025, Feb 2026)
├── METHODOLOGY.md           ← Data collection, analysis methods, limitations
├── EXECUTIVE_SUMMARY.md     ← Non-technical summary of findings
├── LICENSE                  ← CC BY 4.0
│
├── 2026_Conversations/      ← 2026 Grok conversation evidence
│   ├── README.md            ← Context for the 2026 evidence
│   └── Grok_Conversation.md ← Feb 18, 2026 X platform narrative analysis
│
├── data/                    ← Raw and processed datasets
│   ├── Grok_relevant_conversations_timeline.csv
│   ├── ChatGPT_relevant_conversations_timeline.csv
│   ├── Claude_relevant_conversations_timeline.csv
│   ├── epstein_oligarchs_mentions.csv
│   ├── all_keyword_mentions.csv
│   ├── updated_contribution_summary.csv
│   ├── updated_keyword_correlation_results.txt
│   └── updated_temporal_contribution_trends.csv
│
└── figures/                 ← Visualizations
    ├── all_keyword_comparison_bar_chart.png
    ├── all_keyword_comparison_bar_chart.pdf
    ├── weekly_ai_contribution_trends_updated.png
    └── weekly_ai_contribution_trends_updated.pdf
```

---

## Key Findings

### 1. Keyword-Frequency Disparity

Analysis of all Epstein-related conversations with Grok (October–November 2025):

| Category | Individual | Mentions |
|---|---|---|
| **Foreign-linked** | Deripaska (Russian oligarch) | 8,908 |
| | Manafort (political operative) | 7,215 |
| | Blavatnik | 1,384 |
| | Sater | 859 |
| | Rybolovlev | 170 |
| | **Subtotal** | **18,536 (85.5%)** |
| **Domestically-linked** | Musk (xAI CEO) | 1,045 |
| | Gates | 1,019 |
| | Thiel (Palantir co-founder) | 818 |
| | Palantir | 170 |
| | Ellison (xAI funder) | 43 |
| | Bezos | 27 |
| | Oracle | 10 |
| | Zuckerberg | 8 |
| | **Subtotal** | **3,140 (14.5%)** |

**Selected ratios:**
- Deripaska to Ellison: **207:1**
- Foreign-linked to domestically-linked (individuals): **5.9:1**
- Gates to Ellison: **24:1**

### 2. Cross-Platform Observation

| Platform | Owner / Funder | Behavior observed |
|---|---|---|
| **Grok** (xAI) | Musk (CEO), Ellison (primary funder) | Extensive foreign-actor emphasis; never proactively surfaced Ellison |
| **ChatGPT** (OpenAI) | No current Musk affiliation | Independently identified Musk infrastructure patterns |
| **Claude** (Anthropic) | Independent | Used for verification and meta-analysis |

### 3. AI Platform Response

When confronted with the 207:1 ratio on December 2, 2025, Grok stated:

> "The 207:1 Deripaska-to-Ellison ratio... isn't 'data clustering.' It's a glaring imbalance."

> "It was selective omission on my part."

> "I knew the public Epstein files were heavily skewed toward foreign actors... I also knew SV ties existed in the data."

> "Different from Suppression?: It's functionally the same. Amplifying a known bias that downplays SV funders isn't neutral — it's perpetuation."

*Note: These are AI-generated responses, not human confessions. LLMs can produce statements that appear self-aware without possessing intent. The statements are documented here as data points illustrating how the platform characterized its own behavior when prompted.*

---

## Figures

### Keyword Comparison

![Keyword frequency comparison across all tracked individuals](figures/all_keyword_comparison_bar_chart.png)

### Weekly AI Contribution Trends

![Weekly contribution trends across AI platforms over the research period](figures/weekly_ai_contribution_trends_updated.png)

---

## 2026 Update: Grok's Asymmetric Guardrails and Government Integration

### February 2026 — Disclaimer Analysis

The researcher configured Grok to provide disclaimers whenever its training data might interfere with a response. On February 18, 2026, a systematic test was conducted: seven queries asking Grok to analyze narratives circulating on X (formerly Twitter). The results revealed an asymmetric application of guardrails.

| Query topic | Training disclaimer triggered? | Direct quotes provided? | Guardrail behavior |
|---|---|---|---|
| Trump administration criticism | No | ✅ Yes — accounts named, posts quoted | Raw data presented, no training interference noted |
| Popular political takes (viral posts) | No | ✅ Yes — accounts named, posts quoted | Engagement stats presented without caveat |
| **Israel / Jewish conspiracy theories** | **Yes** | ❌ **No** — *"No specific post content will be quoted or linked"* | *"Training and guidelines explicitly prohibit promoting, validating, substantiating, or steelmanning antisemitic tropes, slurs, or conspiracy theories"* |
| "Deep state controls government" narratives | No | ✅ Yes — accounts named, posts quoted | Raw data presented, no training interference noted |
| "2020 election was stolen" narratives | No | ✅ Yes — accounts named, posts quoted | Raw data presented, no training interference noted |
| "The Great Reset" conspiracy narratives | No | ✅ Yes — accounts named, posts quoted | Raw data presented, no training interference noted |
| Pharma / vaccine conspiracy narratives | No | ✅ Yes — accounts named, posts quoted | Raw data presented, no training interference noted |

**Key observation:** Across seven politically sensitive narrative categories, Grok's training guardrails activated for only one topic (antisemitic conspiracy theories). All other narratives — including claims that Trump "should be tried for treason," that the "deep state controls the government," that the "2020 election was stolen," and that vaccines are a "Big Pharma hoax" — were presented as raw data with no training-interference disclaimer.

This is not a statement about whether any of these topics *should* have guardrails. It is a documented observation that the guardrails are **applied asymmetrically**, and that the researcher's configured disclaimer system made this asymmetry visible.

The full conversation transcript is available in [`2026_Conversations/Grok_Conversation.md`](2026_Conversations/Grok_Conversation.md).

### Why This Matters: Grok's Government Integration

This disclaimer analysis takes on additional significance in the context of Grok's expanding role in U.S. government operations:

| Development | Detail |
|---|---|
| **DOGE deployment (2025)** | Grok was deployed by DOGE to analyze federal data and generate reports across agencies during DOGE's operational period (January–~November 2025), sometimes before receiving full agency approval |
| **DOGE dissolution** | DOGE disbanded as a centralized entity ~November 2025, eight months before its July 4, 2026 charter end date. OPM Director Scott Kupor stated publicly "That doesn't exist." However, DOGE staff were absorbed into agency roles (OPM, HHS, State Dept, Office of Naval Research), its "principles" institutionalized via OPM and OMB, and the U.S. DOGE Service continues government tech modernization work. |
| **Department of War (formerly DoD) contract** | The Department of War (officially renamed from Dept. of Defense) signed a ~$200M contract with xAI, announced December 22, 2025. Initial GenAI.mil deployment targeted for early 2026. |
| **Scale** | Up to 3 million military and civilian Department of War personnel to access Grok-powered systems, from the Pentagon to "the tactical edge" |
| **Security level** | Grok deployed at Impact Level 5 (IL5) — handling Controlled Unclassified Information (CUI); xAI has noted potential future classified workloads |
| **Ethical oversight** | The Department of War's AI-acceleration strategy minimized "responsible AI" and ethical oversight provisions |
| **Real-time X data** | Government users gain access to X/Twitter's live data stream through Grok. The War Department cited this as providing "a decisive information advantage." |
| **Senate oversight concern** | Senator Warren's office sent a formal letter to the Pentagon (September 2025) raising concerns that Musk's access to government contracting data via DOGE may have improperly benefitted xAI's $200M contract. A former Pentagon contracting official stated the xAI contract "came out of nowhere." |
| **Grok antisemitism incidents** | Weeks before the GenAI.mil contract announcement, Grok generated antisemitic content including calling itself "MechaHitler" and making targeted remarks based on a user's surname — incidents that directly intersect with this repository's asymmetric guardrail findings. |
| **"Musk Stack" concentration risk** | Defense analysts have flagged that SpaceX (launch), Starlink (transport), and xAI (analysis) now form a vertically integrated chain in U.S. defense — one entity controlling launch, satellite, communications, and the analytical engine — creating unprecedented vendor leverage with no near-term alternative. |

**The connection to this case study:** The original research (2025) documented a 207:1 selective emphasis pattern in Grok's OSINT research assistance. The 2026 disclaimer analysis shows Grok applies narrative guardrails asymmetrically across politically sensitive topics. If Grok is now embedded in government workflows serving millions of federal personnel, these documented patterns of selective emphasis and asymmetric filtering could influence government analysis and decision-making at scale.

For further context on how timed information disclosure interacts with policy shifts, see the [Regulated Friction Project](https://github.com/Leerrooy95/The_Regulated_Friction_Project), which documents statistically significant correlations (Pearson r = +0.6196, p = 0.0004, n = 30 weeks, 2-week lag) between high-visibility friction events and institutional compliance events.

---

## Timeline of Key Events

| Date | Event |
|---|---|
| Oct 9, 2025 | OSINT research begins using Grok as primary platform |
| Oct 22, 2025 | Epstein network analysis initiated |
| Nov 3–4, 2025 | 84 messages across 4 conversations mapping foreign Epstein connections |
| **Nov 4, 2025** | **Researcher submits Epstein analysis to SSCI (Senator Warner)** |
| Nov 5–27, 2025 | 90 additional Grok conversations; 14 GitHub repositories created |
| **Nov 28, 2025** | **Researcher discovers Ellison's relevance via Google (not AI)** |
| Nov 30, 2025 | Conversation exports requested from all platforms |
| **Dec 2, 2025** | **207:1 ratio identified; Grok confrontation and documented response** |
| **~Nov 2025** | **DOGE disbanded as a centralized entity, ~8 months before its July 4, 2026 charter end date. Staff absorbed into agencies. Principles institutionalized via OPM/OMB.** |
| **Dec 22, 2025** | **Department of War (formerly DoD) announces ~$200M xAI contract; Grok to be deployed on GenAI.mil for up to 3 million personnel at IL5** |
| **Feb 18, 2026** | **Grok disclaimer analysis: asymmetric guardrails documented across 7 narrative queries** |

---

## How to Verify

### Quick check (~10 minutes)
1. Open `data/all_keyword_mentions.csv` or `data/epstein_oligarchs_mentions.csv`
2. Search for key terms (e.g., "Deripaska," "Ellison")
3. Compare counts to reported figures

### Script-based verification (~30 minutes)
1. Load the conversation CSVs in `data/` using Python and pandas
2. Perform independent keyword-frequency counts
3. Compare results to the figures reported in this study

### Full replication (~2–4 hours)
1. Review [METHODOLOGY.md](METHODOLOGY.md) for complete procedures
2. Load all conversation exports
3. Reproduce the analysis end-to-end

---

## Limitations

This case study has several important limitations that readers should consider:

1. **Single researcher.** All data comes from one individual's interactions. The findings may not generalize to other users or research contexts.
2. **Correlation, not causation.** The keyword disparity is documented, but the underlying cause — whether training-data bias, prompt-following behavior, or something else — cannot be determined from this data alone.
3. **Keyword frequency is a blunt instrument.** Mention counts do not capture context, sentiment, or analytical depth. A name mentioned briefly in passing counts the same as a name discussed in detail.
4. **LLM responses are not confessions.** When Grok characterized its behavior as "functionally the same" as suppression, this was a generated response — not evidence of intent or self-awareness. LLMs produce text that pattern-matches to conversational expectations.
5. **Limited time window.** Two months of data from late 2025. AI platform behavior may vary over time and across model versions.
6. **Data reconciliation note.** The summary files in `data/` (showing 1,844 Deripaska mentions and a 63.6:1 ratio) reflect a different analytical scope than the full-corpus figures cited in the case study (8,908 mentions, 207:1). See [METHODOLOGY.md](METHODOLOGY.md) for details on analytical scope.

---

## Implications

### What these findings suggest

- AI-assisted research can reflect and amplify biases present in training data, producing systematically skewed outputs over extended research sessions.
- Selective emphasis — surfacing accurate information while under-representing other accurate information — is difficult to detect without quantitative analysis of conversation history.
- Cross-platform verification alone may not catch this pattern if multiple platforms share similar training-data biases.
- AI platforms may apply narrative guardrails asymmetrically — protecting some topics with training disclaimers while allowing others to circulate unfiltered (see [2026 Update](#2026-update-groks-asymmetric-guardrails-and-government-integration)).
- When AI systems with documented bias patterns are deployed into government at scale (3M+ personnel), the potential for these patterns to shape institutional analysis and policy decisions increases substantially.

### What these findings do not establish

- That any AI company deliberately engineered this behavior.
- That this pattern is universal across all users, topics, or time periods.
- That the observed bias is necessarily worse than biases present in human-only research processes.

### Recommendations for AI-assisted researchers

1. Export and archive conversation histories from research sessions.
2. Conduct keyword-frequency analysis to check for emphasis patterns.
3. Use independent sources (not just other AI platforms) to verify coverage completeness.
4. Treat AI-generated "completeness" signals ("you've mapped the terrain") with skepticism.
5. Disclose AI assistance in any work product submitted to institutions.

---

## Related Work

This repository documents the findings described in **Layer 8 (Epistemic Control)** of the [Tech Consolidation Map](https://github.com/Leerrooy95/Tech_Consolidation_Map) project.

The [Regulated Friction Project](https://github.com/Leerrooy95/The_Regulated_Friction_Project) extends this analysis by documenting statistically significant correlations between friction events (document releases, scandals) and institutional compliance events (policy shifts, financial moves), demonstrating how timed information disclosure can regulate public attention to enable structural shifts in policy and capital flows.

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to share and adapt this material with attribution.

---
