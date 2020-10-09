---
layout: single
classes:
  - landing
---

## Wikitables Project

Abstract: We propose methods for extracting triples from Wikipedia’s HTML tables using a reference knowledge graph. Our methods
are based on a distant-supervision approach to find existing triples in the knowledge graph for pairs of entities on the same row of a
table, postulating the corresponding relation for pairs of entities from other rows in the corresponding columns, thus extracting novel
candidate triples. Binary classifiers are applied on these candidates to detect correct triples and thus increase the precision of output
triples. We extend this approach with a preliminary step where we first group and merge similar tables, thereafter applying extraction on
the larger merged tables. More specifically, we propose an observed schema for individual tables, which is used to group and merge
tables. We compare the precision and number of triples extracted with and without table merging, where we show that merging leads to
an increase in the number of triples that can be extracted at a similar precision. Ultimately, from the tables of English Wikipedia, we
extract 5.9 million novel and unique triples for Wikidata at an estimated precision of 0.718.

## Data

All data used for the experiments in this paper are made available for download at [https://zenodo.org/record/3483254](https://zenodo.org/record/3483254).

## Contact

- Jhomara Luzuriaga
- Aidan Hogan
