<!-- SPACY PROJECT: AUTO-GENERATED DOCS START (do not remove) -->

# 🪐 spaCy Project: la_dep_cltk_sm

Code required to train spaCy-compatible sm model for Latin. Latin pipeline with POS tagger, morphologizer,  lemmatizer, and dependency parser trained on all available Latin UD treebanks, i.e. Perseus, PROIEL, ITTB,  UDante, and LLCT (see below). This project is based on the spaCy tagger_parser_ud project template with the  following modifications: 1. uses Latin language-specific spaCy module; 2. combines multiple treebanks for  train, dev, and test sets; 3. uses a custom Latin senter sentence segmenter; and 4. normalizes u/v and i/j  in lemmas as a pretraining step (beta!).


## 📋 project.yml

The [`project.yml`](project.yml) defines the data assets required by the
project, as well as the available commands and workflows. For details, see the
[spaCy projects documentation](https://spacy.io/usage/projects).

### ⏯ Commands

The following commands are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run).
Commands are only re-run if their inputs have changed.

| Command | Description |
| --- | --- |
| `assets` | Download assets |
| `preprocess` | Convert the data to spaCy's format |
| `normalize` | U/V and I/J normalization before training, spec. for lemmatizer |
| `train` | Train tagger/pagger on Latin UD treebanks |
| `evaluate` | Evaluate on the test data and save the metrics |
| `package` | Package the trained model so it can be installed |
| `document` | Document dep_cltk_sm |
| `clean` | Remove intermediate files |

### ⏭ Workflows

The following workflows are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run)
and will run the specified commands in order. Commands are only re-run if their
inputs have changed.

| Workflow | Steps |
| --- | --- |
| `all` | `assets` &rarr; `preprocess` &rarr; `normalize` &rarr; `evaluate` &rarr; `package` &rarr; `document` &rarr; `clean` |

### 🗂 Assets

The following assets are defined by the project. They can
be fetched by running [`spacy project assets`](https://spacy.io/api/cli#project-assets)
in the project directory.

| File | Source | Description |
| --- | --- | --- |
| `assets/UD_Latin-Perseus` | Git |  |
| `assets/UD_Latin-PROIEL` | Git |  |
| `assets/UD_Latin-ITTB` | Git |  |
| `assets/UD_Latin-LLCT` | Git |  |
| `assets/UD_Latin-UDante` | Git |  |

<!-- SPACY PROJECT: AUTO-GENERATED DOCS END (do not remove) -->

## Current version

| Feature | Description |
| --- | --- |
| **Name** | `la_dep_cltk_sm` |
| **Version** | `0.2.0` |
| **spaCy** | `>=3.4.2,<3.5.0` |
| **Default Pipeline** | `senter`, `tok2vec`, `tagger`, `morphologizer`, `trainable_lemmatizer`, `parser` |
| **Components** | `senter`, `tok2vec`, `tagger`, `morphologizer`, `trainable_lemmatizer`, `parser` |
| **Vectors** | 0 keys, 0 unique vectors (0 dimensions) |
| **Sources** | UD_Latin-Perseus<br />UD_Latin-PROIEL<br />UD_Latin-ITTB<br />UD_Latin-LLCT<br />UD_Latin-UDante |
| **License** | `MIT` |
| **Author** | [Patrick J. Burns](https://diyclassics.github.io/) |

### Accuracy

| Type | Score |
| --- | --- |
| `SENTS_F` | 70.85 |
| `SENTS_P` | 77.20 |
| `SENTS_R` | 65.47 |
| `TAG_ACC` | 81.50 |
| `POS_ACC` | 96.01 |
| `MORPH_ACC` | 85.80 |
| `LEMMA_ACC` | 93.01 |
| `DEP_UAS` | 77.80 |
| `DEP_LAS` | 71.77 |
| `TOK2VEC_LOSS` | 9385275.09 |
| `TAGGER_LOSS` | 2402286.08 |
| `MORPHOLOGIZER_LOSS` | 2427212.87 |
| `TRAINABLE_LEMMATIZER_LOSS` | 961562.15 |
| `PARSER_LOSS` | 7532397.57 |

NB: For full details on tags etc., see the README.md in the model package.
