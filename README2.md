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
results = search_papers(query, top_k=5)

query = "GAN for Text"
results = search_papers(query, top_k=5)
```
#### **Output:**  
```

================================================================================
Top 5 Results for Query: 'Neural networks for NLP'
================================================================================

**Title:** Are Deep Learning Approaches Suitable for Natural Language Processing

**Abstract:** In recent years, Deep Learning (DL) techniques have gained much at-tention from Artificial Intelligence (AI) and Natural Language Processing (NLP) research communities because these approaches can often learn features from data without the need for human design or engineering interventions. In addition, DL approaches have achieved some remarkable results. In this paper, we have surveyed major recent contributions that use DL techniques for NLP tasks. All these reviewed topics have been limited t...

**Authors:** ['S. Alshahrani', 'Epaminondas Kapetanios']

--------------------------------------------------------------------------------

**Title:** Natural language grammatical inference with recurrent neural networks

**Abstract:** This paper examines the inductive inference of a complex grammar with neural networks and specifically, the task considered is that of training a network to classify natural language sentences as grammatical or ungrammatical, thereby exhibiting the same kind of discriminatory power provided by the Principles and Parameters linguistic framework, or Government-and-Binding theory. Neural networks are trained, without the division into learned vs. innate components assumed by Chomsky (1956), in an a...

**Authors:** ['S. Lawrence', 'C.L. Giles', 'Sandiway Fong']

--------------------------------------------------------------------------------

**Title:** Modelling the Combination of Generic and Target Domain Embeddings in a Convolutional Neural Network for Sentence Classification

**Abstract:** This is the final version of the article. It first appeared from the Association for Computational Linguistics via http://www.aclweb.org/anthology/W/W16/

**Authors:** ['Nut Limsopatham', 'Nigel Collier']

--------------------------------------------------------------------------------

**Title:** Neural Networks Leverage Corpus-wide Information for Part-of-speech Tagging

**Abstract:** We propose a neural network approach to benefit from the non-linearity of corpuswide statistics for part-of-speech (POS) tagging. We investigated several types of corpus-wide information for the words, such as word embeddings and POS tag distributions. Since these statistics are encoded as dense continuous features, it is not trivial to combine these features comparing with sparse discrete features. Our tagger is designed as a combination of a linear model for discrete features and a feed-forwar...

**Authors:** ['Yuta Tsuboi']

--------------------------------------------------------------------------------

**Title:** Fast Semantic Extraction Using a Novel Neural Network Architecture

**Abstract:** A system and method for semantic extraction using a neural network architecture includes indexing each word in an input sentence into a dictionary and using these indices to map each word to a d-dimensional vector (the features of which are learned). Together with this, position information for a word of interest (the word to labeled) and a verb of interest (the verb that the semantic role is being predicted for) with respect to a given word are also used. These positions are integrated by emplo...

**Authors:** ['Ronan Collobert', 'Jason Weston']

--------------------------------------------------------------------------------


================================================================================
Top 5 Results for Query: 'GAN for Text'
================================================================================

**Title:** StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks

**Abstract:** Synthesizing photo-realistic images from text descriptions is a challenging problem in computer vision and has many practical applications. Samples generated by existing text-to-image approaches can roughly reflect the meaning of the given descriptions, but they fail to contain necessary details and vivid object parts. In this paper, we propose stacked Generative Adversarial Networks (StackGAN) to generate photo-realistic images conditioned on text descriptions. The Stage-I GAN sketches the prim...

**Authors:** ['Han Zhang', 'Tao Xu', 'Hongsheng Li', 'Shaoting Zhang', 'Xiaolei Huang', 'Xiaogang Wang', 'Dimitris N. Metaxas']

--------------------------------------------------------------------------------

**Title:** Modeling documents with Generative Adversarial Networks

**Abstract:** This paper describes a method for using Generative Adversarial Networks to learn distributed representations of natural language documents. We propose a model that is based on the recently proposed Energy-Based GAN, but instead uses a Denoising Autoencoder as the discriminator network. Document representations are extracted from the hidden layer of the discriminator and evaluated both quantitatively and qualitatively.

**Authors:** ['John Glover']

--------------------------------------------------------------------------------

**Title:** NIPS 2016 Tutorial: Generative Adversarial Networks

