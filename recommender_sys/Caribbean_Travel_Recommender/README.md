# Caribbean Travel Recommender

This project simulates a **Generative AI–powered travel agent** specializing in weekend getaways to the Caribbean.  
It was developed as part of the **5-Day Gen AI Intensive Course with Google (Capstone Project)**.

---

## 1. Project Overview
Traditional travel websites rely on static listings or rigid, rule-based recommendation systems, which limit personalization.  
This project demonstrates how a **Large Language Model (LLM)** can dynamically generate relevant promotional content and interpret user queries in a flexible, context-aware way — creating a more intuitive and engaging travel planning experience.

While this notebook is a simulation and does not connect to real-time booking or inventory systems, it highlights the **potential of Generative AI** to power intelligent travel agents.

---

## 2. Gen AI Capabilities Used
- **Few-shot Prompting**  
  Used to guide the generation of initial travel promotion descriptions, ensuring consistent format and style.  
- **Embeddings (Gemini model)**  
  Travel promotions are converted into embeddings that capture semantic meaning, enabling similarity-based recommendations.  
- **Retrieval Augmented Generation (RAG)**  
  When a user submits a query, its embedding is matched with stored promotions to retrieve the most relevant options.  
- **Vector Search (Cosine Similarity)**  
  The `vector_search` function ranks and retrieves the top-N most similar promotions to the user’s query.  
- **Gen AI Evaluation**  
  The generated promotions are evaluated by the LLM itself against criteria such as relevance, attractiveness, conciseness, and accuracy.

---

## 3. Data Source
This project does **not** use an external dataset.  
All travel promotion descriptions and package details are **synthetically generated** using the LLM (Gemini API) through few-shot prompting and content generation.  

---

## 4. Dependencies
```txt
google-genai==1.7.0
google-api-core
numpy
scikit-learn
ipython```

---

## 5. How to use

git clone https://github.com/musicwil/Projects-in-Artificial-Intelligence.git
cd Projects-in-Artificial-Intelligence/recommender_sys/Caribbean_Travel_Recommender
Install the required dependencies:
pip install -r requirements.txt
Open the notebook:
jupyter notebook Caribbean_Travel_Recommender.ipynb
Run all cells in order.
Generated descriptions and visuals will appear directly in the notebook and be stored in the assets/ folder.

---

## 6. Repository Structure

Caribbean_Travel_Recommender/
├── Caribbean_Travel_Recommender.ipynb   # Main notebook
├── assets/                              # Folder for assets
│   └── caribbean_beach_couple.png       # Caribbean beach illustration
├── requirements.txt                     # Project dependencies
├── .gitignore                           # Ignore rules for notebook workflow
├── LICENSE                              # MIT license
└── README.md                            # Project documentation

---

## 7. Assets
caribbean_beach_couple.png
A realistically generated Caribbean beach scene with a couple running happily along the shore, used for illustrative purposes in the notebook.

---

## 8. How to Contribute

Contributions are welcome!
Fork the repository.
Create a new branch for your feature (git checkout -b feature/YourFeature).
Commit and push your changes.
Open a Pull Request for review.

---

## 9. License

This project is licensed under the MIT License — see the LICENSE file for details.

---

## 10. Author

Will Contreras
Developed during the Google Gen AI Intensive Capstone Project.

---
