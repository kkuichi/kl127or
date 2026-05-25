# Metódy extrahovania informácií z medicínskych dát
Khrystyna Lobach  
Bakalárska práca

## Prehľad projektu

Tento repozitár obsahuje notebooky a výsledky použité pri bakalárskej práci zameranej na extrahovanie informácií z medicínskych textov pomocou metód Biomedical Named Entity Recognition (NER). Projekt zahŕňa predspracovanie dát, trénovanie modelov a vyhodnotenie výsledkov troch transformerových modelov: BioBERT, SciBERT a RoBERTa.

## Zdroj dát

Pre trénovanie a vyhodnotenie modelov bol použitý dataset zo zdrojového repozitára MedNER:

https://github.com/PARSA-MHMDI/MedNER

Dataset je dostupný aj prostredníctvom Hugging Face:

https://huggingface.co/datasets/parsa-mhmdi/Medical_NER

Spracovaný dataset (`ner_covid_final_data_v3`) nie je súčasťou repozitára z dôvodu veľkosti (~1.5 GB).

## Modely

Použité modely:

- BioBERT
- SciBERT
- RoBERTa

## Notebooky

| Notebook | Popis |
|-----------|--------|
| BioBERT_training.ipynb | Trénovanie a vyhodnotenie modelu BioBERT |
| SciBERT_training.ipynb | Trénovanie a vyhodnotenie modelu SciBERT |
| RoBERTa_training.ipynb | Trénovanie a vyhodnotenie modelu RoBERTa |

## Výsledky

Priečinok `results` obsahuje:

**results/figures/**  
Grafy train a validation loss pre jednotlivé modely.

**results/metrics/**  
Výsledné tabuľky obsahujúce Precision, Recall, F1-skóre a Support pre jednotlivé entity.

## Použité metriky hodnotenia

- Precision (Presnosť)
- Recall (Úplnosť)
- F1-skóre
- Support (Počet výskytov)

## Odporúčaná organizácia súborov

```text
notebooks/
├── BioBERT_training.ipynb
├── SciBERT_training.ipynb
└── RoBERTa_training.ipynb

results/
├── figures/
│   ├── loss_curve_biobert.png
│   ├── loss_curve_scibert.png
│   └── loss_curve_roberta.png
│
└── metrics/
    ├── biobert_entity_report_by_support.csv
    ├── scibert_entity_report_by_support.csv
    └── roberta_entity_report_by_support.csv

README.md
```
