# IEEE_CSDE-BanglaSentiEmo
Official implementation of the IEEE CSDE 2026 paper:
"BanglaSentiEmo: Diagnosing Cross-Task Affective Structure and Transfer with a Shared BanglaBERT Encoder for Bengali Sentiment-Emotion Classification"

Key finding: Bengali sentiment and emotion labels are strongly associated (Cramér's V ≈ 0.68), but a hard-parameter-sharing BanglaBERT model shows no statistically significant macro-F1 advantage over matched single-task models (exact paired permutation tests, p = 0.5625 and p = 0.8750). Strong task relatedness does not guarantee positive multi-task transfer. The shared encoder does, however, reduce parameters by 49.9%.

Overview
A single shared BanglaBERT encoder with two task-specific heads:

Sentiment: 5-class (Very Negative, Negative, Neutral, Positive, Very Positive)

Emotion: 7-class source-defined taxonomy (Happy, Calm, Fearful, Sexual, Hateful, Surprised, Religious)

Compared against matched single-task (STL) baselines using the same backbone, optimizer, loss, and training budget. The only architectural difference is parameter sharing.

## Setup
git clone https://github.com/<your-username>/IEEE_CSDE-BanglaSentiEmo.git
cd IEEE_CSDE-BanglaSentiEmo
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt


## Dataset

The dataset is not redistributed here. Download it from Mendeley Data V2:
DOI [10.17632/6bnbF33nnw.2](https://doi.org/10.17632/6bnbF33nnw.2)

python src/data/deduplicate.py --config configs/mtl.yaml
python src/data/preprocess.py --config configs/mtl.yaml

