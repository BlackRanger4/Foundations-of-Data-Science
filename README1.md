# 📚 **AI Research Assistant – Phase 1**  

## **Overview**  
This project aims to build an **AI-powered research assistant** that helps users find **relevant academic papers**.  
The dataset provided (DBLP) includes papers up to **2017**, but we enhanced it by **scraping recent research papers** and conducting **exploratory data analysis (EDA)**.  

### **Phase 1 Goals**  
This phase consists of:  
1. **Exploratory Data Analysis (EDA)** to uncover patterns in research papers.  
2. **Network Analysis** to understand relationships between papers, authors, and conferences.  
3. **Clustering & Community Detection** to group authors and papers based on similarity.  

The insights gained will later help develop **a citation predictor** and **a Retrieval-Augmented Generation (RAG) system** for AI-driven research assistance.  

---

## **📊 1. Exploratory Data Analysis (EDA)**  
### **1.1 Basic Analysis**  
We performed fundamental data analysis on the research dataset:  

- 📈 **Publication Trends:**  
  - Bar charts of the **number of publications** across different time periods (**1937-1950, 1950-1970, 1970-1990**).  
  - Number of **references and authors** over the years.  

- 📊 **Correlation Analysis:**  
  - Pearson & Spearman correlation between **number of authors and references**.  
  - Pearson & Spearman correlation between **number of authors and citations**.  

- 🔍 **Text Analysis:**  
  - **WordCloud** of frequently used terms in abstracts.  
  - Analysis of **title lengths over time**.  

- 🏆 **Top Researchers & Papers:**  
  - **Top 10 authors** with the most publications.  
  - **Top 10 papers** with the highest references and citations.  
  - Predicting **how well publication count correlates with citation count**.  

---

## **🌐 2. Network Analysis**  
### **2.1 Citation Network (Paper-Paper Network)**  
- **Nodes**: Papers  
- **Edges**: Citation relationships (from references field)  
- 📌 **Insights:**  
  - Clustering coefficient over time to measure **network interconnectedness**.  
  - Average **path length & network diameter** to analyze **reachability**.  
  - Identifying **influential papers** using **PageRank**.  

### **2.2 Co-authorship Network (Author-Author Network)**  
- **Nodes**: Authors  
- **Edges**: Co-authorship relationships  
- 📌 **Insights:**  
  - **Network density per year** to analyze **collaboration trends**.  
  - Identifying **influential researchers** using **centrality measures** (degree, betweenness, closeness).  
  - Finding **author communities** working in similar fields.  

### **2.3 Venue Network (Conference-Journal Network)**  
- **Nodes**: Conferences/Journals  
- **Edges**: Citation relationships between venues  
- 📌 **Insights:**  
  - Analyzing **interdisciplinary collaborations**.  
  - Identifying **influential venues** using **centrality metrics**.  
  - Tracking **emerging research fields**.  

### **2.4 Temporal Evolution of the Citation Network**  
- 📌 **Key Observations:**  
  - Citation network **growth over time**.  
  - Identifying **high-impact papers** that suddenly gain many citations.  
  - Understanding how **new papers integrate into the research ecosystem**.  

---

## **🔍 3. Clustering & Community Detection**  
### **3.1 Author-Author Community Detection**  
- 🏆 **Task:** Group authors into communities using clustering algorithms.  
- ✅ **Approach:**  
  - Trained **three clustering algorithms** (Louvain, Walktrap, Spectral, etc.).  
  - Evaluated clusters using **clustering coefficient** to determine the best algorithm.  

### **3.2 Naming the Communities**  
- Extracted **keywords from paper titles and abstracts** using **KeyBERT**.  
- Aggregated **keywords per author-community** to define **research topics**.  
- Named each **community** based on dominant topics.  

### **3.3 Paper Clustering via Embeddings**  
- Embedded **abstracts and titles** using **BERT-based embeddings**.  
- Clustering performed using **K-Means, DBSCAN, or Agglomerative Clustering**.  
- Evaluated using **Silhouette Score & Davies-Bouldin Index**.  
- **Compared clusters with paper venues** using **Jaccard Similarity Index**.  

