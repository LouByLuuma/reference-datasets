# reference-datasets

Public reference datasets ingested by the Lou platform. All content is **official
open data relayed verbatim** — no PHI, no proprietary content.

## `ansm/` — ANSM Thésaurus des interactions médicamenteuses

Structured (NDJSON) extraction of the French ANSM drug-interaction thesaurus,
published by the ANSM as PDF only.

- `ansm-thesaurus-2023-09.ndjson` — edition **September 2023** (`source_revision = 2023-09`).
  3352 interactions. One JSON object per line:
  `{substanceA, substanceB, level, conduite?, mechanism?}` where `level ∈
  {contre_indication, association_deconseillee, precaution_emploi, a_prendre_en_compte}`.

Source: <https://ansm.sante.fr/documents/reference/thesaurus-des-interactions-medicamenteuses-1>
Extraction process: `docs/ops/ansm-thesaurus-refresh.md` in the Lou platform repo.
Consumed via `ANSM_THESAURUS_DATASET_URL` (LOU-1417 / LOU-1493).
