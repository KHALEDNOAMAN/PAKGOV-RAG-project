# PAKGOV RAG - Technical Guide

## RAG Pipeline
```
Documents --> OCR --> Chunking --> Embeddings --> Vector DB
                                                    |
User Query --> Hybrid Retrieval --> LLM Generation --> Cited Answer
                  |
            BM25 + Semantic
```

## Key Components
| Component | Technology | Purpose |
|-----------|-----------|---------|
| OCR | Tesseract/EasyOCR | Urdu + English text extraction |
| Embeddings | sentence-transformers | Bilingual embeddings |
| Vector Store | FAISS/ChromaDB | Similarity search |
| Retrieval | BM25 + Cosine | Hybrid search strategy |
| LLM | GPT-4/Llama | Answer generation |
| Grounding | Citation engine | Source attribution |

## Bilingual Support
| Feature | Urdu | English |
|---------|------|---------|
| OCR | ✅ | ✅ |
| Search | ✅ | ✅ |
| Generation | ✅ | ✅ |
| Citations | ✅ | ✅ |

## Evaluation Metrics
- Retrieval: Precision@K, Recall@K, MRR
- Generation: ROUGE, faithfulness, citation accuracy