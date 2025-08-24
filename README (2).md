# DS24 Kunskapskontroll 2 – RAG-baserad chattbot Det här repo-upplägget följer filstrukturen läraren efterfrågat: - `DS24_Kunskapskontroll2_RAG_Notebook.ipynb` – **huvudnotebooken** med teori + praktik.
- `docs/personalhandbok.txt` – källa för RAG-demon (byt/utöka med egna dokument).
- `README.md` – denna fil. ## Snabbstart (lokalt) 1. Skapa och aktivera en Python 3.10+ miljö.
2. Installera paket: ```bash pip install faiss-cpu sentence-transformers langchain langchain-community langchain-core langchain-text-splitters pypdf tiktoken openai python-dotenv ```
3. Starta Jupyter och öppna `DS24_Kunskapskontroll2_RAG_Notebook.ipynb`.
4. Kör cellerna uppifrån och ned. > **OpenAI (valfritt):** Om du vill använda en riktig LLM, skapa `.env` i roten med `OPENAI_API_KEY=...` och byt ut `simple_answer` i notebooken. ## Struktur ```
.
├── DS24_Kunskapskontroll2_RAG_Notebook.ipynb
├── README.md
└── docs/ └── personalhandbok.txt
``` ## Vad som ingår - En fungerande, enkel RAG-pipeline med **FAISS + sentence-transformers**.
- struktur för **teoretiska svar** (bias/varians, optimering, aktiveringar, CNN/RNN/Transformer, RAG-komponenter).
- Förslag på **utvärdering** och hur du lägger till källcitat. ## Tips till redovisning/rapport - Beskriv datakällor, chunking-strategi och val av embeddingmodell.
- Redogör för metrik (t.ex. precision@k) och begränsningar (hallucinationer, drift).
- Visa jämförelse mellan olika `k`, chunk-storlekar och embeddings. 