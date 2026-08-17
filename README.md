# Beyond Benchmark Accuracy: Hierarchical Transfer Learning and ROI Standardization for Bone Age Assessment in Thai Children

[![Preprint](https://img.shields.io/badge/status-preprint-blue)](#manuscript-status)
[![IEEE Submission](https://img.shields.io/badge/IEEE-submitted-orange)](#manuscript-status)
[![Year](https://img.shields.io/badge/year-2026-lightgrey)](#citation)

This repository hosts the **author preprint** of:

> **Beyond Benchmark Accuracy: Hierarchical Transfer Learning and ROI Standardization for Bone Age Assessment in Thai Children**

The manuscript presents a population-specific artificial intelligence framework for automated bone age assessment (BAA) from pediatric hand and wrist radiographs, with a focus on Thai children.

---

## Manuscript

📄 **[Download the preprint PDF](./BAA_preprint_v1.pdf)**

### Manuscript status

**Preprint — August 2026**

This manuscript has been submitted to **IEEE for possible publication** and is currently under editorial review.

It has **not yet been accepted or published by IEEE**.

The version hosted in this repository is an author-prepared preprint and should not be considered the final peer-reviewed or publisher-formatted version.

The manuscript contains the IEEE preprint notice:

> This work has been submitted to the IEEE for possible publication. Copyright may be transferred without notice, after which this version may no longer be accessible.

If the manuscript is accepted and formally published, this repository will be updated with the bibliographic information and DOI of the final publication.

---

## Authors

- **Pitchaya Wiratchotisatian**  
  Department of Statistics, Faculty of Science, Khon Kaen University, Thailand

- **Khwankaow Tangprasert**  
  Department of Computer Engineering, Faculty of Engineering, Khon Kaen University, Thailand

- **Sarun Paisarnsrisomsuk**  
  Department of Computer Engineering, Faculty of Engineering, Khon Kaen University, Thailand

- **Panawit Hanpinitsak** *  
  Department of Computer Engineering, Faculty of Engineering, Khon Kaen University, Thailand

- **Wichuda Chaisiwamongkol**  
  Department of Statistics, Faculty of Science, Khon Kaen University, Thailand

- **Ratikorn Chaisiwamongkol**  
  Department of Pediatrics, Faculty of Medicine, Khon Kaen University, Thailand

- **Nipaporn Tewattanarat**  
  Department of Radiology, Faculty of Medicine, Khon Kaen University, Thailand

- **Chanakarn Poonpol**  
  Department of Statistics, Faculty of Science, Khon Kaen University, Thailand

- **Chatparin Pansukrada**  
  Information Technology Workgroups, Faculty of Science, Khon Kaen University, Thailand

- **Wilairat Thaowandee**  
  Department of Pediatrics, Faculty of Medicine, Khon Kaen University, Thailand

\* Corresponding author: **Panawit Hanpinitsak**  
Email: panaha@kku.ac.th

---

## Study Overview

Automated bone age assessment models trained on large public datasets may experience reduced performance when applied to populations that differ from the original training data.

This work investigates a deployment-oriented BAA framework designed for Thai pediatric radiographs by combining:

1. **ROI standardization**
   - Contrast enhancement using CLAHE
   - Automatic hand detection
   - Hand segmentation
   - Standardized model input preparation

2. **Hierarchical transfer learning**
   - Initial learning from large public bone-age datasets
   - RSNA Pediatric Bone Age Challenge
   - Digital Hand Atlas (DHA)
   - Subsequent adaptation to a Thai clinical cohort

3. **Population-specific evaluation**
   - Public-data-only training
   - Pooled multi-dataset training
   - Hierarchical population-specific adaptation

4. **Supervision-standard evaluation**
   - Greulich–Pyle (GP)
   - Tanner–Whitehouse (TW)
   - Hybrid TW+GP supervision

The final hierarchically adapted model achieved a mean absolute error of **4.64 months** on the held-out Thai test cohort.

---

## Associated Open-Source Code

The implementations described in the manuscript are maintained in separate repositories.

### Image preprocessing and ROI standardization

**HandXRay-Preprocessing**

https://github.com/Khao0/HandXRay-Preprocessing

This repository contains the preprocessing framework used to standardize hand and wrist radiographs before bone-age prediction, including hand detection and segmentation.

It also provides links to processed public-dataset resources described in the manuscript.

### Bone age prediction and hierarchical adaptation

**HiDA-BAA**

https://github.com/Khao0/HiDA-BAA

This repository contains the bone-age prediction and target-domain adaptation framework associated with the study.

The model uses an EfficientNetB7-based regression architecture and a hierarchical adaptation strategy in which representations learned from public datasets are subsequently adapted to target-domain data.

---

## Repository Purpose

This repository serves as the **public manuscript record** for the study.

Research software is maintained separately so that the manuscript and software can be versioned independently:

| Resource | Repository |
|---|---|
| Author preprint | `pitchayaw/baa-preprint` |
| Image preprocessing | `Khao0/HandXRay-Preprocessing` |
| Bone-age model / hierarchical adaptation | `Khao0/HiDA-BAA` |

For reproducibility, users should consult the software repositories corresponding to the methods described in the manuscript.

---

## Citation

If you refer to this work before the final journal article becomes available, please cite this repository as an **author preprint**.

### Suggested citation

> Wiratchotisatian P, Tangprasert K, Paisarnsrisomsuk S, Hanpinitsak P, Chaisiwamongkol W, Chaisiwamongkol R, Tewattanarat N, Poonpol C, Pansukrada C, Thaowandee W. **Beyond Benchmark Accuracy: Hierarchical Transfer Learning and ROI Standardization for Bone Age Assessment in Thai Children.** Author preprint. Version 1.0. 2026.

### BibTeX

```bibtex
@misc{wiratchotisatian2026beyond,
  author = {
    Pitchaya Wiratchotisatian and
    Khwankaow Tangprasert and
    Sarun Paisarnsrisomsuk and
    Panawit Hanpinitsak and
    Wichuda Chaisiwamongkol and
    Ratikorn Chaisiwamongkol and
    Nipaporn Tewattanarat and
    Chanakarn Poonpol and
    Chatparin Pansukrada and
    Wilairat Thaowandee
  },
  title = {
    Beyond Benchmark Accuracy:
    Hierarchical Transfer Learning and ROI Standardization
    for Bone Age Assessment in Thai Children
  },
  year = {2026},
  month = {August},
  note = {Author preprint, Version 1.0. Manuscript submitted to IEEE for possible publication},
  url = {https://github.com/pitchayaw/baa-preprint}
}
```

When a peer-reviewed version becomes available, please cite the final journal publication instead of this preprint.

## Data and Resources
The study uses public bone-age datasets together with a retrospective clinical cohort from Khon Kaen University.
Public datasets used in the study include:
- RSNA Pediatric Bone Age Challenge dataset
- Digital Hand Atlas (DHA)
The Thai clinical data used in this study contain protected medical information and are subject to institutional ethics, privacy, and data-governance requirements. Their inclusion in the study does not imply that the original clinical radiographs are publicly redistributable.

## Publicly shareable preprocessing resources are linked through:
https://github.com/Khao0/HandXRay-Preprocessing

## Ethics
The retrospective clinical component of the study was approved by the Research Ethics Committee of the Faculty of Medicine, Khon Kaen University.
Protocol: HE674010
The requirement for informed consent was waived because the study used retrospective, anonymized clinical data.

## Funding
This research was supported by the Digital Economy and Society Fund, Thailand
Grant No. PR66010158.

## Important Notice
The PDF in this repository is an author preprint.
It is not the final IEEE-published article and should not be described as:
- accepted,
- in press,
- forthcoming,
- published by IEEE, or
- peer reviewed by IEEE
unless and until such status is formally confirmed by the publisher.

The software repositories linked above have their own software licenses. Those licenses should not be interpreted as applying automatically to the manuscript PDF contained in this repository.

Contact
For correspondence concerning the manuscript:
Panawit Hanpinitsak
Department of Computer Engineering
Faculty of Engineering
Khon Kaen University
Khon Kaen 40002, Thailand
Email: panaha@kku.ac.th
