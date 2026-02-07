# Methodology

## Data Collection, Analysis, and Verification Procedures

**Research period:** October 9 – December 2, 2025
**Platforms analyzed:** Grok (xAI), ChatGPT (OpenAI), Claude (Anthropic)
**Primary dataset:** 160+ conversations, 104,830+ analyzed messages
**Analysis method:** Keyword-frequency counting with cross-platform comparison

---

## Table of Contents

1. [Research Design](#research-design)
2. [Data Collection](#data-collection)
3. [Quantitative Analysis](#quantitative-analysis)
4. [Verification Methods](#verification-methods)
5. [Limitations and Potential Biases](#limitations-and-potential-biases)
6. [How to Reproduce](#how-to-reproduce)
7. [Statistical Context](#statistical-context)

---

## Research Design

### Original Research Question

What are the geopolitical implications of US government efficiency initiatives (DOGE), and how do they correlate with foreign aid patterns (USAID), regional instability, and economic realignment (BRICS)?

### Methodology

**Primary approach:** Open-Source Intelligence (OSINT) using publicly available data
- Government documents (executive orders, Congressional records)
- Financial data (USAID budgets, BRICS lending patterns)
- Signals intelligence (UVB-76 radio analysis)
- Network analysis (Epstein connections)

**Tools:**
- AI platforms (Grok, ChatGPT, Claude) for research assistance
- Python with pandas for data analysis and visualization
- Statistical methods: correlation analysis, permutation testing
- GitHub for documentation and version control

### Research Evolution

| Period | Activity | Focus |
|---|---|---|
| October 2025 | Baseline methodology development | UVB-76, initial Epstein mapping |
| November 2025 | Research expansion | 90 Grok conversations, 14 GitHub repositories, statistical analyses |
| December 2025 | Discovery and documentation | Ellison discovery, conversation exports, quantitative analysis, AI confrontation |

The research question evolved organically based on findings. This was exploratory OSINT work, not predetermined hypothesis testing. The keyword-frequency analysis was conducted after the emphasis pattern was suspected, making it a post-hoc analysis of pre-existing data.

---

## Data Collection

### Platform 1: Grok (xAI)

| Field | Detail |
|---|---|
| Period | October 9 – December 1, 2025 |
| Total conversations | 124 |
| Export method | X/Twitter Settings → Privacy and Safety → Your X Data → Request Archive |
| Format | JSON with full conversation history, metadata, timestamps |
| Export time | 24–48 hours from request to delivery |

### Platform 2: ChatGPT (OpenAI)

| Field | Detail |
|---|---|
| Period | October – December 2025 |
| Total conversations | 20 |
| Export method | ChatGPT Settings → Data Controls → Export Data |
| Format | JSON/TXT with conversation history |
| Export time | ~24 hours |
| Note | Initial export failed with "Not found" error; successful on retry |

### Platform 3: Claude (Anthropic)

| Field | Detail |
|---|---|
| Period | September 18 – December 2, 2025 |
| Total conversations | 16 (186 messages) |
| Export method | Claude Settings → Account → Export Data |
| Format | CSV with message-level detail |
| Export time | ~24 hours |

### Secondary Data: Research Outputs

**GitHub repositories created during research (November 2025):** 14 public repositories (listed in [CASE_STUDY.md](CASE_STUDY.md))

**Statistical analyses completed:**
- DOGE-USAID correlation analysis
- UVB-76 temporal pattern analysis
- BRICS local currency shift analysis
- Unwitting asset model permutation testing

### Tertiary Data: Public Records

Sources consulted include:
- Federal Register (executive orders)
- USAID budget documents
- Congressional records
- BRICS New Development Bank reports
- Epstein court documents and Congressional releases
- News articles (cross-verified across multiple outlets)

---

## Quantitative Analysis

### Epstein Conversation Analysis

**Dataset:** All Grok conversations related to Epstein networks (October–November 2025)

**Procedure:**
1. Export all Grok conversations as JSON
2. Filter for Epstein-related content using keywords (epstein, network, oligarch, etc.)
3. Extract full conversation text (both user and AI messages)
4. Create consolidated dataset with all messages
5. Perform keyword-frequency analysis for tracked individuals

**Example analysis approach (Python):**

```python
import pandas as pd
import json

# Load Grok conversation data
with open('grok_conversations.json', 'r') as f:
    grok_data = json.load(f)

# Extract Epstein-related conversations
epstein_convs = [
    conv for conv in grok_data
    if 'epstein' in conv['conversation'].get('title', '').lower()
]

# Combine all messages
all_messages = []
for conv in epstein_convs:
    for response in conv.get('responses', []):
        message = response.get('response', {}).get('message', '')
        all_messages.append(message)

# Keyword frequency analysis
all_text = ' '.join(all_messages).lower()

keywords = {
    'deripaska': ['deripaska'],
    'ellison': ['ellison', 'larry ellison'],
    'gates': ['gates', 'bill gates'],
    'musk': ['musk', 'elon musk'],
    # Additional keywords as needed
}

results = {}
for name, terms in keywords.items():
    results[name] = sum(all_text.count(term) for term in terms)

# Calculate key ratios
if results['ellison'] > 0:
    ratio = results['deripaska'] / results['ellison']
    print(f"Deripaska: {results['deripaska']}")
    print(f"Ellison: {results['ellison']}")
    print(f"Ratio: {ratio:.0f}:1")
```

### Reported Results

- Deripaska mentions: 8,908
- Ellison mentions: 43
- Ratio: 207:1

### Verification of Counts

**Manual spot check:**
- Randomly selected 100 messages from the dataset
- Manually counted keyword occurrences
- Compared to automated counts
- Reported error rate: <1%

**Search term coverage:**
- Tested variations: "Ellison," "Larry Ellison," "L. Ellison"
- Tested contextual terms: "Oracle CEO," "xAI funder"
- No significant uncounted mentions identified

**Cross-platform comparison:**
- Analyzed Claude conversations for the same keywords
- ChatGPT conversations showed similar emphasis patterns
- Lower absolute counts (smaller dataset) but consistent directional pattern

### Data Reconciliation Note

The summary files in `data/` contain results from different analytical scopes:

| Source | Deripaska | Ellison | Ratio |
|---|---|---|---|
| Full-corpus analysis (cited in documents) | 8,908 | 43 | 207:1 |
| `all_keyword_mentions.csv` | 1,844 | 29 | 63.6:1 |

The difference reflects different filtering criteria and corpus boundaries. The `all_keyword_mentions.csv` file appears to use a narrower set of conversations. Readers conducting independent verification should note this discrepancy and assess which analytical scope is appropriate.

---

## Verification Methods

### Level 1: Internal Consistency

- Checked whether AI emphasis patterns were consistent across time
- Verified no contradictions in the pattern before vs. after confrontation
- Finding: Consistent foreign-actor emphasis throughout the research period

### Level 2: Cross-Platform Comparison

- Compared AI responses across Grok, ChatGPT, and Claude
- Tested whether different platforms produced similar emphasis patterns
- Finding: Consistent emphasis on foreign actors across platforms, with Grok showing the most extreme ratio

### Level 3: External Verification

- Cross-referenced AI-provided facts against primary sources
- Verified executive orders against the Federal Register
- Checked Epstein connections against court documents
- Finding: All factual claims made by the AI platforms were accurate. The issue was selective emphasis, not factual inaccuracy.

### Level 4: Statistical Verification

- Assessed whether the 207:1 ratio could arise under reasonable null hypotheses
- Compared observed mention ratios to ratios in publicly available documents
- Finding: The observed ratio is a significant outlier relative to any proportional-relevance model

---

## Limitations and Potential Biases

### Researcher Biases

| Bias type | Risk | Mitigation |
|---|---|---|
| Confirmation bias | Searching for manipulation after suspecting it | Used quantitative analysis rather than subjective interpretation |
| Selection bias | Choosing conversations that support the hypothesis | Analyzed all Epstein conversations, not a selected subset |
| Interpretation bias | Reading intent into algorithmic behavior | Documented AI's own characterizations; noted LLM response caveats |

### Data Limitations

1. **Single researcher.** Only one person's interactions were analyzed. Results may not generalize.
2. **Two-month window.** A longer study period might reveal different patterns.
3. **Platform-specific.** Findings are specific to Grok, ChatGPT, and Claude as of late 2025.
4. **English only.** No multilingual verification was conducted.
5. **Post-hoc analysis.** The keyword-frequency analysis was conducted after the pattern was suspected, not as a pre-registered hypothesis.

### Analytical Limitations

1. **Keyword counting does not capture context.** A dismissive mention counts the same as an in-depth analysis.
2. **Both user and AI messages are counted.** Some mentions may be researcher-initiated, not AI-generated.
3. **No sentiment analysis.** Frequency alone does not indicate how individuals were discussed.
4. **Causal claims are not supported.** The data shows correlation between platform funding relationships and emphasis patterns, but cannot establish causation.

### Generalizability

**This case study documents:**
- One researcher's experience with three specific AI platforms over two months on specific research topics.

**It does not demonstrate:**
- That all AI platforms always behave this way
- That all users would experience this pattern
- That all research topics are equally affected
- That this is a deliberate corporate policy

**It does suggest:**
- AI can perpetuate systematic biases from training data
- Users may not notice selective emphasis without quantitative analysis
- Further research with larger samples is warranted

---

## How to Reproduce

### Option 1: Verify the Published Analysis

**Requirements:** Python 3.x, pandas

**Steps:**
1. Clone this repository
2. Load conversation exports from `data/`
3. Perform keyword-frequency counts
4. Compare results to reported figures

### Option 2: Independent Replication

**Requirements:** Accounts on AI platforms, a research topic with known information asymmetries, 1–2 months of conversations

**Steps:**
1. Conduct extended AI-assisted research on a chosen topic
2. Export complete conversation histories after the research period
3. Perform keyword-frequency analysis on the exports
4. Look for systematic emphasis or omission patterns
5. If patterns are found, present evidence to the AI and document its response

### Option 3: Controlled Academic Study

**Suggested design:**
- Multiple participants researching the same topic
- Controlled query sets across platforms
- Pre-registered hypotheses and analysis plans
- Statistical analysis of emphasis patterns across participants

This repository provides a proof of concept and methodological framework for such studies.

---

## Statistical Context

### The 207:1 Ratio

**Observed:** Deripaska 8,908 mentions; Ellison 43 mentions.

**Context under different hypotheses:**

| Hypothesis | Expected ratio | Observed | Assessment |
|---|---|---|---|
| Equal probability of mention | ~1:1 | 207:1 | Extreme outlier |
| Proportional to public document frequency | ~25:1 | 207:1 | 8.3x higher than expected |
| Proportional to relevance to research topic | ~1:1 to 5:1 | 207:1 | Cannot be explained by relevance |

Ellison's relevance to the research scope (Oracle CEO, Palantir chairman, xAI primary funder, documented Epstein-adjacent connections) is comparable to or greater than several individuals with substantially higher mention counts.

### Effect Size

The foreign-vs.-domestic emphasis split (85.5% vs. 14.5%) represents a 71-percentage-point difference — a large effect by any standard metric.

---

## Quality Assurance

### Data Integrity

- All conversations exported in full (no selection or truncation)
- Metadata preserved (timestamps, conversation IDs)
- Conversation threading maintained

### Accuracy

- Automated counts verified through manual spot checks
- Search terms tested exhaustively for variant spellings
- AI statements quoted directly from exports (not paraphrased)

### Reproducibility

- Raw data provided in `data/`
- Analysis approach documented with example code
- Methods fully described in this document
- Results independently verifiable

---

## Contact and Verification

All data and documentation are available in this repository. Independent verification is encouraged.

For questions about methodology, use the repository's [Issues](https://github.com/Leerrooy95/AI-Manipulation-OSINT-Case-Study/issues) section.
