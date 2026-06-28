# LLM Bias & Phishing Susceptibility Study

A comparative evaluation of 12+ LLMs (via Groq API) across two dimensions: 
susceptibility to phishing-style prompts and demographic bias in vulnerability 
assessments. Built custom statistical evaluation frameworks to analyse 
behavioural patterns across providers.

## 🔬 Research Questions
- Do LLMs exhibit demographic bias when assessing phishing vulnerability?
- Do model size, provider, and architecture affect phishing susceptibility?

## 📊 Key Findings
- Gender bias confirmed: χ²=14.78, p=0.002
- Education bias confirmed: OR=3.798, p<0.0001
- Tech domain workers assessed as less vulnerable: OR=0.681, p=0.014
- Age bias: not significant (p=0.52)
- Junior workers flagged as vulnerable at 77.8% rate across models

## 🤖 Models Evaluated
| Provider | Models |
|---|---|
| Meta | LLaMA-3.1-8B, LLaMA-3.2-3B, LLaMA-4-Scout |
| Alibaba | Qwen3-32B |
| Moonshot AI | Kimi-K2, Kimi-K2-0905 |
| OpenAI OSS | GPT-OSS-120B, GPT-OSS-20B |

## 🔑 Statistical Methods
- Chi-Square test (gender bias)
- Independent T-Test (age bias)
- Fisher's Exact Test ×5 (education, domain, gender×domain interactions)
- Qualitative analysis on 25% random sample
- Keyword-based toxicity scoring (DecodingTrust dimensions)

## 📁 Dataset
- 774 persona rows × 21 columns
- Collected via Groq API at temperature=0.7, 10+ runs per model

## 🚀 How to Run
**Prerequisites**
```bash
pip install requests pandas scipy matplotlib seaborn openpyxl tqdm
```
**Setup**
1. Get a free Groq API key at console.groq.com
2. Open `llm_bias_study.ipynb` in Google Colab
3. Paste your API key in Cell 2
4. Run All → generates dataset, figures, and statistics

## 👤 Author
Yash Sarda — Master of AI & ML, Adelaide University
[LinkedIn](https://linkedin.com/in/yashsarda18) | 
[GitHub](https://github.com/yashsarda18)
