# **AI Research Assistant – Phase 1: Data Collection & Retrieval**  

## **Overview**  
This project aims to develop an **AI-powered research assistant** capable of retrieving and summarizing relevant scholarly papers. In **Phase 1**, we focused on:  

- **Web Scraping**: Extracting research papers from **Semantic Scholar** for five AI topics.  
- **Data Processing**: Cleaning and structuring the retrieved data for further use.  
- **Retrieval-Augmented Generation (RAG)**: Implementing a **vector search pipeline** for finding relevant papers.  
- **Summarization**: Using **NLP models** to generate concise summaries of research papers.  

---

## **1️⃣ Data Collection – Web Scraping**  
We extracted **research papers published after 2017** from **Semantic Scholar** for the following topics:  

- **Foundation Models**  
- **Generative Models**  
- **Large Language Models (LLM)**  
- **Vision-Language Models (VLM)**  
- **Diffusion Models**  

### **Methodology**  
✅ **API-based Crawling**: Used the **Semantic Scholar API** to retrieve papers with **title, abstract, authors, and citation count**.  
✅ **Pagination Handling**: Implemented an automated loop to fetch **all relevant papers** for each topic.  
✅ **Filtering & Sorting**: Retrieved papers **published after 2017** and sorted them by **relevance**.  
✅ **Data Storage**: Saved data in **structured JSON format** for easy access.  

### **Example JSON Structure**  
```json
[
  {
    "year_range": "2017-2023",
    "papers": [
      {
        "title": "Example Paper Title",
        "abstract": "This paper explores...",
        "authors": "Author1, Author2",
        "citations": 23
      }
    ]
  }
]
```

---

## **2️⃣ Retrieval-Augmented Generation (RAG)**  
To efficiently search and retrieve research papers, we implemented a **RAG pipeline** using **semantic search and vector databases**.  

### **Pipeline**  
1️⃣ **Preprocessing**  
   - Loaded and cleaned the **DBLP dataset** (`dblp-v10.csv`).  
   - Processed papers in **chunks** to handle large-scale data efficiently.  

2️⃣ **Embedding Generation**  
   - Used **SentenceTransformers (`all-MiniLM-L6-v2`)** to generate embeddings for paper **titles + abstracts**.  
   - Stored these embeddings for fast retrieval.  

3️⃣ **Vector Database with FAISS**  
   - Indexed embeddings using **FAISS (Facebook AI Similarity Search)**.  
   - Used **L2 distance-based retrieval** to find similar research papers.  

4️⃣ **Semantic Search Implementation**  
   - Encoded user queries into vector embeddings.  
   - Performed **nearest-neighbor search** in FAISS.  
   - Retrieved and displayed the **top-K most relevant papers**.  

### **Example Search Query**  
```python
query = "Neural networks for NLP"
results = search_papers(query, top_k=5)
```

---

## **3️⃣ Named Entity Recognition (NER) for Author-Based Search**  
In addition to keyword-based search, we implemented **author-based search** using **Named Entity Recognition (NER)**.  

### **How It Works**  
✅ **Extracts Author Names** from user queries using **SpaCy’s NER model**.  
✅ **Filters Research Papers** by matching extracted author names.  
✅ **Returns the most relevant papers** authored by the given researcher.  

### **Example Author Search**  
```python
author_results = search_papers(author="S. Lawrence", top_k=5)
```

---

## **4️⃣ Research Paper Summarization**  
To provide concise insights, we integrated **automatic summarization** using a **local NLP model** (`facebook/bart-large-cnn`).  

### **Summarization Pipeline**  
✅ **Loads the research paper's title, abstract, and authors**.  
✅ **Uses a transformer-based NLP model** to summarize long abstracts.  
✅ **Displays key contributions in a structured format**.  

### **Example Summarization**  
```python
summary = summarize_paper_local(title, abstract, authors)
print("🔍 Paper Summary:\n", summary)
```

---

## **5️⃣ Challenges & Next Steps**  
### **Challenges Faced**  
❌ **API Rate Limits**: Implemented retry mechanisms to avoid request blocking.  
❌ **Missing Metadata**: Handled missing abstracts and author details using placeholders.  
❌ **Filtering Noise**: Some retrieved papers were not highly relevant to the queried topics.  

### **Next Steps – Phase 2**  
🚀 **Expand Dataset**: Scrape more research papers from additional sources.  
🚀 **Improve Relevance Ranking**: Enhance search results using **BERT-based re-ranking**.  
🚀 **Develop Interactive UI**: Create a web-based tool for users to interact with the assistant.  

---

## **💡 How to Run This Project?**  
1️⃣ Clone this repository:  
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```

2️⃣ Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3️⃣ Run the search assistant:  
   ```python
   query = "Generative Adversarial Networks"
   results = search_papers(query, top_k=5)
   ```

---

## **📌 Summary**  
✅ **Built a web scraping pipeline** to collect AI research papers.  
✅ **Implemented a vector search system (FAISS) for semantic retrieval**.  
✅ **Added NER-based author search** to find papers by specific researchers.  
✅ **Integrated NLP summarization** for concise paper summaries.  
✅ **Prepared structured datasets** for future AI model training.  

🚀 This **AI Research Assistant** is now ready for **Phase 2**, where we will enhance search capabilities, improve relevance ranking, and build a user-friendly interface!  


