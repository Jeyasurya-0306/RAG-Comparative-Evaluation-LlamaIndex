# RAG Comparative Evaluation: Optimizing Policy Document Q&A

## 💡 Project Summary

This project establishes a rigorous, **quantitative methodology** for building and optimizing a Retrieval-Augmented Generation (RAG) system using **LlamaIndex**. The core objective was to process the LIC New Jeevan Shanti policy document and determine the **optimal combination** of embedding models and Large Language Models (LLMs) by measuring response quality using **BERTScore**.

This work demonstrates deep proficiency in RAG pipeline development, model benchmarking, and quantitative evaluation.

---

## 🎯 Technical Objective & Evaluation

The primary goal was to move beyond qualitative testing and determine which RAG configuration produced the most faithful and correct answers based on the source policy document.

### Methodology Highlights:

1.  **Multiple Embedding Models Tested:** Evaluated **DistilBERT-MSMARCO**, **MiniLM-MSMARCO**, and **Sentence-T5-Large** to assess impact on retrieval quality.
2.  **LLM Synthesis Comparison:** Tested both **Flan-T5-base** and **OPT-350M** for synthesizing the final answer from the retrieved context.
3.  **Quantitative Evaluation:** Responses were validated against ground-truth answers using **BERTScore** to calculate Precision, Recall, and F1 scores (measuring faithfulness and semantic correctness).

---

## 🏗️ Technical Workflow

The project follows a five-stage LlamaIndex workflow detailed in the documentation and notebook:

1.  **PDF Parsing:** Used **LlamaParser** to extract structured and unstructured text from the Policy PDF.
2.  **Vector Store Indexing:** Parsed data was chunked and converted into a **Vector Store Index** for efficient semantic retrieval.
3.  **Embedding Generation:** Applied different embedding models to create vector representations.
4.  **Query & Synthesis:** The RAG system queries the index and feeds the retrieved context to the different LLMs for final answer generation.
5.  **Evaluation:** **BERTScore** was used to score the outputs against a curated set of reference answers.

### 📊 Key Findings (Example Data - Fill in Your Exact Results)

| Configuration | F1 Score (BERTScore) | Precision | Recall |
| :--- | :--- | :--- | :--- |
| **Optimal Result** | **[Insert Best F1 Score]** | **[Insert Precision]** | **[Insert Recall]** |
| (Achieved with) | **[Best Embedding Model Name]** | **[Best LLM Name]** | |

*(Note: The full, detailed results of all combinations are available in the **`basic_rag.ipynb`** notebook and the **Project Report**.)*

---

## 🛠️ Technical Stack & Files

| Category | Component | Purpose |
| :--- | :--- | :--- |
| **Framework** | LlamaIndex | Core RAG pipeline development and vector indexing. |
| **Language** | Python 3 | Core development. |
| **LLMs Tested** | Flan-T5-base, OPT-350M | Answer generation and synthesis. |
| **Evaluation** | BERTScore (using Hugging Face) | Quantitative measurement of response quality. |

### Project Files:

* **`basic_rag.ipynb`**: The complete, runnable Jupyter Notebook containing all the code, LlamaIndex setup, model comparisons, and the final BERTScore evaluation results.
* **`Building the RAG - Report.docx`**: The comprehensive project documentation, detailing the objectives, methodology, and conclusion.

---

## ⚙️ Setup and Execution

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[Jeyasurya-0306]/RAG-Comparative-Evaluation-LlamaIndex.git
    cd RAG-Comparative-Evaluation-LlamaIndex
    ```
2.  **Install Dependencies:** Install `llama-index`, `transformers`, `torch`, `datasets`, and other required libraries (You may need a `requirements.txt` file, or install dependencies directly from the notebook).
3.  **Run:** Open and execute all cells in the **`basic_rag.ipynb`** notebook sequentially to replicate the workflow and view the evaluation results.

## 🧑‍💻 Author

**Jeya Surya** | [https://www.linkedin.com/in/jeya-surya-2b8931378?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app] | [jeyasurya.m02@gmail.com]
