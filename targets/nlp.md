# Targets — NLP

Pick **2 primaries + 2 secondaries**. spaCy and sentence-transformers are the friendliest starting points.

| Repo | Why | First moves |
|---|---|---|
| **explosion/spaCy** ⭐ primary | Industrial NLP; historic GSoC participant; high code standards | pipeline/rule fixes, docs |
| **huggingface/sentence-transformers** ⭐ | Embeddings everywhere; approachable | docs, model-card fixes, small features |
| huggingface/datasets · tokenizers | Data layer of the HF stack | loader bugs, encoding edge cases |
| deepset-ai/haystack | RAG framework | retriever improvements, component fixes |
| argilla-io/argilla | Data annotation | frontend/backend fixes |
| nltk/nltk · RaRe-Technologies/gensim | Classics | bug fixes, docs |
| flairNLP/flair · stanfordnlp/stanza · hankcs/HanLP | Academic toolkits | bug fixes, model ports |
| open-compass/OpenCompass · EleutherAI/lm-eval-harness · stanford-crfm/helm | Benchmarks | new eval tasks |
| dottxt-ai/outlines · guidance-ai/guidance | Structured generation | grammar fixes, docs |
| google/sentencepiece · OpenNMT/OpenNMT-py | Tokenization / MT | edge-case fixes |
| xhluca/bm25s et al. | Retrieval utilities | small features, tests |

**Progression path:** docs → tokenizer/pipeline edge cases → eval task authorship (each new benchmark task is a self-contained, demonstrable contribution) → large PR (new pipeline component or eval suite).

**Note on datasets/tokenizers:** HF core repos move fast — pin to their current CONTRIBUTING flow (fix-forward on main, PR template required).