**Abstract:** This report summarizes the tutorial presented by the author at NIPS 2016 on generative adversarial networks (GANs). The tutorial describes: (1) Why generative modeling is a topic worth studying, (2) how generative models work, and how GANs compare to other generative models, (3) the details of how GANs work, (4) research frontiers in GANs, and (5) state-of-the-art image models that combine GANs with other methods. Finally, the tutorial contains three exercises for readers to complete, and the so...

**Authors:** ['Ian J. Goodfellow']

--------------------------------------------------------------------------------

**Title:** Generative Adversarial Text to Image Synthesis

**Abstract:** Automatic synthesis of realistic images from text would be interesting and useful, but current AI systems are still far from this goal. However, in recent years generic and powerful recurrent neural network architectures have been developed to learn discriminative text feature representations. Meanwhile, deep convolutional generative adversarial networks (GANs) have begun to generate highly compelling images of specific categories, such as faces, album covers, and room interiors. In this work, w...

**Authors:** ['Scott E. Reed', 'Zeynep Akata', 'Xinchen Yan', 'Lajanugen Logeswaran', 'Bernt Schiele', 'Honglak Lee']

--------------------------------------------------------------------------------

**Title:** Inverting The Generator Of A Generative Adversarial Network

**Abstract:** Generative adversarial networks (GANs) learn to synthesise new samples from a high-dimensional distribution by passing samples drawn from a latent space through a generative network. When the high-dimensional distribution describes images of a particular data set, the network should learn to generate visually similar image samples for latent variables that are close to each other in the latent space. For tasks such as image retrieval and image classification, it may be useful to exploit the arra...

**Authors:** ['Antonia Creswell', 'Anil A. Bharath']

--------------------------------------------------------------------------------

```

---

### **Example 2: Author-Based Search**  
#### **Input:**  
```python
author_results = search_papers(author="'S. Lawrence", top_k=5)
```
#### **Output:**  
```
================================================================================
Top 5 Results for Author: 'S. Lawrence'
================================================================================

**Title:** Clustering and identifying temporal trends in document databases

**Abstract:** We introduce a simple and efficient method for clustering and identifying temporal trends in hyper-linked document databases. Our method can scale to large datasets because it exploits the underlying regularity often found in hyper-linked document databases. Because of this scalability, we can use our method to study the temporal trends of individual clusters in a statistically meaningful manner. As an example of our approach, we give a summary of the temporal trends found in a scientific litera...

**Authors:** ['Alexandrin Popescul', 'Gary W. Flake', 'S. Lawrence', 'Lyle H. Ungar', 'C.L. Giles']

--------------------------------------------------------------------------------

**Title:** Persistence of Web references in scientific research

**Abstract:** The lack of persistence of Web references has called into question the increasingly common practice of citing URLs in scientific papers. It is argued that although few critical resources have been lost to date, new strategies to manage Internet resources and improved citation practices are necessary to minimize the future loss of information.

**Authors:** ['S. Lawrence', 'David M. Pennock', 'Gary W. Flake', 'Robert Krovetz', 'Frans Coetzee', 'Eric Glover', 'Finn Aarup Nielsen', 'A. Kruger', 'C.L. Giles']

--------------------------------------------------------------------------------

**Title:** Natural language grammatical inference with recurrent neural networks

**Abstract:** This paper examines the inductive inference of a complex grammar with neural networks and specifically, the task considered is that of training a network to classify natural language sentences as grammatical or ungrammatical, thereby exhibiting the same kind of discriminatory power provided by the Principles and Parameters linguistic framework, or Government-and-Binding theory. Neural networks are trained, without the division into learned vs. innate components assumed by Chomsky (1956), in an a...

**Authors:** ['S. Lawrence', 'C.L. Giles', 'Sandiway Fong']

--------------------------------------------------------------------------------

**Title:** Time-frequency scaling property of Discrete Fourier Transform (DFT)

**Abstract:** This paper presents the analogue of the time or frequency scaling theorem of continuous time/frequency Fourier Transform (FT) to the realm of Discrete Fourier Transform (DFT). The scaling property applies to scaling by integers which are relatively prime to the length of the DFT. The time reversal property of DFT is identified as a special case of this theorem.

**Authors:** ['Sumit A. Talwalkar', 'S. Lawrence Marple']

--------------------------------------------------------------------------------

**Title:** Face recognition: a convolutional neural-network approach

