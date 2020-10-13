---
layout: single
classes:
  - landing
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/figure1.png
---

# Wikitables Project

Abstract: We propose methods for extracting triples from Wikipedia’s HTML tables using a reference knowledge graph. Our methods
are based on a distant-supervision approach to find existing triples in the knowledge graph for pairs of entities on the same row of a
table, postulating the corresponding relation for pairs of entities from other rows in the corresponding columns, thus extracting novel
candidate triples. Binary classifiers are applied on these candidates to detect correct triples and thus increase the precision of output
triples. We extend this approach with a preliminary step where we first group and merge similar tables, thereafter applying extraction on
the larger merged tables. More specifically, we propose an observed schema for individual tables, which is used to group and merge
tables. We compare the precision and number of triples extracted with and without table merging, where we show that merging leads to
an increase in the number of triples that can be extracted at a similar precision. Ultimately, from the tables of English Wikipedia, we
extract 5.9 million novel and unique triples for Wikidata at an estimated precision of 0.718.

# Data

Data used for the experiments in this paper are made available for download at [https://zenodo.org/record/3483254](https://zenodo.org/record/3483254), including:

* `wikipedia_html.tar`: the Wikipedia HTML corpus; 
* `tablesByCluster.tar.gz`: the corpus of (grouped) Wikitables; 
* and the final candidate triples extracted from:
  * `triplesProbalModelB.csv.gz` individual tables with extended features (I*/B), 
  * `triplesProbalModelC.csv.gz` individual tables with extended and merged features (I+/C), and 
  * `triplesProbalModelD.csv.gz` merged tables with extended and merged features (M+/D). 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3483254.svg)](https://doi.org/10.5281/zenodo.3483254)

Further data are provided in this [Github repository](https://github.com/wikitables/wikitables.github.io) including:

* `feature_names.tsv`: A desription of each feature, the ID used in these data, and the ID used in the paper (for clarity we reordered some of the feature IDs in the paper).
* `wikidata_prop_en_labels.tsv`: English labels for Wikidata properties used (note that `Pn-1` indicates the inverse of `Pn`).
* `wikidata_prop_stats.tsv`: Statistics for Wikidata properties used to build features.
* `wikidata_prop_compat_stats.tsv`: Statistics for pairs of Wikidata properties used to compute compatibility scores.
* `train_tables_500.tsv`: A set of 500 labelled candidate triples extracted from individual tables (I) used for training.
* `test_tables_100.tsv`: A set of 100 labelled candidate triples extracted from individual tables (I) used for testing.
* `train_groups_500.tsv`: A set of 500 labelled candidate triples extracted from grouped tables (M) used for training.
* `test_groups_100.tsv`: A set of 100 labelled candidate triples extracted from grouped tables (M) used for testing.
* `validation_results.xlsx`: The results of the validation of 200 output candidate triples from (I*/B), (I+/C) and (M+/D).

# Code

The code for the project is available from the [following repository](https://github.com/wikitables/web-of-data-tables/tree/master/source).

# Contact

- Jhomara Luzuriaga
- Aidan Hogan
