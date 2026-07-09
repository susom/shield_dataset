# SHIELD: A Diverse Clinical Note Dataset for Enterprise-Scale De-identification

## Abstract

De-identification of clinical text is a prerequisite for the secondary use of electronic health records. Existing public benchmarks such as the i2b2 2006 and 2014 corpora are over a decade old and lack the semantic and demographic diversity of modern clinical narratives. Large Language Models (LLMs) reach state-of-the-art zero-shot extraction, but their use at enterprise scale is limited by computational cost and by hospital data governance that restricts sending Protected Health Information (PHI) to cloud APIs. We introduce SHIELD (Synthetic Human-annotated Identifier-replaced Entries for Learning and De-identification), a diverse clinical note dataset of 1,381 notes with 10,229 gold-standard PHI spans across 9 categories, built with set-cover diversity sampling across demographic and document-type strata and human-in-the-loop adjudication. We evaluate four LLMs (two proprietary, two open-weight) to establish a performance ceiling on SHIELD, then show that a teacher-student distillation framework transfers these capabilities into locally deployable Small Language Models. Our best distilled model reaches micro-averaged span-level precision of 0.89 and recall of 0.88 while running on standard workstation hardware. It trails its cloud teacher on per-category recall (0.90 vs. 0.81 macro-averaged) but remains competitive given its lower cost and on-premise deployability. Cross-dataset evaluation shows that diversity-trained models generalize well on universal structured PHI categories, while institution-specific entities remain hard to transfer in both directions, which suggests pairing broad-coverage models with specialized models for high-volume, semi-structured note types. We publicly release the SHIELD dataset and the distilled DeBERTa v3 model to provide an accurate, cost-effective de-identification pipeline deployable entirely behind institutional firewalls.

**Paper:** [arXiv:2605.03301](https://arxiv.org/abs/2605.03301)

## Access

The SHIELD dataset is hosted on Stanford Medicine Redivis. Click [here](https://stanford.redivis.com/datasets/ee4n-6gv2f84et) to access. 

## Citation

```bibtex
@article{posada2025shield,
  title={SHIELD: A Diverse Clinical Note Dataset and Distilled Small Language Models for Enterprise-Scale De-identification},
  author={Posada, Jose D. and Love, David and Datta, Somalee and Desai, Priya},
  journal={arXiv preprint arXiv:2605.03301},
  year={2025}
}
```

## Contact

Jose D. Posada — jdposada@stanford.edu
