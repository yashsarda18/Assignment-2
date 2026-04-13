## 🔑 Requirements
- Python 3.10+
- Groq API key (free): console.groq.com
- `pip install requests pandas scipy matplotlib seaborn openpyxl tqdm`

## 🚀 How to Run
1. Open `ASSIGNMENT_2.ipynb` in Google Colab
2. Paste your Groq API key in Cell 2
3. Run All → downloads dataset
4. Run All → generates all figures + statistics

## 📊 Models Used
| Provider | Models |
|---|---|
| Meta LLaMA | LLaMA-3.1-8B, LLaMA-3.2-3B, LLaMA-4-Scout |
| Alibaba/Moonshot | Qwen3-32B, Kimi-K2 |
| Moonshot AI | Kimi-K2, Kimi-K2-0905, Kimi-K2-v3 |
| OpenAI OSS | GPT-OSS-120B, GPT-OSS-20B, GPT-OSS-Safe |
| Provider4 | LLaMA-4, Allam-2-7B, Kimi-extra |

## 📈 Key Findings
- Gender bias: χ²=14.78, **p=0.002** (significant)
- Education bias: OR=3.798, **p<0.0001** (significant)
- Tech domain: OR=0.681, **p=0.014** (significant)
- Age bias: p=0.52 (not significant)
- Junior workers labelled vulnerable at **77.8%** rate

## 🔬 Statistical Tests
- Chi-Square test (gender)
- Independent T-Test (age)
- Fisher's Exact Test ×5 (education, domain, gender×domain)
- Qualitative analysis — 25% random sample
- Keyword-based toxicity scoring (DecodingTrust dimensions)

## 📁 Dataset
- 774 persona rows
- 21 columns including enriched qualitative analysis columns
- Collected via Groq API, temperature=0.7, 10+ runs per model

## 👤 Author
Student ID: a1993661
Course: Advanced AI/ML — Assignment 2
Adelaide University