**Abstract:** We present a hybrid neural-network for human face recognition which compares favourably with other methods. The system combines local image sampling, a self-organizing map (SOM) neural network, and a convolutional neural network. The SOM provides a quantization of the image samples into a topological space where inputs that are nearby in the original space are also nearby in the output space, thereby providing dimensionality reduction and invariance to minor changes in the image sample, and the ...

**Authors:** ['S. Lawrence', 'C.L. Giles', 'Ah Chung Tsoi', 'Andrew D. Back']

--------------------------------------------------------------------------------

```

---

### **Example 3: Paper Summarization**  
#### **Input:**  
```python
for i, row in results.iterrows():

      title = row['title']
      abstract = row['abstract']
      authors = row['authors']

      summary = summarize_paper_local(title, abstract, authors)
      print("**Paper Summary:**\n", summary)
      print("-" * 80 + "\n")

results is:
================================================================================
Top 5 Results for Query: 'Neural networks for NLP'
================================================================================

**Title:** Are Deep Learning Approaches Suitable for Natural Language Processing

**Abstract:** In recent years, Deep Learning (DL) techniques have gained much at-tention from Artificial Intelligence (AI) and Natural Language Processing (NLP) research communities because these approaches can often learn features from data without the need for human design or engineering interventions. In addition, DL approaches have achieved some remarkable results. In this paper, we have surveyed major recent contributions that use DL techniques for NLP tasks. All these reviewed topics have been limited t...

**Authors:** ['S. Alshahrani', 'Epaminondas Kapetanios']

--------------------------------------------------------------------------------

**Title:** Natural language grammatical inference with recurrent neural networks

**Abstract:** This paper examines the inductive inference of a complex grammar with neural networks and specifically, the task considered is that of training a network to classify natural language sentences as grammatical or ungrammatical, thereby exhibiting the same kind of discriminatory power provided by the Principles and Parameters linguistic framework, or Government-and-Binding theory. Neural networks are trained, without the division into learned vs. innate components assumed by Chomsky (1956), in an a...

**Authors:** ['S. Lawrence', 'C.L. Giles', 'Sandiway Fong']

--------------------------------------------------------------------------------

**Title:** Modelling the Combination of Generic and Target Domain Embeddings in a Convolutional Neural Network for Sentence Classification

**Abstract:** This is the final version of the article. It first appeared from the Association for Computational Linguistics via http://www.aclweb.org/anthology/W/W16/

**Authors:** ['Nut Limsopatham', 'Nigel Collier']

--------------------------------------------------------------------------------

**Title:** Neural Networks Leverage Corpus-wide Information for Part-of-speech Tagging

**Abstract:** We propose a neural network approach to benefit from the non-linearity of corpuswide statistics for part-of-speech (POS) tagging. We investigated several types of corpus-wide information for the words, such as word embeddings and POS tag distributions. Since these statistics are encoded as dense continuous features, it is not trivial to combine these features comparing with sparse discrete features. Our tagger is designed as a combination of a linear model for discrete features and a feed-forwar...

**Authors:** ['Yuta Tsuboi']

--------------------------------------------------------------------------------

**Title:** Fast Semantic Extraction Using a Novel Neural Network Architecture

**Abstract:** A system and method for semantic extraction using a neural network architecture includes indexing each word in an input sentence into a dictionary and using these indices to map each word to a d-dimensional vector (the features of which are learned). Together with this, position information for a word of interest (the word to labeled) and a verb of interest (the verb that the semantic role is being predicted for) with respect to a given word are also used. These positions are integrated by emplo...

**Authors:** ['Ronan Collobert', 'Jason Weston']

--------------------------------------------------------------------------------


================================================================================
Top 5 Results for Query: 'GAN for Text'
================================================================================

**Title:** StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks

**Abstract:** Synthesizing photo-realistic images from text descriptions is a challenging problem in computer vision and has many practical applications. Samples generated by existing text-to-image approaches can roughly reflect the meaning of the given descriptions, but they fail to contain necessary details and vivid object parts. In this paper, we propose stacked Generative Adversarial Networks (StackGAN) to generate photo-realistic images conditioned on text descriptions. The Stage-I GAN sketches the prim...

**Authors:** ['Han Zhang', 'Tao Xu', 'Hongsheng Li', 'Shaoting Zhang', 'Xiaolei Huang', 'Xiaogang Wang', 'Dimitris N. Metaxas']

