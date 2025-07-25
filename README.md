# HARM

## SBIC-Explain 

The dataset proposed by this work is based on the [original SBIC dataset](./README.md#original-sbic-reference).

The dataset is in the parquet format and can be loaded using pandas:

```python
import pandas as pd

sbic_explain = pd.read_parquet("./SBIC-Explain.parque.gzip")
```

### General metrics

| Metric    | Value |
| -------- | ------- |
| Instances  | 123596    |
| Posts  | 30899    |

### Number of instances per model

| base_model                |   count |
|:--------------------------|--------:|
| Falcon3-10B-Instruct-Q8_0 |   30899 |
| Gemma-3-27b-it-Q4_0       |   30899 |
| Phi4-14B-Q8_0             |   30899 |
| Qwen3-14B-Q8_0            |   30899 |

### Statistics of `is_offensive` annotation.

|       |   is_offensive |
|:------|---------------:|
| mean  |       0.532562 |
| std   |       0.457962 |
| min   |       0        |
| 25%   |       0        |
| 50%   |       0.5      |
| 75%   |       1        |
| max   |       1        |

# References

## Harm-reference

```
To be filled
```

## Original SBIC-reference

```
@inproceedings{sap-etal-2020-social,
    title = "Social Bias Frames: Reasoning about Social and Power Implications of Language",
    author = "Sap, Maarten  and
      Gabriel, Saadia  and
      Qin, Lianhui  and
      Jurafsky, Dan  and
      Smith, Noah A.  and
      Choi, Yejin",
    booktitle = "Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.acl-main.486",
    doi = "10.18653/v1/2020.acl-main.486",
    pages = "5477--5490",
    abstract = "Warning: this paper contains content that may be offensive or upsetting. Language has the power to reinforce stereotypes and project social biases onto others. At the core of the challenge is that it is rarely what is stated explicitly, but rather the implied meanings, that frame people{'}s judgments about others. For example, given a statement that {``}we shouldn{'}t lower our standards to hire more women,{''} most listeners will infer the implicature intended by the speaker - that {``}women (candidates) are less qualified.{''} Most semantic formalisms, to date, do not capture such pragmatic implications in which people express social biases and power differentials in language. We introduce Social Bias Frames, a new conceptual formalism that aims to model the pragmatic frames in which people project social biases and stereotypes onto others. In addition, we introduce the Social Bias Inference Corpus to support large-scale modelling and evaluation with 150k structured annotations of social media posts, covering over 34k implications about a thousand demographic groups. We then establish baseline approaches that learn to recover Social Bias Frames from unstructured text. We find that while state-of-the-art neural models are effective at high-level categorization of whether a given statement projects unwanted social bias (80{\%} F1), they are not effective at spelling out more detailed explanations in terms of Social Bias Frames. Our study motivates future work that combines structured pragmatic inference with commonsense reasoning on social implications.",
}
```