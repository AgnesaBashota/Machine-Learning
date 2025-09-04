# KK2 – Kreditkortsbedrägerier (Agnesa Bashota)

Minimal kodnotebook med **auto-install** och **autosave** av resultat.

## Struktur
- `kk2_kreditbedrageri_.ipynb` – kör allt.
- `data/` – lägg `creditcard.csv` här (annars används syntetisk data).
- `images/` – sparar figurer (ROC, Confusion Matrix, klassfördelning).
- `logs/` – sparar `metrics.csv`, `classification_report_*.txt`, `meta.json`, `run_info.json`.
- `requirements.txt` – paketen om du vill installera manuellt.

## Körning
1. (Valfritt) `pip install -r requirements.txt` – eller kör notebooken direkt (första cellen installerar automatiskt).
2. Lägg `data/creditcard.csv` i `data/` om du vill köra på Kaggle-datat.
3. Kör cellerna uppifrån och ner. Resultat hamnar i `images/` och `logs/`.