--------------------------------------------------------------------------------

**Title:** Modeling documents with Generative Adversarial Networks

**Abstract:** This paper describes a method for using Generative Adversarial Networks to learn distributed representations of natural language documents. We propose a model that is based on the recently proposed Energy-Based GAN, but instead uses a Denoising Autoencoder as the discriminator network. Document representations are extracted from the hidden layer of the discriminator and evaluated both quantitatively and qualitatively.

**Authors:** ['John Glover']

--------------------------------------------------------------------------------

**Title:** NIPS 2016 Tutorial: Generative Adversarial Networks

**Abstract:** This report summarizes the tutorial presented by the author at NIPS 2016 on generative adversarial networks (GANs). The tutorial describes: (1) Why generative modeling is a topic worth studying, (2) how generative models work, and how GANs compare to other generative models, (3) the details of how GANs work, (4) research frontiers in GANs, and (5) state-of-the-art image models that combine GANs with other methods. Finally, the tutorial contains three exercises for readers to complete, and the so...

**Authors:** ['Ian J. Goodfellow']

--------------------------------------------------------------------------------

**Title:** Generative Adversarial Text to Image Synthesis

**Abstract:** Automatic synthesis of realistic images from text would be interesting and useful, but current AI systems are still far from this goal. However, in recent years generic and powerful recurrent neural network architectures have been developed to learn discriminative text feature representations. Meanwhile, deep convolutional generative adversarial networks (GANs) have begun to generate highly compelling images of specific categories, such as faces, album covers, and room interiors. In this work, w...

**Authors:** ['Scott E. Reed', 'Zeynep Akata', 'Xinchen Yan', 'Lajanugen Logeswaran', 'Bernt Schiele', 'Honglak Lee']

--------------------------------------------------------------------------------

**Title:** Inverting The Generator Of A Generative Adversarial Network

**Abstract:** Generative adversarial networks (GANs) learn to synthesise new samples from a high-dimensional distribution by passing samples drawn from a latent space through a generative network. When the high-dimensional distribution describes images of a particular data set, the network should learn to generate visually similar image samples for latent variables that are close to each other in the latent space. For tasks such as image retrieval and image classification, it may be useful to exploit the arra...

**Authors:** ['Antonia Creswell', 'Anil A. Bharath']

--------------------------------------------------------------------------------


```
#### **Output:**  
```
Device set to use cuda:0
**Paper Summary:**
 Synthesizing photo-realistic images from text descriptions is a challenging problem in computer vision and has many practical applications. We propose stacked Generative Adversarial Networks (StackGAN) to generate photos conditioned on text descriptions. The Stage-I GAN sketches the primitive shape and basic colors of the object based on the given text description.
--------------------------------------------------------------------------------

Device set to use cuda:0
**Paper Summary:**
 This paper describes a method for using Generative Adversarial Networks to learn distributed representations of natural language documents. We propose a model that is based on the recently proposed Energy-Based GAN, but instead uses a Denoising Autoencoder. Document representations are extracted from the hidden layer of the discriminator and evaluated both quantitatively and qualitatively.
--------------------------------------------------------------------------------

Device set to use cuda:0
**Paper Summary:**
 This report summarizes the tutorial presented by the author at NIPS 2016 on generative adversarial networks (GANs) The tutorial describes: (1) Why generative modeling is a topic worth studying, (2) how generative models work, and (3) how GANs compare to other models. The tutorial contains three exercises for readers to complete, and the solutions.
--------------------------------------------------------------------------------

Device set to use cuda:0
**Paper Summary:**
 Generative Adversarial Text to Image Synthesis (GAN) is a new type of AI system. It uses deep convolutional generative adversarial networks (GANs) to generate images of specific categories. The model can generate plausible images of birds and flowers from detailed text descriptions.
--------------------------------------------------------------------------------

Device set to use cuda:0
**Paper Summary:**
 This paper introduces techniques for projecting image samples into the latent space using any pre-trained GAN, provided that the computational graph is available. We evaluate these techniques on both MNIST digits and Omniglot handwritten characters. In the case ofMNIST digits, we show that projections into the. latent space maintain information about the style and the identity of the digit. We show that even characters from alphabets that have not been seen during training may be projected well into. the latent. space.
--------------------------------------------------------------------------------

```


