# The Warehouse is the Co-Pilot
### *A New Paradigm for M&A Due Diligence*

> A submission for the Google Cloud BigQuery AI Hackathon (September 2025). This project demonstrates a groundbreaking workflow that combines all three hackathon tracks: AI Architect, Semantic Detective, and Multimodal Pioneer.

---

## 📖 The Problem: The M&A Data Room Dilemma

In any multi-billion dollar M&A deal, the "data room" is a digital swamp of unstructured data: thousands of PDF contracts, scanned documents, and email chains. This critical business information is **opaque to traditional analytics**, rendering standard databases and reporting tools useless.

As a result, legal teams must resort to a dangerously slow and expensive process of manual review, where **highly-paid lawyers spend weeks acting as human keyword scanners**. This process is not only inefficient but fraught with risk, as a single missed "poison pill" clause or hidden liability can cost millions and jeopardize the entire deal.

## ✨ Our Solution: The Warehouse Co-Pilot

Our solution is **The Warehouse Co-Pilot**, an AI-powered due diligence engine built entirely within **Google BigQuery**. It introduces a new paradigm by treating the data warehouse as the central nervous system for analysis, bringing powerful AI capabilities directly to the data, rather than moving data out to the AI.

This entire workflow is orchestrated with a few lines of **SQL**, replacing what would traditionally be a complex data engineering pipeline with a simple, scalable query. The result is the ability to **query the unqueryable**—transforming the slow, manual review process into a fast, automated, and accurate data analysis task that allows legal teams to find multi-million dollar risks in minutes, not weeks.

## 🏛️ Architecture

Our warehouse-native architecture ensures security, scalability, and simplicity by keeping all data and processing within the Google Cloud ecosystem.

*(Insert your downloaded diagram image here. In GitHub, you can just drag and drop the image into the text editor, and it will generate the link for you.)*

**The data flows through three main stages:**
1.  **Ingestion:** Unstructured PDFs and images stored in a **Google Cloud Storage** bucket are made accessible to the data warehouse via **BigQuery Object Tables**.
2.  **AI Analysis:** Using simple **SQL**, we call a **Remote Model** connected to **Gemini 1.5 Pro** to perform analysis and use **Vector Search** to find semantic similarities.
3.  **Output:** The results are instantly written to a new, structured **BigQuery Table**, ready for analysis and reporting.

## 🚀 Key Features

This project utilizes a powerful combination of BigQuery's cutting-edge AI capabilities:

* **Multimodal Pioneer 🖼️:** Uses **BigQuery Object Tables** to create a direct SQL interface over unstructured PDFs and PNG files, breaking down the barriers between structured and unstructured data.
* **AI Architect 🧠:** Leverages a **Remote Model** connected to **Gemini 2.5 Pro** and the `ML.GENERATE_TEXT` function to perform deep analysis and structured data extraction from complex legal documents.
* **Semantic Detective 🕵️‍♀️:** Implements **Vector Search** (using `ML.GENERATE_EMBEDDING` and `VECTOR_SEARCH`) to go beyond keywords and find conceptually similar clauses based on their meaning.

## 🛠️ How to Use

The entire project is contained within the `[your_notebook_name].ipynb` Kaggle notebook file. To run, you will need a Google Cloud project with the necessary APIs enabled, a service account with the required IAM permissions, and the sample data files uploaded to a GCS bucket.
