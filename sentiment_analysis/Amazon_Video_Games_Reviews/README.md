# Amazon Video Games Ratings — Sentiment Analysis

This project analyzes Amazon video-game reviews by classifying sentiment and ranking titles by customer satisfaction.  
**Timeframe:** October 14, 1999 – July 22, 2014.

## 1. Project Overview
E-commerce platforms host vast amounts of unstructured review text, making it hard to convert thousands of opinions into clear signals. This notebook demonstrates how a **Large Language Model (Azure OpenAI, gpt-4o-mini)** can reliably label reviews as **positive** or **negative** and surface product-level insights.

The workflow filters the dataset to titles with **≥ 100 reviews** to ensure meaningful comparisons, yielding a focused subset (~**5,674 reviews**). Reviews are first explored with a **zero-shot** prompt and then scaled using a **few-shot** prompt built from curated “gold” examples. Inference is executed in batches and intermediate predictions are saved for reproducibility.

At the product level (ASIN), predictions are aggregated to compute **positive/negative counts**, a **sentiment ratio**, and then combined with the **average star rating** to form a simple **final score**. The result is a **top-10 / bottom-10** ranking of video-game titles for the period. While this notebook operates offline and isn’t connected to any live Amazon systems, it illustrates how Generative AI can turn free-text reviews into decision-ready insights for product, marketing, and support teams.

## 2. Capabilities Used

### 2a. Gen AI Capabilities Used
- **Zero-shot Prompting** — Baseline using a concise instruction to produce single-token labels (“positive”/“negative”) with deterministic decoding.  
- **Few-shot Prompting with Gold Examples** — Curated review→label pairs improve reliability; prompts assembled programmatically.  
- **Deterministic Outputs** — Temperature = 0, very small `max_tokens`, strict formatting for easy parsing at scale.  
- **Batched LLM Inference** — Chunked processing with progress tracking and simple backoff.  
- **Lightweight Gen-AI Evaluation** — Spot-checks against a hand-labeled set and iterative refinement of examples.

### 2b. Other Capabilities Used
- **Data Curation & Filtering** — Keep ASINs with ≥ 100 reviews (`data_100min`) for stable signals.  
- **Token Budgeting** — `tiktoken` for prompt sizing/estimation.  
- **Fault-Tolerant Processing** — Periodic CSV checkpoints to resume if interrupted.  
- **Aggregation & Ranking** — Per-ASIN counts, **Sentiment_Ratio**, merged star ratings, **Final_Score** and top/bottom-10 tables.  
- **Title Enrichment** — ASIN→title lookups (Tavily) for readable outputs and HTML-styled DataFrame presentation.

## 3. Data Source
- **Dataset:** Hugging Face — `LoganKells/amazon_product_reviews_video_games` (Amazon customer reviews for Video Games).  
- **Scale:** ~**50,000** total reviews across ~**3,400** unique video games (ASINs).  
- **Analysis subset:** Products with **≥ 100 reviews**, yielding **5,674** reviews in the working set (`data_100min`).

## 4. Dependencies
- Python 3.x  
- Jupyter  
- ipykernel  
- openai or azure-ai-openai  
- tiktoken  
- tavily-python  
- IPython  
- session_info  
- textwrap

## 5. How to Use
```bash
# Clone the umbrella repo and enter the project folder
git clone https://github.com/musicwil/Projects-in-Artificial-Intelligence.git
cd Projects-in-Artificial-Intelligence/sentiment_analysis/Amazon_Video_Games_Reviews

# (Optional) create a venv, then install deps
# python -m venv .venv && source .venv/Scripts/activate
pip install -r requirements.txt

# Set keys as needed
# export OPENAI_API_KEY=...         # or:
# export AZURE_OPENAI_API_KEY=... 
# export AZURE_OPENAI_ENDPOINT=...
# export TAVILY_API_KEY=...         # optional for ASIN→title lookups

# Open the notebook
jupyter notebook Amazon_Video_Games_Reviews.ipynb
```

> **Important — Gold Examples**  
> This notebook includes manually curated **ground-truth “gold examples.”**  
> If you rerun from scratch, **either skip/freeze those labeling cells** to preserve the existing gold set **or** be prepared to **manually recreate** the labels before inference.

## 6. Repository Structure
```text
Projects-in-Artificial-Intelligence/
└── sentiment_analysis/
    └── Amazon_Video_Games_Reviews/
        ├── assets/
        │   └── AmazonVideoGamesReviewsIntroImage.png
        ├── .gitignore
        ├── LICENSE
        ├── README.md
        ├── requirements.txt
        └── Amazon_Video_Games_Reviews.ipynb
```
> **Note:** `.gitignore` excludes local data, caches, and editor artifacts to keep the repo clean.

## 7. Assets
- **AmazonVideoGamesReviewsIntroImage.png** — A realistic image of two teenagers on a sofa playing a Formula-1 racing game on a large TV, with snacks and drinks on a table and a smiling girl leaning on the back of the sofa; **used for illustrative purposes in the notebook**.

## 8. How to Contribute
Contributions are welcome!

1. **Fork** this repo on GitHub (`musicwil/Projects-in-Artificial-Intelligence`).  
2. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   # or for fixes:
   git checkout -b fix/short-bug-name
   ```
3. **Commit** with clear messages:
   ```bash
   git add .
   git commit -m "feat: short summary of change"
   ```
4. **Push** and **open a Pull Request** with a brief description and any relevant screenshots.

## 9. .gitignore
This project includes a `.gitignore` to keep the repository lean and professional. It excludes:
- Python/Jupyter caches and checkpoints  
- Virtual environments  
- OS/editor artifacts  
- Local data files and logs

## 10. License
**MIT** © 2025 Will Contreras. See `LICENSE` for details.

## 11. Author
Will Contreras developed this project to leverage an **Azure OpenAI** model to generate reliable sentiment labels from raw Amazon video-game reviews and combine them with star ratings for a more faithful evaluation of titles. The workflow produces clear, reproducible leaderboards—**Top 10** and **Bottom 10**—grounded in both model-generated sentiment and observed ratings.
