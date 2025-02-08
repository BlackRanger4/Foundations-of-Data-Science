# 📚 **AI Research Assistant – Phase 1 (Part 4)**  

## **Overview**  
This project develops an **AI-powered research assistant** that retrieves **relevant academic papers** based on user queries.  
Using a **vector-based search system**, the assistant efficiently finds **scholarly papers** from an indexed **database of research articles**.  

🚀 **Key Capabilities:**  
✔️ Find **relevant papers** by topic  
✔️ Retrieve **papers by author**  
✔️ Extract **key insights** from papers  
✔️ Generate **summaries of retrieved papers**  

---

## **🛠 Features**  
### ✅ **1. Query-Based Paper Retrieval**  
- Input: **A topic or keyword (e.g., "Neural Networks for NLP")**  
- Output: **Top-ranked research papers** matching the query  

### ✅ **2. Author-Based Search**  
- Input: **An author’s name (e.g., "S. Lawrence")**  
- Output: **Papers written by the specified author**  

### ✅ **3. Paper Summarization**  
- Extracts **key insights** from retrieved papers  
- Generates **concise summaries** using **NLP techniques**  

---

## **🔍 Usage Examples**  
### **Example 1: Query-Based Retrieval**  
#### **Input:**  
```python
query = "Neural networks for NLP"
retrieve_papers(query)
```
#### **Output:**  
```
================================================================================
Top 5 Results for Query: 'Neural networks for NLP'
================================================================================

Title: Are Deep Learning Approaches Suitable for Natural Language Processing  
Authors: ['S. Alshahrani', 'Epaminondas Kapetanios']  
Abstract: In recent years, Deep Learning (DL) techniques have gained much attention from AI and NLP research communities...
--------------------------------------------------------------------------------

Title: Natural language grammatical inference with recurrent neural networks  
Authors: ['S. Lawrence', 'C.L. Giles', 'Sandiway Fong']  
Abstract: This paper examines the inductive inference of a complex grammar with neural networks...
--------------------------------------------------------------------------------
```

---

### **Example 2: Author-Based Search**  
#### **Input:**  
```python
author_name = "S. Lawrence"
retrieve_by_author(author_name)
```
#### **Output:**  
```
================================================================================
Top 5 Results for Author: 'S. Lawrence'
================================================================================

Title: Clustering and identifying temporal trends in document databases  
Authors: ['Alexandrin Popescul', 'Gary W. Flake', 'S. Lawrence', 'Lyle H. Ungar', 'C.L. Giles']  
Abstract: We introduce a simple and efficient method for clustering and identifying temporal trends...
--------------------------------------------------------------------------------

Title: Face recognition: a convolutional neural-network approach  
Authors: ['S. Lawrence', 'C.L. Giles', 'Ah Chung Tsoi', 'Andrew D. Back']  
Abstract: We present a hybrid neural-network for human face recognition...
--------------------------------------------------------------------------------
```

---

### **Example 3: Paper Summarization**  
#### **Input:**  
```python
query = "GAN for Text"
generate_summary(query)
```
#### **Output:**  
```
================================================================================
Paper Summary:
================================================================================

- **Title:** StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks  
- **Summary:** Synthesizing photo-realistic images from text descriptions is a challenging problem. This paper proposes a Stacked GAN (StackGAN) architecture for improved text-to-image synthesis.
--------------------------------------------------------------------------------

- **Title:** Modeling documents with Generative Adversarial Networks  
- **Summary:** This paper describes using GANs to learn document representations with a denoising autoencoder as the discriminator.
--------------------------------------------------------------------------------
```


