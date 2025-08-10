# Enterprise RAG Prototype: LangChain + FAISS

This repository contains a working **Retrieval-Augmented Generation (RAG)** prototype using:

- **LangChain** for orchestrating the RAG workflow  
- **FAISS** to store and search embeddings  
- **Hugging Face** for generating local embeddings  
- **OpenAI GPT** as the language model for query generation

---

## Repository Contents
```
├── enterprise-rag-langchain-faiss.ipynb ← Fully functional Colab notebook
├── data/
│ └── sample_texts/ ← 5 finance-related .txt documents
├── faiss_index/ ← Saved FAISS index files (not committed)
├── README.md ← This file
└── .gitignore
```

---

##  Quickstart (Colab)

1. Open `rag_build_index_query.ipynb` in Colab.  
2. Follow along with the notebook’s **Text** and **Code** cells that walk through:
   1. **Set up Colab** → install libs, mount Drive  
   2. **Configure API key** → securely load your OpenAI key  
   3. **Load documents** → import your sample `.txt` files  
   4. **Chunking** → split long text into smaller chunks  
   5. **Embeddings** → embed chunks using Hugging Face locally  
   6. **Vector Index** → build and save a FAISS index  
   7. **Retriever + LLM** → connect to GPT and run queries  

3. Try your own finance or enterprise-related questions using the `ask(...)` helper.

---

##  Project Philosophy & Ideal For

This prototype is designed for **blog readers and enterprise practitioners** who want a quick but clear demonstration of RAG without production complexity.

It is:
- Self-contained in a single Colab notebook  
- Fast, with Hugging Face embeddings and small datasets  
- Adaptable and easy to retrace for your own document collections  

---

##  Tips for Extension (Optional)

If you'd like to expand the prototype:
- Swap Hugging Face embeddings for `OpenAIEmbeddings` (requires billing setup)  
- Scale up using large document collections or parallelize indexing  
- Add evaluation metrics (e.g., retrieval precision, latency analysis)  
- Swap FAISS for managed vector DBs like Pinecone or Weaviate

---

##  License

This project is released under the **MIT License**. Feel free to use it as a foundation for exploration or teaching.

---

##  Acknowledgements

- LangChain team for seamless RAG workflows  
- Hugging Face for accessible embedding models  
- OpenAI for powerful GPT models used in QA chains

