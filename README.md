# NoNE Found Paper Dataset

This repository contains a **derived subset of the IDRISI-RE/LMR Dataset** used in the experiments reported in:

> [Jane Arleth dela Cruz, Iris Hendrickx, and Martha Lason]. “NoNE Found: Explaining the Output of Sequence-to-Sequence Models When No Named Entity Is Recognized” Explainable Artificial Intelligence. xAI 2024. Communications in Computer and Information Science, vol 2153. Springer, Cham., 2024.
> [[DOI or publication link]([https://doi.org/10.1016/j.ipm.2023.103340](https://doi.org/10.1007/978-3-031-63787-2_14))]

It is provided to support reproducibility of the accompanying article and is not an independently collected dataset.

## Source Dataset

The dataset is derived from the [IDRISI dataset](https://github.com/rsuwaileh/IDRISI/) introduced by:

> Suwaileh, R., Elsayed, T., & Imran, M. “IDRISI-RE: A generalizable dataset with benchmarks for location mention recognition on disaster tweets.”  Information Processing and Management Journal, 2023.

Please cite the original dataset and publication when using this resource.

## Dataset Description

For the accompanying study, a subset of events from the original dataset was selected. The data were also modified to use a simplified location annotation scheme.

Specifically:

* Only the events required for the study are included.
* The original fine-grained location types (e.g., `CITY`, `CTRY`, `STREET`) were mapped to a single generic `LOC` label.

This dataset therefore focuses on **location NER*, without distinguishing between specific types of locations.

## Annotation Scheme

| Label | Description                                          |
| ----- | ---------------------------------------------------- |
| `LOC` | A span referring to a geographical location or place |
| `O`   | A token that is not part of a location mention       |

BIO-style format is used, location mentions are represented using `B-LOC` and `I-LOC`.

## Reproducibility

The dataset was created by:

1. Obtaining the original IDRISI dataset.
2. Selecting the events used in the study.
3. Mapping the original location-type labels to `LOC`.
4. Applying any additional preprocessing required by the study (adding the COIN token)

Any scripts used for these transformations are included in this repository where applicable.

## Citation

If you use this dataset, please cite both the accompanying article and the original IDRISI dataset.

### This dataset

```bibtex
@article{delaCruz2024-NoNEFound,
author="dela Cruz, Jane Arleth
and Hendrickx, Iris
and Larson, Martha",
title="NoNE Found: Explaining the Output of Sequence-to-Sequence Models When No Named Entity Is Recognized",
booktitle="Explainable Artificial Intelligence",
year="2024",
publisher="Springer Nature Switzerland",
address="Cham",
pages="265--284",
}
```

### Original dataset

```bibtex
@article{rsuwaileh2023idrisire,
    title = {{IDRISI}-{RE}: A generalizable dataset with benchmarks for location mention recognition on disaster tweets},
    author = {Reem Suwaileh and Tamer Elsayed and Muhammad Imran},
    journal = {Information Processing & Management},
    volume = {60},
    number = {3},
    pages = {103340},
    year = {2023},
    issn = {0306-4573},
    doi = {https://doi.org/10.1016/j.ipm.2023.103340},
    url = {https://www.sciencedirect.com/science/article/pii/S0306457323000778},
    publisher={Elsevier}
  }
```

## License and Data Provenance

This dataset is derived from the IDRISI dataset, which is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

Users should also consult the [original repository](https://github.com/rsuwaileh/IDRISI/) for information about data provenance, redistribution, and any restrictions applying to the underlying social-media data.

## Acknowledgements

We thank the authors of the original IDRISI dataset for making their resource publicly available. Our paper is part of the project `Indeep: Interpreting Deep Learning Models for Text and Sound' with project number NWA.1292.19.399, which is partly financed by the Dutch Research Council (NWO).
