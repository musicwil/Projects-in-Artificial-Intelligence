# **ExpressWay Logistics - Sentiment Analysis**

This project classifies customer reviews for **ExpressWay Logistics** into positive or negative sentiment to monitor service quality and improve customer satisfaction.
It was completed as the final required task to graduate from the **Generative AI for Business with Microsoft Azure OpenAI Program** imparted by *Great Learning*.

## 1. Project Overview

Logistics companies receive a constant flow of customer feedback that is often unstructured and difficult to analyze at scale.
This notebook applies **Large Language Model (LLM) prompt engineering techniques** to classify reviews as **positive** or **negative**, providing both technical evaluation and business-oriented insights.

The workflow demonstrates how **few-shot prompting** can be used to improve classification accuracy and reliability, while also capturing actionable recommendations from the results. It highlights the potential of Generative AI to transform raw customer reviews into decision-ready insights for operations, quality control, and customer service teams.

## 2. Generative AI Capabilities Used

* **Prompt Engineering (Zero-shot & Few-shot prompting):** Applied to classify customer reviews into positive or negative sentiment, with few-shot examples improving reliability.
* **Large Language Model (Azure OpenAI):** Leveraged to process unstructured text and generate consistent, context-aware sentiment predictions.

## 3. Data Source  

The dataset used in this project was provided by **Great Learning** as part of the *Generative AI for Business with Microsoft Azure OpenAI Program*.  
Its original source was not disclosed, and the data is intended solely for educational and demonstration purposes within the scope of this project.  


## 4. requirements.txt  

The project requires the following packages:  

```txt
numpy==1.25.2
pandas==2.0.3
scikit-learn==1.2.2
openai==0.28.0
tabulate==0.9.0
tqdm==4.66.4
session_info==1.0.0
tiktoken

Install with:

pip install -r requirements.txt


## 5. How to Use

```bash
# Clone the umbrella repo and enter the project folder
git clone https://github.com/musicwil/Projects-in-Artificial-Intelligence.git
cd Projects-in-Artificial-Intelligence/sentiment_analysis/ExpressWay_Logistics

# (Optional) create a venv, then install deps
# python -m venv .venv && source .venv/Scripts/activate
pip install -r requirements.txt

# Set Azure OpenAI keys
export AZURE_OPENAI_API_KEY=...
export AZURE_OPENAI_ENDPOINT=...

# Open the notebook
jupyter notebook "ExpressWayLogistics.ipynb"

```

```markdown
## 6. Repository Structure

```text
Projects-in-Artificial-Intelligence/
├── LICENSE
├── projects/
├── recommender_sys/
└── sentiment_analysis/
    ├── Amazon_Video_Games_Reviews/
    └── ExpressWay_Logistics/
        ├── README.md
        ├── requirements.txt
        ├── .gitignore
        ├── ExpressWayLogistics.ipynb
        └── assets/
            ├── ExpressWayLogistics.png
            └── courier-service_reviews.csv

```



## 7. Assets

* `ExpressWay Logistics.png` — Project image.
* `courier-service_reviews.csv` — Dataset provided by Great Learning for this project.

## 8. How to Contribute

Contributions are welcome!

1. Fork this repo on GitHub (`musicwil/Projects-in-Artificial-Intelligence`).
2. Create a branch:

   ```bash
   git checkout -b feature/your-feature-name
   # or for fixes:
   git checkout -b fix/short-bug-name
   ```
3. Commit with clear messages:

   ```bash
   git add .
   git commit -m "feat: short summary of change"
   ```
4. Push and open a Pull Request with a brief description and any relevant details.

## 9. .gitignore

This project includes a `.gitignore` to keep the repository lean and professional. It excludes:

* **Python/Jupyter** caches and checkpoints (`__pycache__/`, `.ipynb_checkpoints/`)
* **Virtual environments** (`.venv/`, `venv/`, `env/`)
* **OS/editor artifacts** (`.DS_Store`, `Thumbs.db`, `.vscode/`, `.idea/`)
* **Local scratch files and logs** (e.g., `*.log`, temporary outputs)

> Note: The project assets `ExpressWay Logistics.png` and `courier-service_reviews.csv` are intentionally **tracked** and not ignored.

## 10. License

This project is covered under the **MIT License**.
See the [LICENSE](../../LICENSE) file at the root of the repository for details.


## 11. Author

Will Contreras developed this project to apply **Azure OpenAI models** and **prompt engineering techniques** for classifying customer reviews of ExpressWay Logistics into positive and negative sentiment. The workflow produces clear, reproducible insights that connect technical evaluation with actionable business recommendations.

This project was completed as the **final required task to graduate** from the *Generative AI for Business with Microsoft Azure OpenAI Program* imparted by **Great Learning**.

