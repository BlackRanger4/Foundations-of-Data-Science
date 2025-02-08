### 📚 AI Research Paper Scraper

## **Overview**
This project aims to develop an **AI assistant** that helps users find relevant **scholarly papers**. Since our given dataset (DBLP) only contains papers up to **2017**, we enhance the assistant’s capabilities by **scraping recent research papers** from **Semantic Scholar**.

This phase (**Phase 0**) focuses on **web scraping** research papers in five major AI topics:

- **Foundation Models**
- **Generative Models**
- **Large Language Models (LLM)**
- **Vision-Language Models (VLM)**
- **Diffusion Models**

The collected data will later be used for **training and evaluating the AI assistant**.

---

## **📥 Data Collection Methodology**
To efficiently retrieve AI research papers, we designed an **automated scraping pipeline** using the **Semantic Scholar API**. The process involves:

1. **Querying Papers**: Searching for each topic and retrieving **relevant papers published after 2017**.
2. **Sorting & Filtering**: Extracting key fields: **title, abstract, authors, and citation count**.
3. **Pagination Handling**: Fetching additional papers beyond API limits.
4. **Rate Limiting & Error Handling**: Implementing a retry mechanism to handle request limits and network failures.
5. **Year Segmentation**: Collecting papers from three time periods: **2017-2020, 2021-2023, and 2024-2025**.

**Goal**: **2,000 papers per topic**, stored in **JSON format**.

---

## **📂 Data Storage Format**
The extracted data is saved in a structured **JSON format** for easy processing.  
Each topic has a separate JSON file, formatted as:

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

This structure allows easy merging and querying.

---

## **🛠 Data Processing**
After collecting research papers, the following steps ensure data consistency:

- **Merging Paper Lists**: Combining papers across different year ranges.
- **Handling Missing Data**: Assigning placeholders for missing abstracts/authors.
- **Removing Duplicates**: Ensuring each paper appears only once.

A dedicated script **loads, cleans, and merges** the datasets for further analysis.

---

## **✅ Data Verification**
To ensure **high-quality data**, we implement a **randomized paper selection check**:

- **Valid abstracts and author names**.
- **Correct citation counts**.
- **No empty or incomplete records**.

---

## **🚧 Challenges & Considerations**
During this phase, we faced several challenges:

- **API Rate Limits**: Semantic Scholar enforces request restrictions.
- **Inconsistent Metadata**: Some papers lack abstracts/authors.
- **Large-Scale Data Handling**: Efficient file management was needed.
- **Irrelevant Results**: Some retrieved papers were off-topic.

To address these, we optimized **rate handling, filtering, and data cleaning**.

---

## **🎯 Conclusion**
This phase successfully built a **structured web scraping pipeline** to collect recent AI research papers. The data is now ready for **further processing** and will be used to enhance the **AI research assistant**.

### **Next Steps**
- Training an AI model using the collected data.
- Implementing a **vector-based search** for efficient paper retrieval.
- Enhancing filtering and ranking algorithms for better recommendations.

