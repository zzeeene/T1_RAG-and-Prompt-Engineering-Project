# NLP RAG & Prompt Engineering Project

## Description

This project is part of the **24-2 Natural Language Processing** course and focuses on building a question-answering system enhanced with Retrieval-Augmented Generation (RAG) and advanced prompt engineering techniques. The system is designed to improve the performance of a Large Language Model (LLM) provided by [Upstage (Solar)](https://www.upstage.ai).  

## Models
1. backbone LLM : **`Upstage solar-1-mini-chat`**
2. Document Loader : **`UpstageLayoutAnalysisLoader`**
3. Splitter : **`RecursiveCharacterTextSplitter`**
4. Embeddings : **`UpstageEmbeddings`**
   - solar-embedding-1-large-passage
   - solar-embedding-1-large-query
5. Preprocessing Tools:
   - **`BeautifulSoup`**
   - **`NLTK`**
   - **`TF-IDF Vectorizer`**
6. API : **`Wikipedia API`**
7. Prompt Engineering : **`langchain_core.prompts.prompt.PromptTemplate`**

## Datasets
1. EWHA Academic Policies
   
2. Domain-Specific Data:
 - Business : Collected from web crawling and Business Math resources.
 - Law : Data sourced from [U.S Government Information](congress.gov)
 - Philosophy : Sourced form *Philosophy 101*
 - Psychology : Sourced from *Cognitive Psychology and its Implications*
   
3. Test Data: MMLU-PRO



## Methodology

The methods used in this project include:

1. Data Collection
   - Implement a keyword extraction pipeline using **NLTK** and **TF-IDF** to enhance query generation.
      - Use stop words from **NLTK** to remove unneccessary words from the list
   - Gather domain-specific documents (Business, Psychology, Philosophy, Law) to improve coverage in underperforming areas.
   - Document retrieval via the **Wikipedia API**.
   - Attempt on web crawling to gather massive information for specific domain.
     
2. Embeddings
   - **RecursiveCharacterTextSplitter** for efficient text segmentation and preprocessing.
   - Use **UpstageEmbeddings** provided by Upstage APIs for document retrieval and domain classification.
   - Embed 3 major things:
      -  the split documents for each domain
      -  query
      -  related keywords lists for each domain
     
3. Preprocess Wikipedia Data
   - d

5. Prompt Engineering
   - Introduce Chain-of-Thought (CoT) reasoning.
   - Develop domain-specific prompts tailored to specific question types.






  
## Contributers

Minji Kim  [About](https://github.com/Janice0381)

Hyemin Boo  [About](https://github.com/hyeminboo)

Seoyoung Kim

Jiin Lee
