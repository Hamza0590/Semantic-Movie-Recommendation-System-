# 🎬 Semantic Movie Recommendation System  
*A Deep-Learning–Powered Search Engine for Movies Using Sentence Transformers and ChromaDB*

---

## 🚀 Overview
This project is an intelligent **movie recommendation system** built with **Streamlit** that uses **semantic search** to find movies similar to a user’s description.  
Instead of relying on keyword matching, the system leverages **transformer-based embeddings** to understand the *meaning* of a user’s query — allowing natural-language inputs such as:

> “A futuristic space adventure with emotional depth like Interstellar.”

The system then retrieves thematically and contextually similar movies using **vector similarity search**.

---

## 🧠 Key Features
- 🗣 **Natural Language Search:** Find movies using full-sentence or descriptive queries.  
- 🧩 **Sentence Transformer Embeddings:** Uses `all-mpnet-base-v2` for high-quality semantic representations.  
- ⚡ **Vector Database:** Stores and queries embeddings via **ChromaDB** with persistent local storage.  
- 🧱 **Efficient Batching:** Embeddings generated in batches for scalability.  
- 🎛 **Streamlit UI:** Interactive, lightweight front-end for instant user feedback.  
- 🧮 **GPU Acceleration:** Automatically uses CUDA for faster embedding computation.  
- 💾 **Dataset Included:** A TMDB-based movie dataset is provided in the accompanying ZIP folder.  

---

## 🧰 Tech Stack
| Component | Technology Used |
|------------|-----------------|
| Frontend | [Streamlit](https://streamlit.io/) |
| Vector Store | [ChromaDB](https://www.trychroma.com/) |
| Embeddings | [Hugging Face Sentence Transformers – `all-mpnet-base-v2`](https://huggingface.co/sentence-transformers/all-mpnet-base-v2) |
| Data Processing | [Pandas](https://pandas.pydata.org/) |
| Language | Python 3.10+ |
| Hardware | CUDA GPU (Optional, for speed) |

---

## 📂 Dataset
A preprocessed **TMDB movie dataset** is included in the ZIP folder as:
It contains metadata such as:
- Movie title  
- Overview  
- Genres  
- Tagline  
- Release date  
- Rating  
- Runtime, etc.

---

## 🧩 System Architecture
1. **Data Preprocessing:**  
   Non-essential columns are removed and missing values handled.  

2. **Embedding Generation:**  
   For each movie, a combined text representation is constructed:
   embedding_text = (
       f"Title: {title}. "
       f"Genres: {genres}. "
       f"Tagline: {tagline}. "
       f"Overview: {overview}. "
       f"Release Year: {release_date[:4]}"
   )
   💻 Installation & Setup:
   1- Clone the Repository
   2- Unzip the Folder
   3- Run: pip install -r requirements.txt
   4- Run: streamlit run movie.py
   5- Open: http://localhost:8501


##🧑‍💻 Author
Muhammad Hamza
Student, FAST University Islamabad
5th Semester – BS Artificial Intelligence
